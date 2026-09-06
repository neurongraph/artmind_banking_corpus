### During Business Hours (09:00–17:00)  
**Hourly Checks (5 minutes each):**  
- [ ] **API Gateway Health** — Monitor Kong gateway
- Command: `kong health --yaml | grep status`
- Expected: All services responding <100ms  
- [ ] **Database Connection Pool** — Check PostgreSQL connections
- Command: `psql -U postgres -c "SELECT datname, count(*) FROM pg_stat_activity GROUP BY datname;"`
- Expected: <80% of max connections (200/250)  
- [ ] **Transaction Processing Rate** — Monitor throughput
- Command: `tail -f /var/log/pps/transactions.log | grep -c "SUCCESS" | head -1`
- Expected: 2–5 transactions/minute during business hours  
**Issue Found?** → Go to Step 6 (Incident Response)