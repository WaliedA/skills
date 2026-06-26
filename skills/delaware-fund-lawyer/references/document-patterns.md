# Document Patterns — Fund Formation

Templates, structures, and conventions for drafting Delaware fund formation documents.

## Table of Contents

1. [General Drafting Conventions](#general)
2. [Limited Partnership Agreement (LPA)](#lpa)
3. [Operating Agreement (LLC)](#operating-agreement)
4. [Certificate of Limited Partnership](#certificate-lp)
5. [Certificate of Formation (LLC)](#certificate-llc)
6. [Subscription Agreement](#subscription)
7. [Side Letter](#side-letter)
8. [Capital Call Notice](#capital-call)
9. [Distribution Notice](#distribution-notice)

---

## General Drafting Conventions {#general}

### Defined Terms
- Capitalize all defined terms: "Limited Partners," "Management Fee," "Investment Period"
- Collect definitions in Article I / Section 1, or use inline definitions on first use with "(as defined herein)"
- Cross-reference definitions when used in operative sections
- Use consistent defined terms across related documents (LPA, sub docs, side letters should use same terms)

### Variable Terms
- Mark all deal-specific terms with square brackets: `[Fund Name]`, `[●]%`, `[Target Fund Size]`
- Include practitioner notes in brackets for judgment calls: `[NTD: Consider whether to include LPAC consent requirement here]`
- For dates, use: `[●], 20[●]` format

### Section Structure
Standard legal document flow:
1. Title and parties
2. Recitals ("WHEREAS" clauses)
3. Definitions (Article I)
4. Operative provisions (Articles II–XII+)
5. General provisions (severability, entire agreement, governing law, counterparts)
6. Signature blocks
7. Exhibits/Schedules

### Governing Law
Always Delaware for Delaware entities:
```
This Agreement shall be governed by and construed in accordance with the laws of
the State of Delaware without regard to the conflicts of law principles thereof.
```

### Signature Blocks
```
[GENERAL PARTNER]
[GP Entity Name], a Delaware limited liability company

By: ___________________________
Name: [●]
Title: [Managing Member / Authorized Person]

[LIMITED PARTNER]
[LP Name]

By: ___________________________
Name: [●]
Title: [●]
```

---

## Limited Partnership Agreement (LPA) {#lpa}

The LPA is the master governing document for a Delaware limited partnership fund. Typical structure:

### Article Outline

```
AMENDED AND RESTATED AGREEMENT OF LIMITED PARTNERSHIP
OF
[FUND NAME], L.P.

Article I    — Definitions
Article II   — Organization
Article III  — Partners; Capital Commitments
Article IV   — Capital Contributions; Default
Article V    — Management Fee; Fund Expenses
Article VI   — Allocations and Distributions; Carried Interest
Article VII  — Management of the Partnership; Powers of the General Partner
Article VIII — LPAC; LP Consent Rights
Article IX   — Transfers of Interests
Article X    — Key Person; Cause Events; Removal of General Partner
Article XI   — Term; Dissolution; Liquidation
Article XII  — Indemnification; Exculpation; Standard of Care
Article XIII — Books, Records, Reports; Tax Matters
Article XIV  — Confidentiality
Article XV   — General Provisions

EXHIBIT A — Partners and Capital Commitments
EXHIBIT B — Waterfall / Distribution Mechanics (if complex)
EXHIBIT C — Key Persons
EXHIBIT D — Investment Guidelines / Restrictions
```

### Key Drafting Notes by Article

**Article I (Definitions):** Include at minimum: Affiliate, Business Day, Capital Account, Capital Commitment, Capital Contribution, Carried Interest, Cause, Closing, Co-Investment Vehicle, Defaulting Partner, Distribution, ERISA, Fiscal Year, Fund Expenses, General Partner, GP Commitment, GP Removal Event, Indemnified Person, Investment Period, Key Person, Key Person Event, LPAC, Limited Partner, Management Fee, Net Profits/Losses, Organizational Expenses, Partner, Percentage Interest, Portfolio Company, Preferred Return, Remaining Commitments, Subscription Agreement, Unfunded Commitment.

**Article IV (Capital Contributions):** Specify minimum capital call notice period (10–15 business days), consequences of default (interest, forfeiture of up to 50% of capital account, forced sale at discount), GP's right to cure on behalf of defaulting LP, and any subscription facility bridge provisions.

**Article VI (Waterfall):** This is the most heavily negotiated article. Draft the waterfall step-by-step with numerical precision. For a standard PE waterfall:
1. Return of contributed capital (including recycled amounts)
2. Preferred return ([8]% compounded annually)
3. GP catch-up (100% to GP until GP has received [20]% of cumulative profits)
4. Residual split ([80]% to LPs / [20]% to GP as Carried Interest)

For VC (no preferred return): simpler — return of capital, then [80/20] split.

**Article XII (Indemnification):** Ensure the exculpation standard and indemnification carve-outs mirror each other. Standard formulation:

```
The General Partner shall not be liable to the Partnership or any Partner for any
act or omission taken or suffered by it in good faith and in the reasonable belief
that such act or omission was in or not opposed to the best interests of the
Partnership, provided that such act or omission does not constitute fraud, willful
misconduct, gross negligence, or a material breach of this Agreement.
```

---

## Operating Agreement (LLC) {#operating-agreement}

Used for GP entities, management companies, and SPVs. Simpler than fund LPAs.

### GP Entity Operating Agreement — Key Sections

```
LIMITED LIABILITY COMPANY AGREEMENT
OF
[GP ENTITY NAME], LLC

Section 1  — Definitions
Section 2  — Formation; Name; Purpose; Term
Section 3  — Members; Capital Contributions; Interests
Section 4  — Management; Officers
Section 5  — Allocations and Distributions
Section 6  — Tax Matters
Section 7  — Transfer Restrictions
Section 8  — Dissolution and Winding Up
Section 9  — Indemnification; Limitation of Liability
Section 10 — General Provisions

EXHIBIT A — Members and Interests
```

**Purpose clause:** Broad enough to cover fund management activities:
```
The purpose of the Company is to serve as the general partner of [Fund Name], L.P.
and to engage in any and all activities incidental or related thereto.
```

**Carried interest allocation:** If carry flows through the GP entity to principals, the Operating Agreement must specify allocation mechanics among the members (GP principals, carry recipients). This is often the most sensitive document in the fund structure — it allocates economics among the GP team.

---

## Certificate of Limited Partnership {#certificate-lp}

Filed with the Delaware Secretary of State. Minimal required content:

```
CERTIFICATE OF LIMITED PARTNERSHIP
OF
[FUND NAME], L.P.

1. Name: [Fund Name], L.P.
2. Registered Office: [Address in Delaware]
3. Registered Agent: [Agent Name] at [Address]
4. General Partner: [GP Entity Name], LLC
   Address: [●]

IN WITNESS WHEREOF, the undersigned has executed this Certificate of Limited
Partnership as of [Date].

[GP ENTITY NAME], LLC
General Partner

By: ___________________________
Name: [●]
Title: [Managing Member]
```

Filing fee: $200 (as of last update — verify with DE Secretary of State).

---

## Certificate of Formation (LLC) {#certificate-llc}

Filed with the Delaware Secretary of State. Even more minimal:

```
CERTIFICATE OF FORMATION
OF
[ENTITY NAME], LLC

1. Name: [Entity Name], LLC
2. Registered Office: [Address in Delaware]
3. Registered Agent: [Agent Name] at [Address]

IN WITNESS WHEREOF, the undersigned has executed this Certificate of Formation
as of [Date].

By: ___________________________
Name: [●]
Title: Authorized Person
```

Filing fee: $90 (as of last update — verify with DE Secretary of State).

---

## Subscription Agreement {#subscription}

The contract between the LP and the fund. Serves three purposes: (1) LP's commitment to invest, (2) LP's representations and warranties, and (3) regulatory compliance (accredited investor / QP verification).

### Structure

```
SUBSCRIPTION AGREEMENT
[FUND NAME], L.P.

1. Subscription and Commitment
2. Representations and Warranties of the Limited Partner
   (a) Authorization and capacity
   (b) Accredited investor / Qualified purchaser status
   (c) Investment intent (not for redistribution)
   (d) Access to information / sophistication
   (e) Tax status (taxable, tax-exempt, non-US)
   (f) ERISA status
   (g) AML/KYC representations
   (h) Bad Actor representations (Rule 506(d))
   (i) Beneficial ownership
   (j) Source of funds
3. Acceptance; Power of Attorney
4. Miscellaneous

INVESTOR QUESTIONNAIRE (Exhibit A)
   — Entity type, jurisdiction, tax ID
   — Accredited investor qualification basis
   — Qualified purchaser qualification basis
   — ERISA plan asset status
   — FATCA status (W-9 or W-8 series)
   — AML/KYC documentation
   — Authorized signatories
```

---

## Side Letter {#side-letter}

Short-form agreement modifying LPA terms for a specific LP.

### Structure

```
SIDE LETTER

[Date]

[LP Name]
[Address]

Re: [Fund Name], L.P. — Side Letter

Dear [●]:

Reference is made to the Agreement of Limited Partnership of [Fund Name], L.P.
dated as of [●] (the "Partnership Agreement"). Capitalized terms used but not
defined herein have the meanings given to them in the Partnership Agreement. In
connection with your subscription to the Partnership, we hereby agree as follows:

1. [Fee Discount / MFN / Co-Invest / Reporting / Regulatory Accommodation]
2. [Additional Term]
3. [Additional Term]

Except as expressly modified hereby, the Partnership Agreement shall remain in
full force and effect. In the event of any conflict between this Side Letter and
the Partnership Agreement, this Side Letter shall control.

[Signature Blocks]
```

---

## Capital Call Notice {#capital-call}

```
NOTICE OF CAPITAL CALL

[Date]

To: The Limited Partners of [Fund Name], L.P.

Pursuant to Section [●] of the Partnership Agreement, the General Partner hereby
calls for Capital Contributions as follows:

Aggregate Amount Called:     $[●]
Your Pro Rata Share:         $[●]
Purpose:                     [Investment in [Portfolio Company] / Management Fee /
                              Fund Expenses / Follow-on Investment]
Due Date:                    [●], 20[●] [not less than 10 business days from notice]

Wire Instructions:
Bank:          [●]
ABA/SWIFT:     [●]
Account Name:  [●]
Account No.:   [●]
Reference:     [Fund Name] — Capital Call [#]

Please confirm receipt of this notice and your intended wire date.

[GP ENTITY NAME], LLC
General Partner of [Fund Name], L.P.
```

---

## Distribution Notice {#distribution-notice}

```
NOTICE OF DISTRIBUTION

[Date]

To: The Limited Partners of [Fund Name], L.P.

The General Partner is pleased to announce a distribution as follows:

Source:                      [Disposition of investment in [Portfolio Company] /
                              Dividend income / Interest income]
Aggregate Distribution:      $[●]
Your Distribution:           $[●]

Character of Distribution:
  Return of Capital:         $[●]
  Gain:                      $[●] ([long-term / short-term] capital gain)
  [Carried Interest to GP:   $[●]] [if applicable]

Distribution Date:           [●], 20[●]
Wire to:                     [LP's bank account on file]

This distribution [does / does not] include amounts attributable to Carried
Interest. The cumulative distribution status as of this distribution is:
  Total Capital Called:      $[●]
  Total Distributions:       $[●]
  DPI:                       [●]x
  TVPI:                      [●]x

[GP ENTITY NAME], LLC
General Partner of [Fund Name], L.P.
```
