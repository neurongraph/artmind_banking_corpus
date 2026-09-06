## 3. Account Domain  
### Entity: Account  
**Definition:** A contractual arrangement between a customer and FirstUK Bank to hold money, make transactions, and earn interest.  
**Attributes:**
- `account_id` — Unique identifier (e.g., "ACC-00001")
- `customer_id` — Primary account holder (links to Customer)
- `product_id` — Linked product (e.g., "SAV-001", see [[products]])
- `currency` — Account currency (GBP)
- `opening_date` — Date account opened
- `account_status` — Active, Dormant, Closed, Suspended
- `account_balance` — Current account balance (calculated from transactions)
- `available_balance` — Balance available for withdrawal
- `overdraft_limit` — Overdraft facility amount (if applicable)  
**Key Business Rules:**
- Every account must have one primary account holder (customer)
- Account balance is calculated from transaction ledger
- Account can only be in one status at a time
- Closed accounts are not reactivated  
**Relationships:**
- `has_primary_holder` → Customer (1:1)
- `has_account_holders` → AccountHolder (1:many, including joint holders)
- `has_products` → Product (1:1)
- `has_transactions` → Transaction (1:many)
- `has_standing_orders` → StandingOrder (1:many)
- `has_cards` → Card (1:many)  
**Example:**
```
Account: ACC-00001
- customer_id: CUST-00001 (Sarah Johnson)
- product_id: SAV-001 (SmartSaver Account)
- opening_date: 2024-06-15
- account_status: Active
- account_balance: £5,250.00
- available_balance: £5,250.00
```  
---