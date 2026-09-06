## SCENARIO 3: Failed Transaction  
**Customer:** "My transfer didn't go through."  
**Agent Script:**  
```
Agent: "I'm sorry to hear that. Let me look into this for you.

Could you tell me:
- When did you attempt the transfer?
- How much was it for?
- To which account?

[Customer provides details]

Let me check your account... [Pull transaction record]

I can see what happened. The transfer failed because [reason:
insufficient funds/invalid recipient/account closed/other].

Here's what we can do:
[Offer resolution based on scenario]

Would this work for you?"

[If insufficient funds:]
"Once you have enough balance, we can resubmit the transfer
immediately."

[If invalid recipient:]
"Can you double-check the account number? If you'd like, I
can help you get it right and resubmit."

[If account closed:]
"It looks like the recipient's account is closed. Do you have
an alternative account for them?"
```  
---