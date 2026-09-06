### Data & Analytics Systems  
#### Data Warehouse (DW)  
**System ID:** DW-001
**Purpose:** Centralized analytics and business intelligence
**Technology:** AWS Redshift, Apache Spark
**Data Model:** Star schema (facts + dimensions)
**Update Frequency:** Real-time (for hot data), nightly batch (historical)  
**Key Data Marts:**
- **Customer Mart:** 500 customers × 50 attributes
- **Account Mart:** 800 accounts × attributes
- **Transaction Mart:** 2,000+ monthly transactions
- **Product Mart:** 5 products × performance metrics
- **Compliance Mart:** KYC, AML, complaints data  
**Dashboards & Reports:**
- Executive Dashboard (daily KPIs)
- Product Performance Dashboard
- Fraud Detection Dashboard
- Compliance & Risk Dashboard
- Customer Analytics Dashboard  
**Retention Policy:**
- Hot data (3 months): Real-time
- Warm data (1–3 years): Nightly batch
- Cold data (3+ years): Archive (S3)  
---