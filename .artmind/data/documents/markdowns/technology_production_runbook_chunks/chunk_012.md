### Issue: "High Fraud Alert Rate"  
**Symptoms:** Many legitimate transactions flagged as fraud, customer complaints  
**Steps:**
```
1. Check FDE alert rate
kubectl logs -f deployment/fde | grep "ALERT" | wc -l
(Compare to baseline: <10 alerts/hour)

2. Review recent alerts
tail -100 /var/log/fde/alerts.log | grep -A5 "false_positive"

3. If alert rate >3x normal
Check for DDoS/attack: kubectl get events -n production

4. Temporarily loosen rules
Edit /config/fraud_rules.yaml, restart FDE
Notify Financial Crime team

5. Review with team
Schedule urgent meeting to review false positives

6. Restore to normal settings
Once resolved, revert rule changes
```  
---