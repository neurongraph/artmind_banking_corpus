## 5. Risk & Compliance Domain  
### Entity: KYC Verification  
**Definition:** Know Your Customer verification confirming customer identity and legitimacy.  
**Attributes:**
- `kyc_id` — Unique identifier
- `customer_id` — Linked customer
- `verification_date` — Date of verification
- `verification_method` — Document, Biometric, Database
- `identity_verified` — Boolean (confirmed identity)
- `address_verified` — Boolean (confirmed address)
- `pep_screened` — Boolean (checked for Politically Exposed Persons)
- `adverse_media_checked` — Boolean (checked for negative news)
- `verification_status` — Verified, Incomplete, Rejected, Expired
- `next_review_date` — Date for KYC refresh (typically 3-5 years)
- `reviewer` — Staff member who performed KYC  
**Key Business Rules:**
- KYC mandatory before account opening
- KYC refreshed periodically (every 3–5 years)
- High-risk customers require Enhanced Due Diligence (EDD)
- KYC documents retained for 6 years post-closure  
**Relationships:**
- `for_customer` → Customer (1:1)
- `verified_documents` → IdentificationDocument (1:many)  
---