## 5. INCIDENT RESPONSE FLOWCHART  
```
Issue Detected
↓
Severity Assessment
├─ Critical (System Down) → IMMEDIATE ESCALATION
├─ High (Partial Outage) → Escalate within 1 hour
└─ Low (Degraded) → Escalate within 4 hours
↓
Investigate (See Troubleshooting)
├─ Issue Identified → Apply Fix
└─ Issue Not Found → Escalate to Team
↓
Implement Fix
├─ Rollback? → Roll back deployment
├─ Restart? → Restart service
└─ Config Change? → Update and reload
↓
Verify Recovery
├─ PASS → Close incident, document
└─ FAIL → Escalate to team lead
↓
Document Incident
- Record in incident log
- Timeline of actions
- Root cause analysis
- Prevention measures for future
```  
---