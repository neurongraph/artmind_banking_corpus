## Network Security  
### Perimeter Security  
**Firewall:**
- Stateful inspection firewall
- Ingress: Port 443 (HTTPS) only for public APIs
- Egress: Restricted outbound (whitelist-based)
- Rules logged and monitored  
**DDoS Protection:**
- AWS Shield (managed DDoS protection)
- Rate limiting on APIs
- Anomalous traffic detection
- Traffic rerouting if DDoS detected  
**Intrusion Detection/Prevention:**
- Network-based IDS (Snort-like rules)
- Host-based IDS on critical systems
- Automated response (block malicious IPs)