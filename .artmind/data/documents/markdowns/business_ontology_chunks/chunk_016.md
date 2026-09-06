## 4. Transaction Domain  
### Entity: Transaction  
**Definition:** A financial event representing money movement or activity on an account.  
**Attributes:**
- `transaction_id` — Unique identifier
- `account_id` — Linked account
- `transaction_type` — Deposit, Withdrawal, Transfer, Interest, Fee, Correction
- `amount` — Transaction amount (in pence for precision)
- `currency` — Currency (GBP)
- `transaction_date` — Date transaction occurred
- `settlement_date` — Date settlement completed
- `description` — Transaction description
- `status` — Pending, Completed, Failed, Reversed
- `reference` — Customer-visible reference  
**Transaction Types:**  
| Type | Direction | Trigger | Example |
|------|-----------|---------|---------|
| Deposit | Credit | Customer adds funds | Branch deposit |
| Withdrawal | Debit | Customer removes funds | ATM withdrawal |
| Transfer | Debit (sender) | Money moved to another account | FPS transfer out |
| Inbound Transfer | Credit | Money received | FPS transfer in |
| Interest | Credit | Interest accrual | Monthly interest |
| Fee | Debit | Service charge | Card replacement fee |
| Standing Order | Debit | Recurring transfer | Mortgage payment |
| Direct Debit | Debit | Bill payment | Utility payment |  
**Key Business Rules:**
- Transaction cannot be deleted (audit trail)
- Account balance = sum of all transactions
- Each transaction linked to fraud risk score
- All transactions logged for compliance  
**Relationships:**
- `on_account` → Account (1:many)
- `from_account` → Account (transfer source, optional)
- `to_account` → Account (transfer destination, optional)
- `initiated_by` → Customer (1:1, optional)
- `flagged_by_fraud_detection` → FraudAlert (1:many, optional)  
**Example:**
```
Transaction: TXN-0000542
- account_id: ACC-00001
- transaction_type: Inbound Transfer
- amount: 150000 (£1,500.00 in pence)
- transaction_date: 2026-01-15
- settlement_date: 2026-01-15
- description: "Salary deposit"
- status: Completed
- reference: "SAL-JAN-2026"
```  
---