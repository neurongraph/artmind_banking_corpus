### Startup Sequence (Follow Exactly)  
**Phase 1: Database (5–10 minutes)**  
```
1. Start PostgreSQL
systemctl start postgresql@main

2. Wait for startup
psql -U postgres -c "SELECT version();"
(Should return version info)

3. Verify replication
psql -U postgres -c "SELECT slot_name, restart_lsn FROM pg_replication_slots;"
(Should show active slots)

4. Verify backups
du -h /var/lib/postgresql/backup/
```  
**Phase 2: Core Applications (10–15 minutes)**  
```
1. Start AMS (Account Management)
kubectl apply -f /deployments/ams-deployment.yaml
kubectl rollout status deployment/ams --timeout=5m

2. Start PPS (Payment Processing)
kubectl apply -f /deployments/pps-deployment.yaml
kubectl rollout status deployment/pps --timeout=5m

3. Start FDE (Fraud Detection)
kubectl apply -f /deployments/fde-deployment.yaml
kubectl rollout status deployment/fde --timeout=5m

4. Verify core services healthy
kubectl get pods -n production | grep Running
(Should see all pods in "Running" state)
```  
**Phase 3: Customer-Facing (5–10 minutes)**  
```
1. Start IBP (Internet Banking)
kubectl apply -f /deployments/ibp-deployment.yaml
kubectl rollout status deployment/ibp --timeout=5m

2. Start MBA (Mobile App backend)
kubectl apply -f /deployments/mba-deployment.yaml
kubectl rollout status deployment/mba --timeout=5m

3. Clear cache
redis-cli FLUSHALL

4. Test endpoints
curl https://api.firstuk.bank/health
(Should return "status": "ok")
```  
**Phase 4: Verification (5 minutes)**  
```
1. Run smoke tests
bash /tests/smoke_tests.sh
Expected: All tests PASS

2. Verify dashboard
Check https://dashboard.firstuk.bank
Expected: All systems Green

3. Notify team
Post to #operations-channel: "Systems startup complete"
```  
**If Any Phase Fails:** Go to Step 6 (Incident Response) — Do NOT proceed to next phase  
---