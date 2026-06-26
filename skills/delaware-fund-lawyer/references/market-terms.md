# Market Terms Reference — Fund Formation

Detailed reference on market-standard terms for investment fund formation. Use this to advise on what's "market" and what's negotiable.

## Table of Contents

1. [Fund Economics](#economics)
2. [Governance & Control](#governance)
3. [Investment Restrictions](#investment-restrictions)
4. [LP Rights & Protections](#lp-rights)
5. [GP Protections](#gp-protections)
6. [Key Person & Cause Events](#key-person)
7. [Conflicts & Related Transactions](#conflicts)
8. [Reporting & Transparency](#reporting)
9. [Side Letter Terms](#side-letters)
10. [Emerging Manager Adjustments](#emerging-manager)

---

## Fund Economics {#economics}

### Management Fee

**Standard:** 2.0% of aggregate commitments during the investment period; steps down to 2.0% of invested capital (net of returned capital) post-investment period.

**Variations:**
- Fee holidays or discounts for first closers / anchor LPs (e.g., 1.75% or 50bp discount)
- Budget-based fees (less common; seen in some PE/RE funds)
- Flat fee amounts for smaller funds
- "1.5 and 20" structures increasingly seen for larger funds or Fund III+ managers
- Offsets: 100% offset of transaction fees, monitoring fees, and broken-deal expenses against management fee is market. 80% offset is LP-unfriendly.
- Organizational expenses above a cap (typically $300K–$500K for emerging managers, $500K–$1M for established) usually borne by GP or offset against fees

### Carried Interest

**Standard:** 20% of net profits (after return of capital and, if applicable, preferred return).

**Waterfall structures:**
- **American/Deal-by-Deal:** Carry distributed on a deal-by-deal basis, subject to loss carryforward. More GP-friendly. Common in VC.
- **European/Whole-Fund:** Carry distributed only after all capital (and preferred return if any) returned to LPs. More LP-friendly. Common in PE/buyout.
- **Hybrid:** Deal-by-deal with a whole-fund clawback — most common compromise.

**Preferred Return (Hurdle Rate):**
- PE/Buyout: 8% compounded annually is market standard
- VC: No preferred return is common (and accepted by LPs)
- Real Estate: 8–9% depending on strategy
- GP Catch-Up: Typically 80/20 (GP receives 100% of profits above hurdle until GP has 20% of total profits, then revert to 80/20 split). Some funds use 50% catch-up — less GP-friendly.

**Section 1061 (Tax):** Since 2017 tax reform, carried interest held less than 3 years taxed at ordinary income rates. Fund LPAs should be drafted with 3-year holding period mechanics in mind.

### GP Commitment

**Standard:** 1–5% of fund size, with 2–3% most common for established managers.

**Source matters:** LPs prefer the GP commitment funded with cash (not management fee waivers). Fee waiver-funded GP commitments reduce economic alignment.

**Emerging managers:** 1% is generally accepted if manager is investing personal capital. LPs understand founders may be capital-constrained.

### Clawback

**Standard:** GP must return excess carried interest at fund liquidation if aggregate distributions exceed what GP was entitled to on a whole-fund basis.

**Key negotiation points:**
- Net of taxes: GP typically reduces clawback obligation by taxes paid on distributed carry (effective tax rate assumed, e.g., 45%)
- Escrow: LPs may require 20–30% of carry escrowed to secure clawback. Less common for VC.
- Several (not joint): Each GP principal's clawback is limited to carry they received — not cross-liable for others' carry
- LP clawback: LPs may be required to return distributions to fund partnership obligations (capped at lesser of distributions received or their commitment). Usually 2–3 year sunset post-fund termination.

---

## Governance & Control {#governance}

### GP Authority

Standard: GP has exclusive authority to manage the fund's business and affairs. LP consent required only for specified "Major Decisions."

**Major Decisions (typical LP consent items):**
- Amendments to LPA that adversely affect LPs
- Extension of fund term beyond permitted extensions
- Removal of GP
- Fund-level borrowing above threshold
- Change of fund investment strategy
- Admission of new LPs after final close (sometimes)

### Voting Thresholds

| Action | Typical Threshold | Notes |
|--------|-------------------|-------|
| LPA amendments (material) | Majority or 66.7% of LP interests | GP should not be able to unilaterally amend economic terms |
| GP removal for cause | Majority of LP interests | "Cause" defined events (fraud, felony, bankruptcy, key person breach) |
| GP removal without cause | 66.7–80% of LP interests | Highly negotiated; GPs resist low thresholds |
| Fund term extension | LPAC consent or majority LP consent | Usually GP can extend 1–2 years; further extensions need LP approval |
| Early termination of investment period | 66.7–75% of LP interests | "No-fault divorce" — sensitive for GPs |
| Dissolution | 75–80% of LP interests | Rarely exercised |

### LPAC (Limited Partner Advisory Committee)

**Composition:** 3–7 LP representatives, typically largest LPs. GP-selected with LP input. Non-fiduciary capacity (explicitly stated in LPA).

**Role:**
- Review and approve conflict transactions
- Consent to valuation methodologies
- Consent to LP transfers
- Approve fund term extensions
- Advise on GP removal situations
- Review portfolio company co-investment allocations

**Key drafting point:** LPAC members must be expressly released from fiduciary duties to other LPs. They serve in a non-fiduciary, consultative capacity only.

---

## Investment Restrictions {#investment-restrictions}

### Concentration Limits

**Standard:**
- No more than 15–25% of aggregate commitments in a single portfolio company
- No more than 20–25% in a single industry sector (less common; more typical in PE than VC)

**VC exception:** VC funds often have wider concentration limits (25–30%) or follow-on investment carve-outs that effectively allow higher concentration in winners.

### Recycling

**Standard:** GP can reinvest proceeds from portfolio dispositions during the investment period, typically capped at 15–25% of aggregate commitments.

**Purpose:** Allows GP to maintain fully invested fund without overcalling capital. Avoids "cash drag" from early exits.

### Borrowing / Credit Facilities

**Standard:** Subscription credit facilities (bridge borrowing against uncalled commitments) are market. LPA should specify:
- Maximum outstanding (typically 20–25% of unfunded commitments)
- Maximum duration (90–180 days for subscription lines; longer for NAV facilities)
- Whether interest on borrowing is a fund expense or management company expense

**NAV facilities:** Borrowing against portfolio asset values is increasingly common but more controversial. LPA should clearly authorize if intended.

---

## LP Rights & Protections {#lp-rights}

### Transfer Restrictions

**Standard:** LP interests generally non-transferable without GP consent (not to be unreasonably withheld). Typical exceptions:
- Transfers to affiliates
- Transfers to other existing LPs
- Transfers by operation of law

**GP veto rationale:** GP needs to control the investor base for regulatory (Reg D, "bad actor") and tax (ERISA, tax-exempt) compliance.

### Excuse / Exclusion Rights

**Standard:** LPs may be excused from investments that would violate their legal, regulatory, or internal policy constraints (e.g., government pension funds with ESG mandates, insurance company investment limitations).

**Mechanics:** LP must notify GP in writing. GP determines whether excuse applies. Excused LP's commitment reallocated pro rata to other LPs (or funded by GP).

### Information Rights

**Standard:**
- Annual audited financial statements (within 120 days of fiscal year end)
- Quarterly unaudited reports with portfolio summary
- Tax K-1s (target March 15; many funds miss this)
- Capital account statements
- Annual meeting or investor update

**Enhanced (negotiated via side letter):**
- Monthly or quarterly NAV estimates
- Portfolio company detail (revenue, EBITDA if available)
- ESG/DEI reporting
- Co-investment pipeline updates
- GP team composition changes

---

## GP Protections {#gp-protections}

### Indemnification

**Standard:** Fund indemnifies GP, its affiliates, and their directors/officers/employees against claims arising from fund activities, EXCEPT for:
- Fraud
- Willful misconduct
- Gross negligence
- Material breach of the LPA
- Bad faith

**Advancement:** GP typically entitled to advancement of legal expenses, subject to repayment if ultimately found liable.

**Indemnification cap:** Some LP-friendly LPAs cap indemnification at fund NAV or GP's carried interest. Increasingly negotiated.

### Exculpation

**Standard:** GP not liable to fund or LPs for acts or omissions EXCEPT for fraud, willful misconduct, gross negligence, material breach, or bad faith.

**Drafting note:** The exculpation standard and the indemnification carve-outs should match. Inconsistencies between the two create ambiguity and litigation risk.

---

## Key Person & Cause Events {#key-person}

### Key Person Provision

**Trigger:** Named key persons (typically 1–3 senior professionals) cease to devote "substantially all" of their business time to the fund.

**Consequence:** Investment period is automatically suspended. GP must notify LPs within [30] days.

**Cure:** Key person event can be cured by:
- Return of the key person
- LPAC or majority LP approval of a replacement
- Majority LP vote to resume investment period

**Best practice:** Define "substantially all business time" — market is 75–85% of professional time. Permit reasonable time for personal investments, board service, and teaching.

### Cause Events (GP Removal for Cause)

**Standard cause events:**
- Fraud, willful misconduct, or gross negligence by GP
- Felony conviction of GP or key person
- Bankruptcy of GP
- Material breach of LPA that is not cured within [60] days of notice
- Key person event not cured within [180] days

---

## Conflicts & Related Transactions {#conflicts}

### Conflicts Policy

**Market approach:** GP discloses conflicts to LPAC. LPAC reviews and provides consent (or not) on a transaction-specific basis. LPAC consent creates safe harbor for GP.

**Common conflict areas:**
- Co-investments allocated to GP principals, affiliates, or other funds
- Broken-deal expenses allocated across multiple funds
- Principal transactions (GP buying from / selling to the fund)
- Cross-fund investments
- GP-affiliated service providers (portfolio consulting, placement agents)
- Allocation of investment opportunities across funds with overlapping mandates

### Co-Investment

**Standard:** GP offers co-investment opportunities to LPs on a no-fee, no-carry basis (or reduced fee/carry). Allocation at GP discretion, though LPs increasingly negotiating pro-rata or priority co-invest rights via side letters.

**Drafting tip:** Specify whether co-investors bear their share of broken-deal expenses. Market is trending toward co-investors sharing deal costs.

---

## Reporting & Transparency {#reporting}

### Financial Reporting

| Report | Frequency | Deadline | Notes |
|--------|-----------|----------|-------|
| Audited financials | Annual | 120 days post-FYE | Big 4 or reputable mid-tier auditor expected by institutional LPs |
| Unaudited financials | Quarterly | 60 days post-quarter | Portfolio summary, capital account, cash flow |
| K-1 tax schedules | Annual | Target March 15 | Many funds deliver late; side letter LPs negotiate hard deadlines |
| Capital call notices | Per event | 10–15 business days before due date | Must specify amount, purpose, due date, wire instructions |
| Distribution notices | Per event | With or shortly before distribution | Must specify amount, source (return of capital vs. gain), tax character |

### Valuation

**Standard:** Quarterly fair value per ASC 820 (GAAP). Valued by GP, reviewed by auditor annually. LPs increasingly requesting independent third-party valuations, especially for PE and credit funds.

**LPAC role:** LPAC may review and advise on valuation methodologies. LPAC does not independently value — that remains GP's responsibility.

---

## Side Letter Terms {#side-letters}

### Common Side Letter Provisions

Side letters are agreements between the fund/GP and a specific LP granting rights beyond the LPA. Common provisions:

- **Fee discounts:** Reduced management fee and/or carry for anchor or large LPs
- **MFN (Most Favored Nation):** LP gets the benefit of any more favorable term granted to another LP (subject to carve-outs for size-based and regulatory-based provisions)
- **Co-investment rights:** Priority or pro-rata access to co-investments
- **ERISA:** Representations limiting fund's ERISA plan asset exposure to <25%
- **Regulatory compliance:** Tailored provisions for government pension funds, insurance companies, banks (e.g., Volcker Rule, BHC Act)
- **Reporting:** Enhanced reporting obligations (more frequent, more detailed)
- **Transfer rights:** Pre-negotiated consent to transfers to specified affiliates
- **Excuse rights:** Right to be excused from specific investment types
- **Sovereign immunity:** Preservation of sovereign immunity for governmental LPs
- **FOIA/Public records:** Protections around confidentiality for governmental LPs subject to freedom of information requests

### MFN Process

**Standard mechanics:**
1. GP compiles MFN-eligible side letter provisions after final close
2. GP sends MFN election notice to eligible LPs (typically 30 days to elect)
3. LPs elect which provisions they want to receive
4. GP confirms elected provisions

**Carve-outs from MFN:** Size-based fee discounts, co-investment rights tied to commitment size, regulatory accommodations specific to LP type.

---

## Emerging Manager Adjustments {#emerging-manager}

First-time or early-fund managers often face different market dynamics:

### What LPs Accept

- Smaller fund size (institutional LPs have minimums; emerging managers work with family offices, HNWIs, fund-of-funds)
- GP commitment at 1% (vs. 2–3% for established managers)
- Less track record data — LPs focus on attribution and sourcing ability
- Simpler fund structure (single LP, no parallel funds, no offshore feeder)

### What LPs Scrutinize More

- Key person provisions (fund depends on 1–2 people)
- Conflict provisions (less institutional infrastructure to manage conflicts)
- Succession planning
- Operational infrastructure (back-office, compliance, fund admin)
- Budget-based management fee to ensure fees cover reasonable expenses

### Cost-Effective Structuring

- **Minimum viable structure:** Delaware LP (fund) + Delaware LLC (GP) + management company (may be same as GP for small funds)
- **Skip the offshore feeder** unless you have committed non-US or tax-exempt capital that requires it
- **Use a fund administrator** from day one — even for small funds. The cost ($30K–$75K/year) is worth the institutional credibility and LP confidence
- **Organizational expense cap:** Keep it reasonable ($250K–$500K). LPs understand formation costs but will question excessive org expenses for a small fund
