# IP & Technology Law Reference

## Estonian IP Framework

### Copyright (Author's Rights Act — *Autoriõiguse seadus*)
- Automatic protection — no registration required
- Duration: Author's life + 70 years
- **Economic rights**: reproduction, distribution, communication to public, making available, adaptation — transferable
- **Moral rights**: attribution, integrity, disclosure — non-transferable under Estonian law
- **Employee works**: Economic rights vest in employer by default for works created in course of duties (§ 32)
- **Commissioned works**: Rights vest in commissioner only if expressly agreed in contract

### Software Protection
- EU Software Directive (2009/24/EC) implemented in Estonian law
- Software protected as a literary work under copyright
- Employee-created software: employer owns economic rights by default
- Decompilation: permitted only for interoperability (narrow exception)
- SaaS/platform: copyright protects the code, not the functionality or business logic
- Database rights: sui generis protection for substantial investment in data collection/verification

### Patents (Patents Act — *Patendiseadus*)
- Registration-based protection via Estonian Patent Office or European Patent Office (EPO)
- Duration: 20 years from filing date
- **Service inventions**: Employer can claim ownership within 4 months; must compensate employee
- Software patents: Generally not patentable in Europe as such, but software with a "technical effect" may be patentable
- Utility model (*kasulik mudel*): Simpler, faster, cheaper alternative for less complex inventions; 4-year initial term, extendable to 10 years

### Trademarks (Trademarks Act — *Kaubamärgiseadus*)
- Registration via Estonian Patent Office or EUIPO (EU Trademark)
- Duration: 10 years, renewable indefinitely
- EU Trademark (EUTM): Single registration covers all EU Member States
- Madrid Protocol: International registration covering 130+ countries
- For cross-border tech partnerships: register brand in all operating jurisdictions

### Trade Secrets
- EU Trade Secrets Directive (2016/943) implemented via Competition Act amendments
- Three conditions: (1) not generally known, (2) commercial value because secret, (3) subject to reasonable steps to maintain secrecy
- No registration — protection depends on maintaining secrecy
- Remedies: injunctions, damages, seizure
- NDA enforcement: Estonian courts enforce NDAs but the information must genuinely qualify as a trade secret

## IP in Technology Agreements

### IP Assignment Clauses
When a party creates IP under a technology/partnership agreement:

**Full Assignment (Developer to Client)**:
```
Developer hereby irrevocably assigns to Client all right, title, and
interest in and to all Intellectual Property created, developed, or
conceived by Developer in the performance of this Agreement ("Work
Product"), including all copyright, patent rights, trade secret rights,
and other intellectual property rights therein. Developer shall execute
all documents and take all actions reasonably necessary to perfect
Client's ownership.
```

**License-Back (Client assigns but Developer retains platform)**:
```
All Intellectual Property in the Platform, including all modifications,
enhancements, and derivative works, shall remain the exclusive property
of Developer. Client is granted a non-exclusive, non-transferable,
revocable license to use the Platform solely for the purposes described
in this Agreement during the Term.
```

**Carve-Out for Pre-Existing IP**:
```
Nothing in this Agreement shall transfer ownership of either Party's
Pre-Existing IP. "Pre-Existing IP" means any Intellectual Property
owned by or licensed to a Party prior to the Effective Date, or
developed independently of this Agreement. Each Party grants the other
a limited license to use its Pre-Existing IP solely to the extent
necessary to perform obligations under this Agreement.
```

### Open Source Considerations
- If platform/software incorporates open source components:
  - Identify all open source licenses (GPL, LGPL, MIT, Apache, BSD)
  - GPL "copyleft" risk: linking GPL code may require disclosing derivative source code
  - Include representation that deliverables don't contain "viral" open source unless disclosed
  - Maintain open source component inventory

### SaaS / Platform Agreements — Key IP Provisions
1. **Platform ownership**: Provider retains all IP in the platform
2. **Customer data**: Customer owns all data uploaded/generated; Provider has limited processing license
3. **Customizations**: Clarify ownership (often contentious — who owns custom features built for one client?)
4. **Usage data / analytics**: Provider typically retains rights to aggregated, anonymized usage data
5. **Feedback**: Customer grants Provider a perpetual license to incorporate feedback/suggestions
6. **No reverse engineering**: Customer prohibited from decompiling, reverse engineering, or creating derivative works

## Data Processing Agreements (DPA)

### When Required
- GDPR Art. 28: Required whenever a controller engages a processor
- In most tech partnerships, one party processes personal data on behalf of the other

### Structure
1. **Scope**: What data, whose data, what processing, how long
2. **Controller obligations**: Provide lawful instructions, ensure legal basis exists
3. **Processor obligations**: Process only on documented instructions, ensure personnel confidentiality, implement appropriate security (Art. 32), assist with DSARs, delete/return data on termination, allow audits
4. **Sub-processors**: List approved sub-processors; notification and objection mechanism for new ones
5. **International transfers**: Safeguards for transfers outside EEA (SCCs, adequacy decisions)
6. **Breach notification**: Processor notifies controller "without undue delay" (ideally within 24-48 hours)
7. **Liability and indemnification**: Processor indemnifies controller for processor's GDPR breaches

### Technical and Organizational Measures (TOMs)
DPA should specify or reference:
- Encryption (at rest and in transit)
- Access controls (role-based, MFA)
- Pseudonymization where feasible
- Regular security testing
- Incident response procedures
- Business continuity and disaster recovery
- Employee training

## Technology Licensing Models

### White Label / OEM
- Provider develops; Customer brands and distributes
- Provider retains all platform IP
- Customer gets limited license to brand and distribute
- Critical clauses: territory, exclusivity, SLA, customization rights, customer data ownership
- Revenue model: per-transaction fee, subscription, or revenue share

### API/Integration License
- Provider grants access to APIs for integration
- License scope: internal use only vs. sublicensable
- Rate limits, SLA, uptime guarantees
- Data handling: who processes what through the API
- Termination: migration period for dependent integrations

### Joint Development
- Parties collaborate to create new IP
- Critical to define: who owns what, how decisions are made, who can commercialize independently
- Options: joint ownership (complex), assignment to one party with license-back, assignment based on contribution
- **Estonian law note**: Joint ownership of IP = each owner can exploit independently but cannot grant exclusive licenses without other owner's consent

## Domain Names and Digital Assets
- .ee domains: administered by Estonian Internet Foundation (EIF)
- UDRP (Uniform Domain-Name Dispute-Resolution Policy) for .com/.net/.org disputes
- .ee dispute resolution: separate EIF procedure
- In agreements, specify who registers/owns domains and social media accounts; include transfer obligations on termination
