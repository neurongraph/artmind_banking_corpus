## Application Landscape  
### Core Banking Systems  
#### 1. Account Management System (AMS)  
**System ID:** AMS-001
**Purpose:** Central repository for customer accounts, balances, and transactions
**Technology:** Java microservices, PostgreSQL database
**Deployment:** Cloud (AWS)
**Availability:** 99.9% (SLA)  
**Key Functions:**
- Account creation and lifecycle
- Balance management
- Transaction recording
- Interest calculation
- Account status tracking  
**Data Model:**
- Customers
- Accounts (see [[business_ontology]])
- Account Holders (primary, secondary, joint)
- Transactions
- Account Status  
**APIs Exposed:**
- `POST /accounts` — Create account
- `GET /accounts/{accountId}` — Retrieve account details
- `GET /accounts/{accountId}/balance` — Get balance
- `GET /accounts/{accountId}/transactions` — Transaction history
- `POST /accounts/{accountId}/transactions` — Record transaction  
**Integration:**
- Internet Banking Platform (IBP)
- Mobile Banking App
- Fraud Detection Engine
- Data Warehouse  
**Database:**
- PostgreSQL 13+
- 800 accounts × 2,000+ transactions = 1.6M records
- Backup: Daily encrypted backup to S3
- Recovery Point Objective (RPO): 15 minutes  
---