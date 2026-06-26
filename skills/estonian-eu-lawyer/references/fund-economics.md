# Fund Economics Reference

## Management Fee Structures

### Standard VC Fund
- **Investment period** (typically years 1-5): 2.0% of **committed capital** per annum
- **Post-investment period** (years 6-10+): 2.0% of **invested capital** (or net invested capital = invested minus returned)
- Step-down alternative: 2.0% → 1.5% after investment period
- Payment: quarterly in advance (most common) or semi-annually

### Venture Studio Fund (Higher Operating Costs)
- Studio operations (office space, mentorship, in-kind services) justify higher fees
- **Typical range**: 2.5%-3.0% of committed capital during investment period
- Alternative: 2.0% management fee + separate "studio services fee" charged to portfolio companies
- Important: clearly disclose in PPM which costs are covered by management fee vs. charged separately

### Management Fee Offsets
- **100% offset**: All transaction fees, monitoring fees, board fees, and broken deal expenses received by GP or affiliates reduce the management fee dollar-for-dollar
- **80% offset**: More GP-friendly; 80% of such fees offset the management fee
- Institutional LPs expect 100% offset; emerging managers may negotiate 80%

### Organizational Expenses
- Fund formation costs (legal, accounting, regulatory filings): typically capped and borne by the fund
- **Standard cap**: $250K-$500K for a small fund; $500K-$1M for institutional funds
- Excess over cap borne by the GP/management company
- Include: legal fees for LPA/PPM, accounting setup, AIFMD registration, initial compliance setup

### Operating Expenses (Borne by the Fund)
- Legal fees for portfolio transactions
- Audit and tax preparation
- Custodian and administrator fees
- Insurance (D&O, E&O for the fund)
- Travel related to portfolio company monitoring (some LPAs cap this)
- NOT included: GP office rent, GP employee salaries, GP overhead — these come from the management fee

## Carried Interest (Carry)

### Standard Terms
- **20% of profits** above the preferred return (hurdle rate)
- Carry is the GP's share of fund profits — the primary economic incentive
- Remaining 80% of profits distributed to LPs pro rata based on capital contributions

### Preferred Return (Hurdle Rate)
- **8% IRR** is the institutional standard (compounded annually)
- Some emerging manager funds negotiate 0% hurdle (especially for seed/pre-seed)
- Hurdle must be cleared before the GP receives any carry
- Purpose: ensures LPs receive a minimum return on their capital before the GP participates in profits

### Distribution Waterfall — European vs. American

**European Waterfall (Whole-Fund / Total Return)** — LP-friendly, institutional standard:
```
Step 1: Return of ALL contributed capital to LPs (across all investments)
Step 2: Preferred return (8% IRR) on all contributed capital to LPs
Step 3: GP catch-up — GP receives 100% of distributions until GP has
        received 20% of total profits (Steps 2 + 3 combined)
Step 4: 80/20 split — remaining profits split 80% LP / 20% GP
```
- GP receives no carry until the entire fund has returned capital + preferred return
- Protects LPs from early winners masking later losses
- **Recommended for institutional quality funds**

**American Waterfall (Deal-by-Deal)** — GP-friendly:
```
Step 1: Return of contributed capital for THAT DEAL to LPs
Step 2: Preferred return on THAT DEAL's capital to LPs
Step 3: GP catch-up on THAT DEAL
Step 4: 80/20 split on THAT DEAL's remaining profits
```
- GP receives carry on each profitable exit, even if the overall fund is underwater
- Requires stronger clawback provisions to protect LPs
- More common in real estate and some emerging manager funds
- **Risk**: GP receives carry on early winners, then fund loses money on later deals

### GP Catch-Up
- After the preferred return is paid to LPs, the GP receives 100% of the next distributions until the GP has "caught up" to its 20% share of total profits
- Example: Fund profits of $10M, 8% hurdle met
  - LP receives preferred return first
  - GP catches up: receives 100% until GP has $2M (20% of $10M)
  - Remaining distributions split 80/20
- Some LPAs use a partial catch-up (e.g., 80% to GP / 20% to LP during catch-up phase)

### Clawback Provisions

**GP Clawback** (protects LPs):
- If the GP has received more carry over the fund's life than it was entitled to (because later investments lost money), the GP must return the excess
- Triggered at fund liquidation or sometimes at specified intervals
- **Critical terms to define**:
  - Joint and several vs. several only (among individual carry recipients)
  - Gross or net of taxes paid by carry recipients
  - Escrow requirement (common: 25-30% of carry held in escrow until final liquidation)
  - Time limit for clawback claims

**LP Clawback** (protects GP):
- If LPs have received distributions that must be returned (e.g., for fund expenses, indemnification claims)
- Typically capped at the lesser of: distributions received or the LP's unfunded commitment
- Time-limited: usually 2-3 years after final distribution

### Carry Allocation Among GP Principals

Carry is allocated from the GP to individuals via:
1. **GP Operating Agreement / LLC Agreement**: Defines carry pool and allocation
2. **Venture Partner Agreements**: Allocates carry to VPs with vesting

Typical allocation framework:
| Role | Carry Allocation | Vesting |
|------|-----------------|---------|
| Managing Partner (founder) | 40-60% of carry pool | Immediate or accelerated |
| Partners | 15-25% each | 4 years, 1-year cliff |
| Full-time Venture Partners | 5-15% | 3-4 years, 1-year cliff |
| Part-time / Strategic VPs | 1-5% | 3-4 years, 1-year cliff |
| Reserve pool (future hires) | 5-15% | Allocated as needed |

