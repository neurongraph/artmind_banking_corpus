### Shutdown Sequence  
**Phase 1: Notify Customers**  
```
1. Post maintenance notice
- Website banner: "System maintenance 02:00–03:00 AM"
- SMS alert to all customers (optional)
- Check: Maintenance window during low-traffic time
```  
**Phase 2: Graceful Shutdown (20 minutes)**  
```
1. Stop accepting new transactions
kubectl scale deployment ibp --replicas=0
kubectl scale deployment mba --replicas=0

2. Wait for in-flight transactions to complete
kubectl logs -f deployment/pps | grep "COMPLETE"
(Monitor for ~10 minutes)

3. Stop payment processing
kubectl scale deployment pps --replicas=0

4. Stop application servers
kubectl scale deployment ams --replicas=0
kubectl scale deployment fde --replicas=0

5. Backup database
/scripts/backup_database.sh

6. Stop database
systemctl stop postgresql@main
```  
**Phase 3: Notify Completion**  
```
Post to #operations: "System shutdown complete"
```  
---