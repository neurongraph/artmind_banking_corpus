### Caching Layer (Redis)  
**Purpose:** Reduce database load, improve response times  
**Cache Keys:**
- `account:{accountId}:balance` — Current balance (5-min TTL)
- `customer:{customerId}:profile` — Customer info (10-min TTL)
- `fraud-rules` — Fraud detection rules (1-hour TTL)  
---