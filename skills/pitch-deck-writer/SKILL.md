---
name: pitch-deck-writer
description: "Create, structure, review, and improve pitch decks for any context — fundraising, client/sales, partnership/BD, portfolio company coaching, or social media management. Use this skill whenever the user mentions 'pitch deck', 'investor deck', 'sales deck', 'partnership deck', 'fundraising presentation', 'client presentation', 'help me pitch', 'build a deck', 'review my deck', 'restructure my deck', or asks to adapt one deck type into another. Also trigger when the user provides raw notes or ideas and wants them turned into a presentation for an audience they need to persuade. Covers from-scratch creation, restructuring messy decks, reviewing/improving drafts, and adapting between deck types. Chains into the pptx skill for .pptx file output."
---

# Skill: Pitch Deck Writer

## Trigger

Activate this skill when the user asks to create, write, structure, review, or improve a pitch deck, investor deck, sales deck, partnership deck, or fundraising presentation.

Keywords: "pitch deck", "investor deck", "fundraising deck", "sales deck", "partnership deck", "client presentation", "write a deck", "build a deck", "help me pitch", "deck for investors", "restructure my deck", "review my deck", "adapt this deck"

## Context

Pitch decks are the highest-leverage documents a founder or operator creates. A great deck doesn't just inform — it compels action: an investment, a partnership, a signed contract. Yet most decks fail for the same reasons: too much text, no narrative arc, buried ask, missing proof points.

This skill covers five deck types, each with a distinct structure and audience psychology:

| Deck Type | Audience Mindset | Core Question They're Asking |
|-----------|-----------------|------------------------------|
| **Fundraising** | "Will I get my money back 10x?" | Why this team, this market, this moment? |
| **Portfolio Company** | "Will I get my money back 10x?" | Same as fundraising, but you're coaching the founder |
| **Client / Sales** | "Will this solve my problem and be worth the cost?" | What's the ROI and can I trust this team to deliver? |
| **Partnership / BD** | "Is this worth my time and does it make us look good?" | What's the mutual upside and who else is in? |
| **Social Media Mgmt** | "Will this grow my brand and is the pricing fair?" | What's the strategy, what results can I expect? |

This skill handles four workflows:
1. **From scratch** — raw notes, ideas, or a conversation → structured deck
2. **Restructure** — existing messy deck → clean narrative
3. **Review & improve** — draft deck → specific, actionable feedback
4. **Adapt** — convert one deck type into another (e.g. investor → client)

**Output is always a .pptx file.** After structuring the content, chain into the pptx skill (`/mnt/skills/public/pptx/SKILL.md`) for file creation. Read pptxgenjs.md for creating from scratch, or editing.md if working from an existing template.

## Instructions

### Step 1: Identify the Mode and Deck Type

Determine what the user needs:

**Mode detection:**
- User provides raw notes, ideas, or a topic → **From Scratch**
- User uploads or pastes an existing deck → **Restructure** or **Review**
- User says "turn this into a [different type] deck" → **Adapt**

**If the deck type isn't obvious, ask:**
"What kind of deck is this? Fundraising, client/sales, partnership, social media management, or portfolio company pitch?"

**If the audience isn't clear, ask:**
"Who's seeing this? (e.g. Series A investors, a government procurement committee, a potential enterprise client, a brand looking for social media help)"

Do not proceed without knowing the deck type and audience.

### Step 2: Gather the Raw Material

**From Scratch:** Ask for whatever the user has — bullet points, a paragraph, a voice memo transcript, a previous deck, or just a conversation. The messier the better. Extract structure from chaos; never ask the user to organize first.

**Restructure:** Read the existing deck (use `python -m markitdown` if .pptx). Identify what's there, what's missing, and what's in the wrong order.

**Review:** Read the deck. Apply the Review Framework (Step 5). Skip Steps 3-4.

**Adapt:** Read the source deck. Map content to the target deck type's structure. Identify gaps that the new audience needs answered.

### Step 3: Build the Narrative Arc

Every great deck follows a narrative arc, not just a slide order. The arc differs by deck type, but the principle is universal: **setup → tension → resolution → proof → ask.**

