### Scenario 2: Temporary Address Change (Holiday Home)  
**Situation:** Customer moving to holiday home for 3 months, wants to update address temporarily  
**Approach:**  
**Option A: Update as Permanent (Simpler)**
- Update to new address
- When customer returns, submit another address change
- Simpler but creates extra work  
**Option B: Mark as Temporary (Better)**
- Note in system: "Temporary address change until [date]"
- Set reminder to contact customer on return date
- Ask: "When you return, shall we change back?"
- Reduces address change requests  
**Implementation:**
```
Address Change Type: TEMPORARY
Old Address: 123 Oak Lane, Manchester, M1 1AA
Temporary Address: 789 Beach Road, Marbella, Spain
Effective Date: 2026-06-01
Return Date: 2026-09-01
Revert To: Manchester address
Contact Before: 2026-08-25 (reminder for customer)
```  
---