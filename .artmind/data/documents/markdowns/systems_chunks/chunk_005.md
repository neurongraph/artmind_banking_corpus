#### 2. Internet Banking Platform (IBP)  
**System ID:** IBP-001
**Purpose:** Web-based customer portal for account access and self-service
**Technology:** React.js frontend, Node.js backend
**Deployment:** Cloud (AWS)
**Availability:** 99.8% (SLA)  
**Key Features:**
- Secure login (username/password + OTP)
- Account information dashboard
- Transaction history and search
- Standing orders and direct debits
- Beneficiary management
- Money transfer
- E-statements
- Profile and settings management  
**Security:**
- TLS 1.3 encryption
- Session management (15-min idle timeout)
- Two-factor authentication (OTP via email/SMS)
- XSS/CSRF protection
- SQL injection prevention  
**Usage:**
- Daily active users: 200–300
- Peak traffic: 10:00–12:00 GMT
- Response time: <2 seconds (p95)  
**Integration:**
- Account Management System (AMS) — account data
- Fraud Detection Engine — transaction validation
- Payment Processing System (PPS) — transfer execution  
---