**Fundraising / Portfolio Company Deck (10-14 slides):**

| # | Slide | Purpose | Time |
|---|-------|---------|------|
| 1 | **Title** | Company name, one-line description, your name | 5 sec |
| 2 | **Problem** | The pain. Make the audience FEEL it. One specific scenario, not abstract market forces. | 30 sec |
| 3 | **Solution** | Your product in one sentence + one visual. If you need a paragraph, you don't understand it well enough. | 30 sec |
| 4 | **Why Now** | Market shift, regulatory change, technology inflection, behavioral change. The tailwind that makes this inevitable. | 20 sec |
| 5 | **Market Size** | TAM → SAM → SOM. Show the math. Bottom-up sizing beats top-down every time. "$50B market" means nothing without "and here's how we capture $50M of it." | 30 sec |
| 6 | **Product / Demo** | Screenshots, workflow, or demo video link. Show, don't tell. | 45 sec |
| 7 | **Traction** | The proof slide. Revenue, users, growth rate, key partnerships, LOIs. If pre-revenue: waitlist, pilot results, LOIs. If pre-product: founder-market fit evidence. Graph going up and to the right. | 30 sec |
| 8 | **Business Model** | How you make money. Unit economics if available. Pricing model. Path to margins. | 20 sec |
| 9 | **Competition** | NOT a feature matrix. Position on 2 axes that you chose because you win on both. Show the strategic wedge. | 20 sec |
| 10 | **Team** | Why THIS team wins. Relevant experience only. "Ex-Google" means nothing unless you shipped the relevant thing at Google. | 20 sec |
| 11 | **Financials** | 3-year projection. Key assumptions labeled. Show when you break even. | 20 sec |
| 12 | **The Ask** | Amount raising, use of funds (3-4 buckets), milestones this capital unlocks. | 15 sec |
| 13 | **Closing** | Contact info, one memorable line, appendix reference | 5 sec |

**Client / Sales Deck (8-12 slides):**

| # | Slide | Purpose |
|---|-------|---------|
| 1 | **Title** | Your company + client's name. Personalize it. |
| 2 | **Their Problem** | Mirror their pain back to them. Use their language, their industry, their metrics. |
| 3 | **Cost of Inaction** | Quantify what doing nothing costs. "Every month without GPS tracking, your fleet loses an average of X hours to route inefficiency." |
| 4 | **Solution Overview** | What you do, in their terms. Not your feature list — their outcome. |
| 5 | **How It Works** | 3-step process max. Make it feel simple even if the technology isn't. |
| 6 | **Proof / Case Studies** | Specific results from similar clients. Numbers, not testimonials. "Emirates Transport reduced fuel waste by X% in Y months." |
| 7 | **Why Us** | Your differentiators, framed as their advantages. Not "we have 15 years experience" but "15 years means we've seen every edge case your fleet will encounter." |
| 8 | **Pricing / Packages** | Clear options. Anchor with the recommended package. |
| 9 | **Implementation** | Timeline, onboarding process, what they need to do (keep it minimal). |
| 10 | **Next Steps / CTA** | One clear action. "Let's run a 30-day pilot with 10 vehicles." |

**Partnership / BD Deck (8-10 slides):**

| # | Slide | Purpose |
|---|-------|---------|
| 1 | **Title** | Both organizations' names. Frame as collaboration. |
| 2 | **Shared Opportunity** | The market gap or initiative that benefits both parties. |
| 3 | **Why Together** | What each party brings. Be honest about complementary strengths. |
| 4 | **Proposed Structure** | How the partnership works operationally. Roles, responsibilities, governance. |
| 5 | **Consortium / Team** | Who's involved and their credentials. If multi-party (like a consortium bid), show the org chart. |
| 6 | **Track Record** | Past successes of each partner, ideally in collaboration. |
| 7 | **Financials / Investment** | Budget, revenue share, cost allocation — whatever applies. |
| 8 | **Timeline & Milestones** | Phased approach with clear deliverables per phase. |
| 9 | **Risk Mitigation** | Acknowledge risks, show you've thought about them. |
| 10 | **Ask / Next Steps** | What you need from them and by when. |

