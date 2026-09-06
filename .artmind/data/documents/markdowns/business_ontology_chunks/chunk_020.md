### Entity: AML Screening  
**Definition:** Anti-Money Laundering screening to detect financial crime risks.  
**Attributes:**
- `screening_id` — Unique identifier
- `customer_id` — Customer being screened
- `screening_date` — Date screening performed
- `screening_lists` — Which lists searched (e.g., OFAC, INTERPOL, HMT)
- `matches_found` — Number of potential matches
- `match_details` — List of matches (name, score, list name)
- `risk_level` — Low, Medium, High
- `manual_review_required` — Boolean (escalation needed)
- `screening_status` — Passed, Flagged, Escalated
- `reviewer` — Staff member who reviewed  
**Screening Lists Checked:**
- OFAC Sanctions List (US Treasury)
- UN Sanctions List
- EU Sanctions List
- HM Treasury Sanctions Designations
- INTERPOL Red Notices
- PEP (Politically Exposed Persons) databases
- Adverse media databases  
**Key Business Rules:**
- AML screening mandatory at account opening
- Ongoing AML monitoring for high-risk customers
- Hit on sanctions list = automatic account freeze + SAR filing
- Failed screening = account application rejected  
**Relationships:**
- `for_customer` → Customer (1:1)
- `triggers_suspicious_activity_report` → SAR (0:many)  
---