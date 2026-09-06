### Entity: Account Holder  
**Definition:** A person with legal rights and responsibilities for an account.  
**Attributes:**
- `holder_id` — Unique identifier
- `account_id` — Linked account
- `customer_id` — Linked customer
- `holder_type` — Primary, Joint, Secondary
- `signatory_required` — Whether signature required for withdrawals
- `added_date` — Date holder added to account  
**Key Business Rules:**
- Account must have at least one primary holder
- Joint account: Both holders must pass KYC/AML
- Either joint holder can withdraw full balance
- Interest calculated on total balance (not per holder)  
**Example:**
```
Joint Account ACC-00002:
- Primary Holder: John Smith (customer_id: CUST-00002)
- Joint Holder: Jane Smith (customer_id: CUST-00003)
- Either can withdraw, both liable for overdraft
```  
---