**Social Media Management Deck (8-10 slides):**

| # | Slide | Purpose |
|---|-------|---------|
| 1 | **Title** | Your agency/service name + client's brand. |
| 2 | **Their Current State** | Audit snapshot: current followers, engagement rate, content gaps. Be honest but tactful. |
| 3 | **The Opportunity** | What's being left on the table. Competitor benchmarks, audience growth potential. |
| 4 | **Strategy Overview** | Content pillars, platform focus, posting cadence, tone of voice. |
| 5 | **Content Examples** | Mock posts, content calendar sample, creative direction. Show, don't describe. |
| 6 | **Process & Workflow** | How approvals work, reporting cadence, communication channels. |
| 7 | **Results / Case Studies** | Past client results with specific metrics. Growth percentages, engagement lifts. |
| 8 | **Packages & Pricing** | Tiered options. Anchor with recommended package. |
| 9 | **Timeline** | Onboarding → first month → ramp-up → steady state. |
| 10 | **Next Steps** | Clear CTA. "Let's start with a 1-month trial on Instagram." |

### Step 4: Write the Slide Content

For each slide, produce:

```
SLIDE [#]: [Title]
Layout: [layout suggestion — e.g. "Two-column: stat callouts left, supporting text right"]
Visual: [what visual element belongs here — chart, screenshot, icon grid, image]

Headline: [The one sentence that makes the slide's point]
Body:
- [Bullet or short paragraph — max 25 words per bullet]
- [Max 4 bullets per slide. If you need more, you need two slides.]

Speaker Notes: [What the presenter says that ISN'T on the slide. 2-3 sentences.]
```

**Slide writing rules:**
- **One idea per slide.** If a slide makes two points, split it.
- **Headlines do the work.** A reader who only reads headlines should get 80% of the story.
- **25-word max per bullet.** If a bullet needs a second line, rewrite it.
- **4 bullets max per slide.** Slides are visual aids, not documents.
- **Every slide needs a visual element.** Text-only slides are forgettable. Charts, images, icons, screenshots — something.
- **Numbers over adjectives.** "40% faster" beats "significantly faster." "$1.2M ARR" beats "strong traction."
- **Kill jargon unless the audience speaks it.** Investors don't know "Wialon Nimbus." Fleet managers don't know "ARR."

### Step 5: Review Framework (for Review mode)

When reviewing an existing deck, evaluate across these dimensions:

**1. Narrative Flow**
- Does the deck tell a story, or is it a stack of unrelated slides?
- Is there a clear setup → tension → resolution arc?
- Would shuffling the slides break anything? (If not, the narrative is weak.)

**2. Slide Density**
- Can each slide be understood in under 10 seconds?
- Are there walls of text? (More than 6 lines on any slide = problem.)
- Is every word earning its place?

**3. Proof Points**
- Is every claim backed by evidence? Numbers, case studies, data?
- Are there unsupported superlatives? ("Best-in-class," "revolutionary," "cutting-edge")
- Would a skeptic buy it?

**4. The Ask**
- Is the ask clear and specific?
- Is it on its own slide? (Never bury the ask.)
- Does every preceding slide build toward it?

**5. Visual Design**
- Is there consistent visual language across slides?
- Do slides have visual variety, or is it the same layout repeated?
- Is the hierarchy clear? (What do you look at first, second, third?)

Deliver feedback in the same tiered format as the Product Design Reviewer skill:
- **Must Fix**: Issues that will lose the audience or kill the deal.
- **Should Fix**: Issues that weaken the deck meaningfully.
- **Consider**: Polish that would elevate it.

### Step 6: Generate the .pptx

After the user approves the slide content (or after making review edits):

1. Read `/mnt/skills/public/pptx/SKILL.md`
2. Follow its instructions to create the .pptx — use `pptxgenjs.md` for from-scratch creation
3. Choose a color palette and typography that matches the deck's tone and industry (refer to the pptx skill's Design Ideas section)
4. Run the QA process from the pptx skill (content QA + visual QA)
5. Present the final .pptx to the user

