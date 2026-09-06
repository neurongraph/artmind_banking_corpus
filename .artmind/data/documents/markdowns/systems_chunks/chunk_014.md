## API Catalogue  
### Account APIs  
| Endpoint | Method | Purpose | Auth |
|----------|--------|---------|------|
| `/accounts` | POST | Create account | API Key + JWT |
| `/accounts/{id}` | GET | Get account details | JWT |
| `/accounts/{id}/balance` | GET | Get balance | JWT |
| `/accounts/{id}/transactions` | GET | List transactions | JWT |
| `/accounts/{id}/transactions` | POST | Record transaction | API Key (internal) |
| `/accounts/{id}/standing-orders` | GET/POST | Standing orders | JWT |
| `/accounts/{id}/direct-debits` | GET/POST | Direct debits | JWT |