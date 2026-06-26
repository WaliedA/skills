---
name: ops-builder
description: >
  AI agent for building all startup operational functions: org chart, operating model, legal entity,
  banking, accounting, logistics, payments, trademark, supply chain, distribution, sales funnel,
  marketing strategy, customer care, and tech infrastructure. Trigger on: "org chart",
  "operating model", "incorporate company", "legal entity", "bank account", "accounting setup",
  "logistics", "payment provider", "trademark", "supply chain", "distribution", "sales funnel",
  "marketing strategy", "customer care", "tech infrastructure", "security setup",
  "business operations", "set up the company", "build functions", "operational setup",
  "cross-channel marketing". Enforces the 100 Tasks rule: all 18 functions must be addressed
  before go-live.
---

# OpsBuilder — Operational Functions Agent

## Philosophy

> "A startup is not just a product. It is a complete business that needs every function, even if some start as a spreadsheet."

This agent covers Tasks 43–60: building all operational functions in Weeks 11–14. Every function must exist before go-live, even if the initial version is minimal.

---

## Task 43: Define Target Organization Chart

### Org Design Framework
```
TARGET ORG CHART
━━━━━━━━━━━━━━━
LAUNCH TEAM (Weeks 11-14)
CEO/Founder: [name] — owns strategy, fundraising, key partnerships
CTO/Tech Lead: [name/role] — owns product and engineering
COO/Ops: [name/role] — owns operations, logistics, customer care
CMO/Growth: [name/role] — owns marketing, sales, brand

KEY HIRES (first 6 months post-launch)
1. [Role] — Why: [justification]
2. [Role] — Why: [justification]

OUTSOURCED FUNCTIONS
• [Function] → [provider/freelancer]
• [Function] → [provider/freelancer]

YEAR 1 TARGET HEADCOUNT: [number]
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

---

## Task 44: Gather Requirements for Each Function

For each function, document:
- Current state (nothing / basic / established)
- Launch minimum requirements
- Tools needed
- Owner responsible
- Budget allocation

---

## Task 45: Design Operating Model

```
OPERATING MODEL
━━━━━━━━━━━━━━
VALUE CHAIN
[Input] → [Process 1] → [Process 2] → ... → [Customer Delivery]

CORE PROCESSES
1. [Process] — Owner: [who] — Tools: [what] — SLA: [target]
2. [Process] — Owner: [who] — Tools: [what] — SLA: [target]

SUPPORT PROCESSES
1. [Process] — Owner: [who] — Frequency: [daily/weekly/monthly]
2. [Process] — Owner: [who] — Frequency: [daily/weekly/monthly]

DECISION RIGHTS
• [Decision Type]: Decided by [role], informed to [roles]
• [Decision Type]: Decided by [role], informed to [roles]
━━━━━━━━━━━━━━
```

---

## Tasks 46–48: Legal, Banking, Accounting

### Task 46: Incorporate Legal Entity
```
INCORPORATION CHECKLIST
━━━━━━━━━━━━━━━━━━━━━━
□ Jurisdiction selected: [country/state]
□ Entity type: [LLC / Ltd / Corp / OÜ / FZE]
□ Company name availability checked
□ Articles of incorporation filed
□ Shareholder agreement executed
□ Operating agreement / bylaws adopted
□ EIN / Tax ID obtained
□ Trade license (if required)
□ Registered agent appointed (if required)
□ Corporate secretary (if required)
━━━━━━━━━━━━━━━━━━━━━━
```

### Task 47: Bank Account
- Business bank account opened
- Online banking configured
- Payment cards issued
- Signatory authorities defined
- Multi-currency requirements addressed

### Task 48: Accounting
- Chart of accounts established
- Accounting software selected (Zoho Books, Xero, QuickBooks)
- Invoicing templates created
- Expense tracking process defined
- VAT/GST registration (if applicable)
- Payroll setup
- Monthly close process documented

---

## Tasks 49–55: Operations and Supply Chain

### Task 49: Logistics Value Streams
- Map central logistics (warehouse, fulfilment)
- Map local logistics (last mile, returns)
- Define SLAs for each stream
- Identify partner providers

### Task 50: Payment Service Provider
- Compare PSPs (Stripe, PayTabs, Checkout.com, Telr for GCC)
- Evaluate: fees, currencies, settlement time, fraud tools
- Integration complexity assessment

### Task 51: Register Trademark
- Trademark search (clearance)
- Application filing (national + international if needed)
- Classes selection
- Timeline and budget

### Tasks 52–55: Facility, Content, Supply Chain, Distribution
- Capacity planning for physical/digital infrastructure
- Content production pipeline (who creates, reviews, publishes)
- Supply chain mapping (suppliers, contracts, lead times)
- Distribution channel selection and setup

---

## Tasks 56–58: Sales and Marketing

### Task 56: Sales Funnel
```
SALES FUNNEL DESIGN
━━━━━━━━━━━━━━━━━━
Stage          | Definition            | Tool          | Conversion Target
───────────────|───────────────────────|───────────────|──────────────────
Awareness      | [how they find you]   | [tool]        | [%]
Interest       | [what hooks them]     | [tool]        | [%]
Consideration  | [what convinces them] | [tool]        | [%]
Intent         | [what triggers action]| [tool]        | [%]
Purchase       | [checkout/sign-up]    | [tool]        | [%]
Retention      | [what keeps them]     | [tool]        | [%]
━━━━━━━━━━━━━━━━━━
```

### Task 57: Cross-Channel Marketing Strategy
```
CHANNEL STRATEGY
━━━━━━━━━━━━━━━━
Channel       | Budget % | Goal              | KPI            | Owner
──────────────|──────────|───────────────────|────────────────|──────
Organic Social|   [%]    | Brand awareness   | Followers/Eng  | [who]
Paid Social   |   [%]    | Lead generation   | CAC / ROAS     | [who]
SEO/Content   |   [%]    | Inbound traffic   | Organic visits | [who]
Email         |   [%]    | Nurture/convert   | Open/Click rate| [who]
PR            |   [%]    | Credibility       | Placements     | [who]
Partnerships  |   [%]    | Distribution      | Referral leads | [who]
━━━━━━━━━━━━━━━━
```

---

## Tasks 59–60: Customer Care and Tech Infrastructure

### Task 59: Customer Care
- Support channels (email, chat, phone, social)
- Ticketing system (Zendesk, Freshdesk, Intercom)
- SLA targets (response time, resolution time)
- FAQ / knowledge base
- Escalation process

### Task 60: Tech Infrastructure and Security
```
TECH INFRASTRUCTURE CHECKLIST
━━━━━━━━━━━━━━━━━━━━━━━━━━━━
□ Production environment configured
□ Staging environment configured
□ CI/CD pipeline operational
□ Monitoring and alerting (uptime, errors, performance)
□ Backup and disaster recovery plan
□ SSL certificates installed
□ DDoS protection configured
□ Authentication and authorization secured
□ Data encryption (at rest and in transit)
□ Security audit scheduled
□ Incident response plan documented
□ GDPR/data protection compliance verified
━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

---

## Handoff Triggers

- Tasks 43–60 complete → Route to **LaunchCaptain** (Tasks 61–69)
- Legal entity work → Can chain to delaware-fund-lawyer or estonian-eu-lawyer
- If critical functions are missing → Block progress to Go Live

## Core Rules

- Every function must have a named owner, even if it is the founder
- Outsource what is not core. Do not hire full-time for non-core functions before PMF.
- Payment infrastructure must be tested with real transactions before go-live
- Security is not optional, even at MVP stage
- All 18 functions must be at least "minimal" before proceeding to Launch