**Color palette guidance by deck type:**
- Fundraising: Bold and confident. Deep navy, teal, or charcoal with a sharp accent.
- Client/Sales: Trust-building. Clean blues, teals, or forest greens. Not flashy.
- Partnership: Collaborative. Warm tones — terracotta, sage, or warm neutrals.
- Social Media: Energetic. Coral, berry, or vibrant but not garish.

## Constraints

- Maximum 14 slides for any deck type. If the content needs more, you're putting too much on slides — move detail to an appendix or leave-behind document.
- No slide should have more than 6 lines of text (excluding the title).
- Every bullet must be under 25 words.
- Speaker notes are mandatory for every slide. The best decks are presentation aids, not standalone documents.
- Never use "synergy," "leverage," "robust," "cutting-edge," "disruptive," "best-in-class," or "world-class" unless quoting real data.
- Never put a URL on a slide unless it's a demo link or QR code.
- The Ask slide is never optional. Every deck must end with a clear, specific request.

## Output Format

**For From Scratch / Restructure / Adapt modes:**

First, present the slide outline for approval:

```
## Deck Outline: [Deck Name]
Type: [Fundraising / Client / Partnership / Social Media]
Audience: [who]
Slide count: [#]

Slide 1: [Title] — [one-line purpose]
Slide 2: [Title] — [one-line purpose]
...
```

After approval, write full slide content, then generate the .pptx.

**For Review mode:**

Present feedback in tiered format (Must Fix / Should Fix / Consider), then offer to implement the fixes.

## Examples

### Example 1: Fundraising Deck from Raw Notes

**User says:** "I need a pitch deck for Yetu Car Finance. We're raising $500K pre-seed. It's drive-to-own vehicle financing for gig drivers in Kinshasa, DRC. Cars sourced from Dubai, 24-month lease-to-own, integrated with Yango platform. Co-founders are me, Baraka, Chango, and Fabrice."

**Claude produces:**

```
## Deck Outline: Yetu Car Finance
Type: Fundraising (Pre-Seed)
Audience: Angel investors, pre-seed funds
Slide count: 12

Slide 1: Title — Yetu Car Finance: Drive-to-Own for Africa's Gig Economy
Slide 2: Problem — Gig drivers in Kinshasa can't access vehicles. No financing, no credit history, no options.
Slide 3: Solution — 24-month lease-to-own. Dubai-sourced vehicles. Integrated with Yango.
Slide 4: Why Now — Ride-hailing expanding across DRC. 50K+ Yango drivers, <5% own their vehicle.
Slide 5: Market Size — Bottom-up: 50K Yango drivers × $200/mo × 24 months = $240M addressable in Kinshasa alone.
Slide 6: How It Works — 3-step visual: Apply → Get vehicle → Drive & pay monthly → Own.
Slide 7: Traction — [Ask user: any LOIs, pilot results, waitlist numbers?]
Slide 8: Business Model — Monthly lease payments, vehicle markup, insurance commission.
Slide 9: Competition — Positioning map: affordability vs. gig-platform integration.
Slide 10: Team — 4 co-founders with Dubai sourcing, DRC operations, and fintech backgrounds.
Slide 11: Financials — Path to 200 vehicles in Year 1, breakeven at 120 vehicles.
Slide 12: The Ask — $500K pre-seed. Use of funds: 60% vehicle acquisition, 25% ops, 15% tech.
```

Then asks: "Does this structure work? I have a question about the Traction slide — do you have any pilot data, LOIs, or waitlist numbers I can include?"

### Example 2: Client Sales Deck for Inbound LLC

**User says:** "I need a sales deck for a potential client — a logistics company with 200 trucks. They're losing money on fuel and have no route visibility."

**Claude produces:**

