### Monitoring Methods  
**Automated Rules (Fraud Detection Engine, see [[systems]]):**  
| Rule | Threshold | Action |
|------|-----------|--------|
| Large deposit | >£50,000 in 24h | Alert + manual review |
| Rapid movement | Deposit then withdrawal <2h | Alert for review |
| Multiple small transfers | 10+ transfers to different recipients <24h | Velocity alert |
| Geographic anomaly | Transaction in different country within 2 hours | Alert for review |
| High-risk jurisdiction | Transaction with sanctioned country | Auto-block |
| Unusual beneficiary | Transfer to new beneficiary >threshold | Alert for review |  
**Manual Monitoring:**
- Financial Crime team reviews alerts
- Pattern analysis for suspicious sequences
- Behavioral profiling changes
- Judgment-based assessment