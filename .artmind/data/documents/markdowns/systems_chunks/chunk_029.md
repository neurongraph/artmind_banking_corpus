### Backup Strategy  
**Database Backups:**
- Continuous replication to standby (real-time)
- Daily encrypted backup to S3 (retention: 30 days)
- Weekly backup to cold storage (retention: 1 year)  
**Application Backups:**
- Source code in Git (GitHub)
- Docker images in registry (AWS ECR)
- Configuration in version control