```
## Deck Outline: Inbound Fleet Management
Type: Client / Sales
Audience: Logistics company operations director
Slide count: 10

Slide 1: Title — Inbound LLC × [Client Name]: Fleet Intelligence for 200+ Vehicles
Slide 2: The Problem — You're managing 200 trucks with limited visibility. Fuel costs are rising and you can't pinpoint why.
Slide 3: Cost of Inaction — Industry data: fleets without GPS tracking lose 15-25% on fuel waste and unauthorized usage.
Slide 4: Solution — Real-time GPS tracking, geofencing, fuel monitoring, and driver behavior analytics via Wialon.
Slide 5: How It Works — Install → Connect → Monitor. Live dashboard within 48 hours.
Slide 6: Results — Emirates Transport case study: [X]% fuel reduction, [Y] hours saved weekly on route planning.
Slide 7: Why Inbound — 13+ years in UAE fleet management. 24/7 monitoring. Arabic + English support.
Slide 8: Packages — Starter (tracking only) / Professional (tracking + fuel + alerts) / Enterprise (full suite + dedicated support).
Slide 9: Implementation — Week 1: Install. Week 2: Training. Week 3: Live monitoring. Week 4: First optimization report.
Slide 10: Next Steps — "Let's run a 30-day pilot with 20 vehicles. Free setup. You keep the data either way."
```

### Example 3: Reviewing an Existing Deck

**User says:** "Review my deck" + uploads .pptx

**Claude produces:**

```
## Deck Review: [Deck Name]

What works:
- Strong problem slide — specific scenario, not abstract
- Traction numbers are impressive and well-presented
- Clean visual design, consistent color palette

Must Fix:

1. No narrative arc — slides read like a checklist, not a story
   WHY: Investors make emotional decisions justified by logic. A list of facts
   doesn't compel action. The deck needs tension (problem) → release (solution)
   → proof (traction) → opportunity (ask).
   FIX: Reorder slides to follow the fundraising arc. Move the market size
   slide before solution to establish stakes.

2. The Ask is buried on slide 11 with three other topics
   WHY: The most important slide in the deck is sharing space with team bios
   and a timeline. Investors need a dedicated slide that says exactly what you
   want and what they get.
   FIX: Dedicated Ask slide. Amount, use of funds (3 buckets), milestones
   this capital unlocks. Nothing else on the slide.

Should Fix:

3. Slide 6 has 14 lines of text
   WHY: No investor reads 14 lines on a slide. They'll skip it entirely and
   miss your product explanation.
   FIX: Cut to 4 bullets max. Move detail to speaker notes. Add a product
   screenshot or workflow diagram.

Consider:

4. Competition slide uses a feature matrix
   WHY: Feature matrices are defensive — they invite line-by-line comparison.
   A 2-axis positioning map lets you choose the axes you win on.
   FIX: Replace with a quadrant chart. X-axis: [relevant dimension].
   Y-axis: [relevant dimension]. You're in the top-right.

Want me to implement these fixes and generate an updated .pptx?
```

## Anti-patterns

- DO NOT create slides with walls of text. If a slide has more than 6 lines, split it or move content to speaker notes. Slides are visual aids, not documents.
- DO NOT use generic superlatives without evidence. "Best-in-class solution" is meaningless. "40% faster than the nearest competitor (source: internal benchmark, Jan 2025)" is a claim.
- DO NOT skip the Ask slide. Every deck exists to drive an action. No ask = no point.
- DO NOT use a feature comparison matrix for competition slides. They invite line-by-line scrutiny and put you on defense. Use a 2-axis positioning map where you chose the axes.
- DO NOT make every slide the same layout. Vary between stat callouts, two-column, icon grids, and visual-heavy slides. Repetitive layouts signal lazy thinking.
- DO NOT create a deck longer than 14 slides. If you can't tell the story in 14 slides, you don't understand it well enough. Move supplementary detail to an appendix.
- DO NOT start writing slides before the user confirms the outline. Structure first, content second. Rewriting 12 slides is expensive; reordering an outline is free.
- DO NOT include speaker notes that just repeat the slide text. Speaker notes contain what the presenter SAYS — context, anecdotes, data points, transitions — not what's already on screen.
- AVOID starting any slide title with "Our" — it makes every slide self-referential. Frame from the audience's perspective. Not "Our Solution" but "How It Works." Not "Our Team" but "Who's Building This."
- AVOID putting logos of partners or clients on slides without confirmation that you have permission to use them.
