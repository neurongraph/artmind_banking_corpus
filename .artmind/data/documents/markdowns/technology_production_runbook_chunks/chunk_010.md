## 4. COMMON ISSUES & TROUBLESHOOTING  
### Issue: "AMS Service Unavailable"  
**Symptoms:** API returns 503, IBP shows error  
**Steps:**
```
1. Check service status
kubectl get pod -n production | grep ams

2. Check logs
kubectl logs -f deployment/ams | tail -50

3. Check database connection
curl https://api.firstuk.bank/ams/health/db

4. If DB connection issue
Verify PostgreSQL running: systemctl status postgresql@main
Verify connection pool: psql -U postgres -c "SELECT count(*) FROM pg_stat_activity WHERE datname='firstuk_prod';"

5. Restart service
kubectl rollout restart deployment/ams
kubectl rollout status deployment/ams --timeout=5m

6. Verify recovery
curl https://api.firstuk.bank/accounts -H "Authorization: Bearer [token]"
(Should return account list)
```