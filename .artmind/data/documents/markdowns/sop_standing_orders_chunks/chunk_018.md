### Failure Handling  
**Step 1: Detect Failure**
- System logs failed standing order attempt
- Marks standing order status as "Failed"  
**Step 2: Alert Customer**
- Email/SMS sent to customer
- Alert includes: Amount, recipient, failure reason
- Request for action (provide funds, update payee)  
**Step 3: Retry Attempt**
- System retries once (usually within 24 hours)
- If retry successful: Standing order resumes  
**Step 4: Escalation**
- If retry fails: Standing order suspended
- Staff review required
- Contact customer to resolve  
**Step 5: Resolution**
- Customer provides corrected information (if needed)
- Staff updates standing order
- Standing order resumes or customer opts for cancellation  
---