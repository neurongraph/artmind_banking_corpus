## Database Architecture  
### Primary Database (PostgreSQL)  
**Database:** `firstuk_prod`  
**Schemas:**
- `public.accounts` — Account records (800 records)
- `public.customers` — Customer records (500 records)
- `public.transactions` — Transaction log (2,000+ records/month)
- `public.account_holders` — Joint account holders
- `public.standing_orders` — Recurring transfers
- `public.direct_debits` — Recurring bill payments
- `public.cards` — Debit card records (800 cards)
- `public.compliance_kyc` — KYC verification records
- `public.compliance_aml` — AML screening records
- `public.products` — Product definitions (5 products)  
**Indexes:**
- Customer ID (for lookups)
- Account ID (for queries)
- Transaction date (for history)
- Account status (for reporting)  
**Backup Strategy:**
- Continuous replication to standby database
- Daily encrypted backup to AWS S3
- RPO: 15 minutes
- RTO: 2 hours