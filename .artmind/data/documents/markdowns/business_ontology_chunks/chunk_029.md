## Constraints & Business Rules  
### Account Constraints  
| Rule | Constraint |
|------|-----------|
| Account must have product | `account.product_id NOT NULL` |
| Account balance = transaction sum | `account.balance = SUM(transactions)` |
| Dormant > 12 months inactive | `account_status = 'Dormant' IF no_activity > 365 days` |
| Account status unique | `account.status IN (Active, Dormant, Closed, Suspended)` |