## Integration Architecture  
### Event-Driven Integration (Asynchronous)  
**Message Queue:** Apache Kafka  
**Key Topics:**
- `account.created` — New account opened
- `transaction.recorded` — Transaction completed
- `account.closed` — Account closed
- `fraud.alert` — Fraud detection alert
- `kyc.completed` — KYC verification done
- `standing-order.processed` — Standing order executed  
**Example Flow:**
```
1. Customer initiates transfer via IBP
2. PPS validates transfer → `transfer.initiated` event
3. FDE checks fraud → `fraud.scored` event
4. If approved: PPS processes → `transfer.completed` event
5. AMS updates balance → `balance.updated` event
6. DW updates data → analytics available in 5 min
```