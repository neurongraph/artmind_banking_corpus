### Entity: Customer  
**Definition:** A natural person (individual) who holds at least one account with FirstUK Bank.  
**Attributes:**
- `customer_id` — Unique identifier (linked to Party)
- `first_name` — Given name
- `last_name` — Family name
- `date_of_birth` — DoB (required for AML)
- `nationality` — Country of citizenship
- `email` — Email address
- `phone` — Primary phone number
- `address` — Registered address (see Address concept)
- `customer_status` — Active, Dormant, Closed, Suspended  
**Key Business Rules:**
- Every customer must have a valid identity (see KYC concept)
- Every customer must pass AML screening before account opening
- Customer can hold multiple accounts
- Customer can have joint account holders  
**Relationships:**
- `has_accounts` → Account (1:many)
- `has_address` → Address (1:many)
- `has_kyc_verification` → KYC_Verification (1:many)  
**Example:**
```
Customer: Sarah Johnson
- customer_id: CUST-00001
- date_of_birth: 1985-03-15
- nationality: UK
- email: sarah.johnson@email.com
- customer_status: Active
- has_accounts: [ACC-00001, ACC-00002]
```  
---