## 1. DAILY OPERATIONS  
### Pre-Business Hours (07:00 AM)  
**Checklist (15 minutes):**  
- [ ] **Check Dashboard** — Open ops dashboard at https://dashboard.firstuk.bank
- AMS status: Should be "Green"
- IBP status: Should be "Green"
- MBA status: Should be "Green"
- PPS status: Should be "Green"  
- [ ] **Review Alerts Overnight** — Check alert queue for any issues reported 00:00–07:00
- Command: `kubectl get events -n production | grep -i warning`
- Action: Address any critical alerts immediately  
- [ ] **Verify Database Backups** — Check last backup completed
- Command: `aws s3 ls s3://firstuk-backups/ --recursive | tail -5`
- Expected: Most recent backup within last 24 hours  
- [ ] **Check Payment Systems** — Verify BACS/FPS connections active
- Command: `curl https://api.firstuk.bank/health | grep "payments"`
- Expected: "status": "ok"  
**Issue Found?** → Go to Step 6 (Incident Response)