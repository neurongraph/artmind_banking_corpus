## Step 5: Standing Order Execution  
### Scheduled Processing  
**Timing:**
- Standing order executes on scheduled date (e.g., 15th of month)
- Processing occurs early morning (before business hours)
- Funds transferred via FPS (Faster Payments Service)
- Recipient account receives funds within 1 hour  
**Execution Process:**
1. System identifies standing orders due
2. Validates source account has sufficient funds
3. Initiates FPS transfer
4. Records transaction in ledger
5. Updates standing order status (completed)
6. Notifies customer (optional, if opted in)  
**If Funds Unavailable:**
- Transfer fails (declined)
- Customer notified of failure
- Retry attempt made (usually once)
- Manual intervention if persistent failure  
---