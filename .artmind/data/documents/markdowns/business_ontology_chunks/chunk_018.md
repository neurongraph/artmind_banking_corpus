### Entity: Direct Debit  
**Definition:** A recurring payment initiated by a third party (biller) authorized by the customer.  
**Attributes:**
- `direct_debit_id` — Unique identifier
- `account_id` — Account paying
- `biller_name` — Billing organization
- `biller_code` — Biller's assigned code
- `reference` — Customer's account with biller (e.g., utility account number)
- `amount_type` — Fixed, Variable, Quarterly
- `expected_amount` — Expected payment amount
- `maximum_amount` — Highest amount allowed
- `frequency` — Monthly, Quarterly, Annual
- `start_date` — First payment date
- `end_date` — Last payment date (if applicable)
- `status` — Active, Paused, Cancelled
- `mandate_reference` — Direct debit mandate ID  
**Key Business Rules:**
- Customer authorizes specific biller via DD mandate
- Biller cannot debit more than maximum amount without notice
- Customer can cancel DD up to 5 days before payment
- Failed DD can be retried (usually once)
- DD protected by Direct Debit Guarantee  
**Relationships:**
- `on_account` → Account (1:many)
- `initiated_by` → Biller (external organization, 1:many)
- `generates_transactions` → Transaction (1:many)  
---