### Tax Treatment of Carry

**Estonian GP (OÜ)**:
- Carry retained in the OÜ: **0% tax** (Estonia's distributed profits tax)
- Carry distributed as dividends from the OÜ: **22% CIT** (or 14% reduced rate)
- This creates a powerful deferral advantage — carry can be reinvested before tax

**US Tax (for US persons receiving carry)**:
- Long-term capital gains treatment if underlying investments held 3+ years (IRC § 1061)
- Rate: 20% + 3.8% NIIT = 23.8%
- Short-term (< 3 years): ordinary income rates (up to 37%)

**Cross-border carry**:
- Estonian GP distributing carry to US persons: Estonia-US DTT applies
- Dividend withholding: 15% (or 5% if 10%+ direct ownership)
- US persons can credit Estonian tax against US liability (foreign tax credit)
- Structure carry as partnership distributive share (not salary) to preserve capital gains treatment

## GP Commitment

### Standard Expectations
- GP commits **1-5% of fund size** from personal capital
- Demonstrates "skin in the game" and alignment with LPs
- Institutional LPs increasingly require minimum 1% GP commit
- For a $3M fund: $30K-$150K GP commitment

### Alternatives to Cash GP Commit
- **Management fee waiver**: GP waives a portion of management fees in exchange for an equivalent LP interest — common for emerging managers
- **Carry as GP commit**: Some structures allow committed carry to count (less common, less LP-friendly)
- **Combination**: Partial cash + partial fee waiver

## Recycling Provisions

### What Is Recycling
- The fund reinvests capital returned from early exits back into new investments
- Effectively increases the "investable capital" beyond the committed amount
- Standard: recycle up to **100-125% of committed capital** (i.e., reinvest up to 25% of returned capital)

### Key LPA Provisions
- **Cap on recycling**: Limit total invested amount to [X]% of commitments
- **Timing restriction**: Only during the investment period (or within 12 months after)
- **Priority**: Returned capital may only be recycled if LPs have first received return of their contributed capital and/or preferred return (depends on waterfall structure)
- **Management fee recycling**: Some LPAs allow management fees to be funded from recycled capital

### Estonian Tax Advantage
- Because the Estonian GP pays 0% tax on retained profits, recycling is particularly efficient
- No tax leakage on returns flowing through the GP before reinvestment
- Compare to US C-corp GP: recycling through a taxable entity creates immediate tax liability

## Capital Calls and Distributions

### Capital Call Mechanics
- LPs commit capital but don't fund it all at once
- GP issues **capital call notices** (typically 10-15 business days advance notice)
- Capital called as needed for investments + management fees + expenses
- Defaulting LP penalties: forfeiture of interest, forced sale at discount, loss of voting rights

### Distribution Mechanics
- In-kind distributions: Distributing securities (shares in portfolio companies) rather than cash
  - Requires LP consent in most LPAs
  - Valuation issues: use fair market value at distribution date
  - Estonian tax: distribution of in-kind assets from OÜ = deemed distribution, triggers CIT
- Timing: Within [30-60] days of liquidity event (cash distributions)
- Tax distributions: Some LPAs require mandatory distributions to cover LPs' tax liabilities

## Fund Term and Extensions

### Standard Terms
- **Fund life**: 10 years (most common for VC)
- **Investment period**: First 5 years (or until committed capital is fully invested/reserved)
- **Harvest period**: Years 6-10 (manage and exit portfolio)
- **Extensions**: Typically 2 x 1-year extensions, requiring LPAC or LP majority approval
- **Zombie fund risk**: If fund can't exit positions and keeps extending — address in LPA with forced liquidation provisions

### Early Termination
- **Key person event**: If a specified key person (usually the managing partner) is unable to devote substantially all their business time to the fund
  - Investment period suspends automatically
  - LPs vote to: (a) resume with replacement, (b) terminate investment period, or (c) wind down
- **For cause removal of GP**: Fraud, willful misconduct, gross negligence, felony conviction, bankruptcy
  - Requires supermajority LP vote (typically 75%+)
  - GP carry may be reduced or forfeited depending on LPA terms
- **No-fault removal**: Some LPAs allow LP majority to remove GP without cause
  - Less common; GP typically negotiates against this or requires supermajority

## Reporting and Valuation

### Reporting Obligations
- **Quarterly reports**: Portfolio summary, NAV, cash flow statement, investment activity
- **Annual reports**: Audited financial statements (GAAP or IFRS), tax reporting (K-1s for US LPs), AIFMD reporting (for Estonian GP)
- **Capital account statements**: Per-LP, showing contributions, distributions, NAV, IRR
- **ESG reporting**: Increasingly expected by institutional LPs

### Valuation (IPEV Guidelines)
- **International Private Equity and Venture Capital Valuation Guidelines (IPEV)** — industry standard
- Fair value hierarchy: recent transaction price → comparable companies → discounted cash flow → net assets
- Early-stage (pre-revenue): Typically valued at cost until a subsequent financing round provides a new reference price
- Markdowns: Required if there's evidence of impairment (failed milestones, down-round, loss of key customer)
- **GP conflicts**: GP is incentivized to value high (for carry and fundraising); LPAC oversight recommended for material valuations
