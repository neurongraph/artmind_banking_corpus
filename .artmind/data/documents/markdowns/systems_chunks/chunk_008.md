#### 5. Payment Processing System (PPS)  
**System ID:** PPS-001
**Purpose:** Process customer payments and inter-bank settlements
**Technology:** Java microservices, message queue (RabbitMQ)
**Deployment:** Cloud (AWS)
**Processing: 24/7 real-time + batch overnight (BACS)  
**Key Functions:**
- Transfer initiation and validation
- Standing order processing
- Direct debit processing
- Settlement to other banks
- Reconciliation and reporting  
**Payment Methods Supported:**
- Faster Payments Service (FPS) — Real-time, up to £1M
- BACS — Overnight, high volume
- CHAPS — High-value, real-time
- Internal transfers (same bank)  
**Batch Processing Schedule:**
- FPS: Real-time (immediate)
- BACS Submission: 20:00 GMT daily
- CHAPS: Real-time (during hours)  
**Performance:**
- FPS processing: <15 minutes
- BACS processing: Next business day
- Success rate: 99.95%
- Failed transactions: <5 per day  
**Integration:**
- Account Management System (AMS) — account validation
- Fraud Detection Engine (FDE) — fraud check
- Bank of England Settlement Systems (external)
- Treasury System — reconciliation  
---