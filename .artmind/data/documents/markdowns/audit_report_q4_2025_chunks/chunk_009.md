### E. Account Closure — ⚠️ NEEDS IMPROVEMENT (Observation)  
**Scope:** Customer-initiated and bank-initiated account closures
**Period Tested:** Oct 1 – Dec 31, 2025
**Closures Tested:** 15 sample closures
**Compliance Rate:** 80%  
**Findings:**  
**✅ Strengths:**
- All closures processed per [[sop_account_closure]]
- Final balances calculated correctly
- Standing orders cancelled  
**⚠️ Finding (High Priority):**  
**Missing Documentation on Bank-Initiated Closures**
- 3 of 15 closures (20%) were bank-initiated
- Only 1 of 3 had proper 30-day notice letter on file
- Only 2 of 3 had documented reason (fraud, policy, regulatory)
- Impact: Regulatory risk (FCA may query closure justification)  
**Remediation Required:**
1. Implement mandatory closure letter procedure
2. Document closure reason (dropdown: regulatory, fraud, policy, other)
3. Mandatory 30-day notice for bank-initiated closures
4. Audit trail for all closures
5. Retest Q1 2026  
**Key Metric:**
- Customer-initiated closures: 12/12 (100%) ✅
- Bank-initiated closures: 3/15 (20%)
- With proper notice: 1/3 (33%) ⚠️
- With documented reason: 2/3 (67%) ⚠️  
---