### D. Standing Orders Management — ⚠️ SATISFACTORY (Observation)  
**Scope:** Recurring payment setup, execution, modifications, cancellations
**Period Tested:** Oct 1 – Dec 31, 2025
**Standing Orders Active:** 47 total orders
**Orders Tested:** 20 sample (42% of active)
**Compliance Rate:** 85%  
**Findings:**  
**✅ Strengths:**
- All standing orders established per [[sop_standing_orders]]
- Execution timing correct (95% on due date)
- Recipient validation working  
**⚠️ Findings (Medium Priority - 2 issues):**  
**Finding 1: Missing Modification Documentation**
- 3 of 20 orders (15%) had modifications without audit trail
- Example: Payment amount changed from £500 to £750, not documented
- Risk: Difficulty tracing changes for audit/dispute
- Impact: Medium (affects audit trail, not customer impact)  
**Finding 2: Cancellation Delay**
- 2 of 20 orders (10%) took >1 day to cancel
- Customer requested cancellation; processed day after
- SLA: Immediate cancellation
- Impact: Low (only 1-day delay, manually corrected)  
**Remediation Required:**
1. Document all modifications (audit trail)
2. Implement automated cancellation (effective immediately)
3. Retest Q1 2026  
**Key Metric:**
- Standing orders created: 47 (100%) ✅
- Timely execution: 44/47 (95%) ✅
- Proper cancellations: 45/47 (96%) ✅
- Missing documentation: 3/47 (6%) ⚠️  
---