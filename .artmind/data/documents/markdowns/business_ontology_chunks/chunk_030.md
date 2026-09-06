### Customer Constraints  
| Rule | Constraint |
|------|-----------|
| Must have identity verified | `customer.kyc_status = 'Verified'` |
| Must pass AML screening | `customer.aml_status != 'Flagged'` |
| Must have valid address | `customer.address IS NOT NULL AND verified` |
| Age 18+ | `customer.age >= 18` |