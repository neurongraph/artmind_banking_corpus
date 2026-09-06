### Compliance Constraints  
| Rule | Constraint |
|------|-----------|
| SAR filed within 30 days | `SAR.filing_date <= suspicion_date + 30 days` |
| KYC refreshed 3-5 years | `KYC.next_review_date <= TODAY() + 5 years` |
| Fraud reimbursement 10 days | `Fraud_claim.reimbursement_date <= claim_date + 10 days` |  
---