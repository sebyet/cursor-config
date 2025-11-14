# Setup Load Balancer

Set up and configure load balancers to distribute traffic across multiple resources.

## What This Command Does

Sets up load balancers by:
- Configuring load balancers (ALB, NLB, etc.)
- Setting up health checks
- Configuring routing rules
- Setting up SSL/TLS termination
- Configuring load balancer security

## How It Works

1. **Understand Load Balancing Needs**
   - Ask about load balancing requirements
   - Identify backend resources
   - Understand traffic patterns
   - Determine load balancer type
   - Get context on cloud provider

2. **Design Load Balancer Configuration**
   - Choose load balancer type
   - Configure health checks
   - Set up routing rules
   - Configure SSL/TLS
   - Plan security groups

3. **Generate Load Balancer Configuration**
   - Create load balancer configuration
   - Set up target groups
   - Configure health checks
   - Set up SSL/TLS certificates
   - Document load balancer setup

4. **Configure Security and Monitoring**
   - Set up security groups
   - Configure WAF rules (if applicable)
   - Set up load balancer monitoring
   - Configure access logs
   - Document security configuration

## What to Tell the User

- "What type of load balancer? (ALB, NLB, Classic, etc.)"
- "What backend resources need load balancing?"
- "What are your traffic requirements?"
- Set up load balancer configuration
- "Load balancer setup complete! Type: [configured]. Health checks: [setup]. SSL: [configured]"

## See Also

- **[Auto Scaling](auto-scaling.md)**: Auto-scaling with load balancers
- **[Check Performance](check-performance.md)**: Monitor load balancer performance
- **[Setup WAF](setup-waf.md)**: Web Application Firewall for load balancers

