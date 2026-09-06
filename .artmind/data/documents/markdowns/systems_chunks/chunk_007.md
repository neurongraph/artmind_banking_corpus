#### 4. Fraud Detection Engine (FDE)  
**System ID:** FDE-001
**Purpose:** Real-time detection and prevention of fraudulent transactions
**Technology:** Python, Apache Kafka, TensorFlow (ML models)
**Deployment:** Cloud (AWS) + on-premises (for sensitive rules)
**Latency:** <100ms per transaction  
**Key Functions:**
- Transaction risk scoring
- Anomaly detection (ML models)
- Rule-based detection
- Card fraud prevention
- Account takeover detection
- Suspicious activity flagging  
**Fraud Rules (Examples):**
- Large transaction amount (>£5,000)
- Geographic anomaly (transaction in different country within 2 hours)
- Velocity checks (>5 transactions within 1 hour)
- Unusual beneficiary (new beneficiary + large transfer)
- Card not present (CNP) high-value transaction  
**Machine Learning Models:**
- Transaction Risk Model (trained on 2,000+ fraud cases)
- Anomaly Detection Model (unsupervised)
- Chargeback Prediction Model  
**Alert Escalation:**
- Low Risk: Auto-approve
- Medium Risk: Require OTP verification
- High Risk: Block transaction, notify customer, escalate to Financial Crime team (see [[departments]])  
**Performance:**
- Detection Rate: 97%+
- False Positive Rate: <2%
- Monthly fraud prevented: ~£45k–£80k  
**Integration:**
- Account Management System (AMS) — transaction data
- Internet Banking Platform (IBP) — real-time blocking
- Mobile Banking App (MBA)
- Payment Processing System (PPS)
- Financial Crime System — SAR filing  
---