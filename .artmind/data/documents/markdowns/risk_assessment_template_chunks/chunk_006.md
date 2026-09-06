## PART 2: SAMPLE RISK ASSESSMENT  
### Example: Account Opening Process — Data Quality Risk  
```
RISK ASSESSMENT FORM
Date Prepared: 15/01/2026
Prepared By: Rachel Green, Risk Manager
Reviewed By: James Wilson, Head of Risk
Assessment Period: Oct 1 – Dec 31, 2025
Risk ID: RISK-2026-001

Process Name: Online Account Opening
Business Unit: Retail Banking
Process Owner: Head of Customer Service
```  
---  
**RISK #1: Customer Data Entry Error**  
```
1. RISK DESCRIPTION
Customer completes online account opening form with incorrect personal information
(wrong name spelling, incorrect DOB, incorrect address). System accepts entry and
creates account with bad data. Later regulatory verification finds discrepancies.

2. RISK CATEGORY
☐ Credit Risk
☑ Operational Risk
☐ Compliance Risk
☐ Technology Risk
☐ Fraud Risk
☐ Reputational Risk

3. RISK SOURCE
☑ Internal Process
☑ People (Customer error, staff oversight)
☐ Systems
☐ External

4. LIKELIHOOD ASSESSMENT
Likelihood Score: 3 (Medium)

Supporting Evidence:
- Historical: 2–3 errors per month (15% of 200 new accounts)
- Trend: Flat (no improvement since Q3)
- Cause: Online form lacks real-time validation
- Industry benchmark: 10–15% error rate typical

5. IMPACT ASSESSMENT

Financial: £20k/year (rework, staff time)
Regulatory: Medium (data accuracy requirement per GDPR)
Customer: Low (1–2 customers affected per occurrence)
Operational: Medium (rework, processing delay)
Reputational: Low (internal issue, not visible to customer)

Impact Score: 3 (Moderate)

6. RISK SCORING
Risk Score = 3 × 3 = 9 (Medium Risk)

7. EXISTING CONTROLS

Control | Owner | Effectiveness | Evidence
---|---|---|---
Online form validation (name field required, format check) | Technology | Adequate | Catches empty/invalid formats
Manual review of application before account creation | CSR | Adequate | CSRs spot ~80% of errors
Post-opening verification (confirmation call/email) | CSR | Weak | Only some customers respond
System test of data import | Technology | Strong | System validates account creation

Overall Effectiveness: ~60% (controls catch most errors, but some slip through)

8. RESIDUAL RISK
Residual Risk = 9 × (1 – 0.60) = 3.6 ≈ 4 (Low-Medium Risk)

9. RISK APPETITE TOLERANCE
Operational Risk Target: <£50k/year
Current Impact: ~£20k/year ✅ (Within tolerance)
Residual Risk: Low-Medium

Compliant? ☑ Yes (but close to tolerance)

10. MITIGATION ACTIONS

Action | Owner | Target Date | Expected Impact
---|---|---|---
Implement client-side form validation (real-time) | Technology | 2026-02-28 | Catch 90% of errors pre-submission
Require confirmation of key fields (name, DOB) | Technology | 2026-02-28 | Reduce entry errors by 50%
Automated post-opening verification call (IVR) | Customer Service | 2026-03-31 | Catch 100% of remaining errors

Post-Mitigation Residual Risk:
Likelihood: 2 (Low) → Risk Score: 2 × 3 = 6
Residual Risk = 6 × (1 – 0.90) = 0.6 ≈ 1 (Low Risk) ✅

11. ACCOUNTABILITY
Risk Owner: Head of Customer Service
Escalation Contact: Head of Risk (if errors exceed £50k/year)
Monitoring: Monthly (error rate dashboard)
Review Date: 2026-04-15
```  
---