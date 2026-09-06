## Security Architecture  
### Authentication & Authorization  
**Customer Authentication:**
- Internet Banking: Username/password + OTP (email/SMS)
- Mobile App: Biometric (fingerprint/face) + optional PIN
- Branch: Photo ID verification  
**Internal Authentication:**
- Staff: LDAP/Active Directory
- API Services: Mutual TLS (mTLS) + JWT
- Admin Access: Multi-factor authentication (MFA)  
**Authorization:**
- Role-Based Access Control (RBAC)
- Attribute-Based Access Control (ABAC) for sensitive operations
- Audit logging for all access