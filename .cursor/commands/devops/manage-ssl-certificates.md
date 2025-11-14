# Manage SSL Certificates

Manage SSL/TLS certificates for secure connections and HTTPS.

## What This Command Does

Manages SSL certificates by:
- Requesting and installing SSL certificates
- Configuring certificate auto-renewal
- Managing certificate lifecycle
- Setting up certificate monitoring
- Configuring certificate security

## How It Works

1. **Understand Certificate Needs**
   - Ask about domains needing certificates
   - Identify certificate type (Let's Encrypt, commercial, etc.)
   - Understand certificate requirements
   - Determine certificate provider
   - Get context on existing certificates

2. **Request and Install Certificates**
   - Request SSL certificates
   - Validate domain ownership
   - Install certificates on servers
   - Configure certificate chains
   - Document certificate installation

3. **Configure Certificate Management**
   - Set up certificate auto-renewal
   - Configure certificate monitoring
   - Set up certificate expiration alerts
   - Configure certificate rotation
   - Document certificate management

4. **Configure Certificate Security**
   - Set up certificate pinning
   - Configure HSTS
   - Set up certificate validation
   - Configure certificate security policies
   - Document security configuration

## What to Tell the User

- "What domains need SSL certificates?"
- "What certificate provider? (Let's Encrypt, AWS ACM, etc.)"
- "What are your certificate requirements?"
- Manage SSL certificates
- "SSL certificate management complete! Certificates: [installed]. Auto-renewal: [configured]. Monitoring: [setup]"

## See Also

- **[Manage DNS](manage-dns.md)**: DNS for certificate validation
- **[Setup Load Balancer](setup-load-balancer.md)**: SSL termination on load balancers
- **[Check Security](check-security.md)**: Security audit including certificates

