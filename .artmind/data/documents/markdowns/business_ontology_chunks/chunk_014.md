### Entity: Joint Account  
**Definition:** An account held by two or more customers with joint and several liability.  
**Attributes:**
- `account_id` — Base account ID
- `joint_type` — Joint and Several, Tenants in Common
- `holders` → AccountHolder (2+ records)
- `interest_split` — How interest allocated (equal, specified %)  
**Key Business Rules:**
- Both holders must consent to account closure
- Both holders responsible for overdraft
- Both holders can initiate transactions
- Dispute resolution per [[departments]] Complaint Handling  
**Regulatory Treatment:**
- Both holders jointly and severally liable
- Both included in AML due diligence
- Both entitled to account information  
---