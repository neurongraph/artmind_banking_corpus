### Relationship: Account → Card → Transaction → FraudAlert  
**Path:** Card linked to Account, transaction can generate fraud alert  
```
Account [has] Card [processes] Transaction [triggers] FraudAlert
Example:
ACC-00001 [has] CARD-00001 [processes] TXN-543 (£2,000 ATM) [triggers] FRAUD-091
```