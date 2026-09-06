### End of Business (17:00 PM)  
**Checklist (10 minutes):**  
- [ ] **Payment Settlement Confirmation** — Verify daily settlement completed
- Expected: All FPS/BACS payments settled by 17:30  
- [ ] **Reconciliation Report** — Run nightly reconciliation
- Command: `python /scripts/reconciliation.py`
- Expected: "PASS: All transactions reconciled"  
- [ ] **Backup Initiation** — Trigger nightly backup
- Command: `aws s3 sync /data/backups s3://firstuk-backups/ --sse AES256`
- Expected: "Backup complete: XXX MB uploaded"  
- [ ] **Data Warehouse Load** — Trigger nightly DW load
- Command: `spark-submit /scripts/dw_load.py`
- Expected: "Load complete: NNN rows inserted"  
---