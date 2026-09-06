### Issue: "Payment Processing Slow"  
**Symptoms:** FPS transfers taking >15 minutes, BACS delayed  
**Steps:**
```
1. Check payment queue
curl https://api.firstuk.bank/pps/queue-length

2. If queue growing
Monitor: kubectl logs -f deployment/pps | grep "pending"

3. Check if database is bottleneck
psql -U postgres -c "SELECT count(*) FROM pg_stat_activity WHERE wait_event_type='IO';"

4. If high I/O wait
Increase database resources: kubectl set resources deployment/ams --limits=memory=4Gi,cpu=2

5. Monitor recovery
Watch queue decrease: watch 'curl https://api.firstuk.bank/pps/queue-length'

6. If not improving
Escalate to database team (see Step 6)
```