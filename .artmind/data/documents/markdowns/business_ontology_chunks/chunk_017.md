### Entity: Standing Order  
**Definition:** A recurring transfer initiated by the account holder.  
**Attributes:**
- `standing_order_id` — Unique identifier
- `account_id` — Account initiating transfer
- `beneficiary_account_id` — Recipient account (if internal)
- `beneficiary_name` — Recipient name
- `beneficiary_account_number` — Recipient account number (external)
- `beneficiary_sort_code` — Recipient bank sort code (external)
- `amount` — Transfer amount
- `frequency` — Weekly, Monthly, Quarterly, Annual
- `start_date` — First transfer date
- `end_date` — Last transfer date (if applicable)
- `status` — Active, Paused, Completed, Cancelled
- `reference` — Payment reference (e.g., "Mortgage-Jan")  
**Key Business Rules:**
- Standing order creates automatic transaction each period
- Amount and frequency cannot change (must cancel and create new)
- Standing order survives account holder changes (if joint)
- 30-day notice for cancellation (except fraud/closure)  
**Relationships:**
- `on_account` → Account (1:many)
- `generates_transactions` → Transaction (1:many)  
---