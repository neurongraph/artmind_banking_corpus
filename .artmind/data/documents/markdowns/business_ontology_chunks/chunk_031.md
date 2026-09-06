### Transaction Constraints  
| Rule | Constraint |
|------|-----------|
| Amount > 0 | `transaction.amount > 0` |
| Account must exist | `transaction.account_id REFERENCES account(account_id)` |
| Immutable post-posting | `transaction.status IN (Pending, Completed) AND cannot_edit_completed` |