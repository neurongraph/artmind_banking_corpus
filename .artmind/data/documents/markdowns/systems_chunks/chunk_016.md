### Customer APIs  
| Endpoint | Method | Purpose | Auth |
|----------|--------|---------|------|
| `/customers` | POST | Create customer | API Key + JWT |
| `/customers/{id}` | GET | Get customer details | JWT |
| `/customers/{id}/kyc` | GET/POST | KYC verification | API Key (internal) |
| `/customers/{id}/aml-screening` | POST | AML screening | API Key (internal) |