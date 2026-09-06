### Entity: Fraud Alert  
**Definition:** A system-generated alert when fraud is detected.  
**Attributes:**
- `alert_id` — Unique identifier
- `account_id` — Linked account
- `transaction_id` — Linked transaction (if applicable)
- `alert_type` — Unauthorized use, Card fraud, Account takeover, Rule violation
- `fraud_score` — Risk score (0–100, where 100 = definite fraud)
- `risk_level` — Low, Medium, High, Critical
- `detected_date` — Date alert generated
- `alert_status` — Auto-approved, Manual review, Blocked
- `action_taken` — Approved, Blocked, Under review, False positive
- `reviewer` — Financial Crime team member (if manual review)  
**Example Fraud Patterns:**
- Transaction in different country within 2 hours of previous transaction
- Large ATM withdrawal (>£2,000) from unusual location
- Card used by different person
- Velocity check (>5 transactions in 1 hour)  
**Key Business Rules:**
- High-risk alerts automatically block transaction
- Customer can dispute fraud (Fraud Policy)
- Bank reimburses unauthorized fraud within 10 days
- Fraud data feeds ML model for continuous improvement  
**Relationships:**
- `on_account` → Account (1:many)
- `on_transaction` → Transaction (0:1)
- `triggers_investigation` → FraudInvestigation (1:1, optional)  
---