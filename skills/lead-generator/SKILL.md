---
name: lead-generator
description: "B2B lead generation agent for Inbound LLC fleet/telematics sales prospecting. Use whenever the user wants to find companies, build a prospect list, generate leads, scrape contacts, or create a sales pipeline. Sources: Google Maps, 2GIS, UAE business directories, LinkedIn, company websites. Trigger on: find me companies, build a lead list, prospect for fleet clients, find transport companies in X, create a contact sheet, get me leads, build an outreach list, find logistics companies in Dubai. Always trigger even for just a quick list — always outputs a formatted .xlsx with: Company Name, Industry/Category, Phone/WhatsApp, Email, Website, LinkedIn, Address, City, Country, Lat, Long, Google Maps Rating, Reviews, Source, Notes."
---

# Lead Generator

A structured lead generation agent for Inbound LLC sales prospecting. Gathers company contact
data from multiple open sources and outputs a clean, enriched Excel file ready for CRM import
or outreach campaigns.

---

## Workflow

### Step 1 — Clarify the Target (if not already provided)

Ask the user for:
- **Industry / company type** — e.g. "logistics companies", "school bus operators", "government fleets"
- **Geography** — e.g. "Dubai", "Abu Dhabi", "GCC", "UAE + KSA"
- **Target size** — e.g. "SME", "enterprise", "any"
- **Number of leads** — e.g. "20 companies", "as many as possible"

If the user has already provided these, skip to Step 2.

---

### Step 2 — Multi-Source Scraping

Run **all sources in parallel** using `web_search` and `web_fetch`. For each source, collect
raw data and note the source name per company row.

#### Source A — Google Maps
Search queries to run (adapt to the target industry/city):
```
"<industry> companies <city> UAE" site:google.com/maps OR maps.google.com
"<industry> <city>" google maps
```
Then fetch the Google Maps search results page or individual listing pages using `web_fetch`.
Extract: company name, phone, address, rating, review count, website, category.

Also try:
```
"<industry> <city> contact phone email" -site:linkedin.com
```

#### Source B — 2GIS
2GIS covers UAE and GCC with rich business directory data.
```
https://2gis.ae/search/<industry>%20<city>
```
Fetch the page and extract business listings. 2GIS often includes phone numbers directly.

#### Source C — UAE Business Directories
Run searches on:
- **YellowPages UAE**: `site:yellowpages.ae "<industry>" "<city>"`
- **Dubai Chamber**: `site:dubaichamber.com "<industry>"`
- **Abu Dhabi Chamber**: `site:abudhabichamber.ae "<industry>"`
- **Kompass UAE**: `site:ae.kompass.com "<industry>"`

Web-fetch the result pages and extract company listings.

#### Source D — LinkedIn (Public Profiles)
```
site:linkedin.com/company "<industry>" "<city>" UAE
```
Extract company LinkedIn URLs and names. Do NOT attempt to log in or bypass LinkedIn.
Only use publicly available search snippets.

#### Source E — Company Websites
For each company found in Sources A–D that has a website URL:
1. `web_fetch` the homepage → look for email addresses, phone numbers in footer/header
2. If not found, `web_fetch` the `/contact` or `/contact-us` page
3. Extract: email, phone/WhatsApp number, address

---

### Step 3 — Geocoding (Latitude / Longitude)

For each company with a physical address, attempt to resolve lat/long by:
1. Searching `"<company name> <address> coordinates"` or using a Google Maps embed URL
2. If a Google Maps link is found (e.g. `maps.google.com/?q=...`), extract coordinates from the URL
3. If not resolvable, leave blank — never guess coordinates

---

### Step 4 — Deduplicate & Enrich

