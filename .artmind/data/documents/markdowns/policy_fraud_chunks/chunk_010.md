## Fraud Detection Framework  
### Detection Methods  
**1. Real-Time Transaction Monitoring (Fraud Detection Engine)**  
**See:** [[systems]] Fraud Detection Engine (FDE-001)  
**Rules Monitored:**
- Large transaction amount (>£5,000)
- Velocity checks (>5 transactions in 1 hour)
- Geographic anomaly (transaction in different country within 2 hours)
- New beneficiary with large transfer
- Unusual merchant/category
- Cash withdrawal followed by immediate large transfer
- Multiple failed authentication attempts  
**Action:** Alert generated, transaction placed on hold (up to 5 days)  
**2. Manual Review**  
**Triggers for Manual Investigation:**
- Customer reports suspected fraud
- Unusual account activity
- Pattern changes (normal behavior deviation)
- High-value transaction
- Regulatory alert (sanctions, AML)  
**Review Process:**
- Financial Crime team analyzes activity
- Customer contacted for explanation (if safe)
- Transaction approved or blocked based on risk  
**3. Fraud Pattern Analysis**  
**Advanced Analytics:**
- Machine learning model learns normal customer behavior
- Anomalies flagged for review
- Recurring fraud patterns identified
- Fraud perpetrators tracked across customers  
**Feedback Loop:**
- Confirmed fraud updates model
- False positives refined
- Model continuously improves  
---