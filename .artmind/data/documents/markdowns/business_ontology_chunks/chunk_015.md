### Entity: Card  
**Definition:** A payment card (debit, credit, or prepaid) linked to an account.  
**Attributes:**
- `card_id` — Unique identifier
- `account_id` — Linked account
- `customer_id` — Cardholder
- `card_type` — Debit, Credit, Prepaid
- `card_number` — 16-digit card number (masked in logs)
- `cardholder_name` — Name on card
- `expiry_date` — Card expiration (MMYY format)
- `cvv` — Security code (not stored after verification)
- `card_status` — Active, Inactive, Lost, Stolen, Expired, Blocked
- `issued_date` — Date card issued
- `daily_limit` — Daily transaction limit (e.g., £500 for ATM)  
**Key Business Rules:**
- Card can be locked/unlocked by cardholder
- Lost/stolen cards can be replaced (fee £15)
- Only one card per account (initially)
- Contactless limit: £100 per transaction  
**Relationships:**
- `linked_to_account` → Account (1:many)
- `has_transactions` → Transaction (1:many)  
---