- Remove duplicate companies (match on name + phone or name + website)
- Standardise phone numbers to E.164 format: `+971XXXXXXXXX`
- Normalise city names: "Dubai", "Abu Dhabi", "Sharjah", "Ajman", "RAK", "Fujairah", "Al Ain"
- Set Country = "UAE" unless another country was explicitly targeted
- For the **Notes** column, add a 1-line qualification note, e.g.:
  - "Fleet operator — likely has 20+ vehicles"
  - "School bus company — strong IVMS fit"
  - "Logistics SME — potential GPS tracking prospect"

---

### Step 5 — Generate Excel File

Use the Python script at `scripts/build_leads_excel.py` to produce the `.xlsx` output.

Pass the collected data as a Python list of dicts. Each dict has these keys:
```python
{
  "company_name": str,
  "industry": str,
  "phone": str,
  "email": str,
  "website": str,
  "linkedin": str,
  "address": str,
  "city": str,
  "country": str,
  "latitude": float | str,   # empty string if unknown
  "longitude": float | str,  # empty string if unknown
  "gmaps_rating": float | str,
  "gmaps_reviews": int | str,
  "source": str,             # "Google Maps", "2GIS", "YellowPages UAE", etc.
  "notes": str
}
```

Run the script:
```bash
cd /home/claude
python lead-generator/scripts/build_leads_excel.py '<json_data>' '<output_path>'
```

Where `<json_data>` is the JSON-encoded list and `<output_path>` is e.g.
`/mnt/user-data/outputs/leads_dubai_logistics_2026.xlsx`

---

### Step 6 — Present the File

Use `present_files` to deliver the Excel file to the user.

Then provide a brief summary:
- Total leads found
- Breakdown by source
- How many have email / phone / both
- Top 3–5 highest-rated companies highlighted

---

## Output Schema

| Column | Description |
|---|---|
| Company Name | Full legal or trading name |
| Industry / Category | e.g. "Logistics", "School Transport", "Government Fleet" |
| Phone / WhatsApp | E.164 format (+971...) |
| Email | Direct contact or info@ email |
| Website | Full URL |
| LinkedIn Profile | linkedin.com/company/... URL |
| Physical Address | Street, area |
| City | Dubai / Abu Dhabi / Sharjah etc. |
| Country | UAE (or other if applicable) |
| Latitude | Decimal degrees |
| Longitude | Decimal degrees |
| Google Maps Rating | 1.0–5.0 |
| No. of Reviews | Integer |
| Source | Where the lead was found |
| Notes | 1-line qualification note |

---

## Quality Rules

- **Never fabricate** phone numbers, emails, or addresses. Leave blank if not found.
- **Always cite the source** for every company row.
- **Minimum viable lead**: must have at least Company Name + one contact method (phone OR email OR website).
- If a company has no contact info at all after checking website, mark Notes as "No contact found — manual lookup needed".
- Do not scrape or store any data that requires authentication (LinkedIn login, paid directories).
- Respect robots.txt — if a site blocks scraping, note it and skip.

---

## Fleet/Telematics Qualification Tags

When writing the Notes column, use these tags to help Inbound LLC sales team prioritise:

| Tag | Meaning |
|---|---|
| 🚌 School Transport | School bus operators — IVMS/GPS compliance required by RTA |
| 🚛 Logistics Fleet | Freight/delivery companies — fuel & route optimisation use case |
| 🏗️ Construction Fleet | Heavy equipment & site vehicles — asset tracking use case |
| 🏥 Medical Transport | Ambulance/healthcare fleets — strict compliance requirements |
| 🏛️ Government Fleet | Municipalities, semi-gov — tender opportunity, long sales cycle |
| 🚕 Ride-hailing / Taxi | High-volume, telematics-ready — driver behaviour monitoring |

Add the relevant emoji tag at the start of the Notes field for quick visual scanning.

---

## Example Invocations

- "Find me 30 logistics companies in Dubai for fleet tracking outreach"
- "Scrape Google Maps for school bus operators in Abu Dhabi"
- "Build a lead list of construction companies in Sharjah with their contacts"
- "Get me contacts for transport companies in Saudi Arabia"
- "Find fuel distribution companies in UAE for GPS tracking pitch"
