### Scalability  
**Auto-Scaling:**
- Microservices: Auto-scale based on CPU (target: 70%)
- Database: Read replicas for read-heavy operations
- API Gateway: Managed by Kong (can scale to 1000+ QPS)  
**Performance Optimization:**
- Caching (Redis) for frequently accessed data
- Database indexes on key columns
- Asynchronous processing (Kafka) for non-critical operations  
---