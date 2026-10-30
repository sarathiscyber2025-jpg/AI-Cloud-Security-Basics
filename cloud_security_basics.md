# Cloud Security Basics — Research Notes

## 1. Introduction
Cloud security is the set of policies, technologies, processes, and operational practices used to protect cloud-hosted identities, applications, infrastructure, and data. The goal is to preserve confidentiality, integrity, and availability.

- **Confidentiality:** information is accessible only to authorized people and services.
- **Integrity:** information and configurations are protected from unauthorized changes.
- **Availability:** systems and data remain accessible when needed.

## 2. Cloud service models
- **IaaS (Infrastructure as a Service):** the customer manages more of the operating system, applications, and configuration.
- **PaaS (Platform as a Service):** the provider manages more of the underlying platform; the customer still secures their application, data, and access.
- **SaaS (Software as a Service):** the provider operates the application; customers still manage user access, data handling, and configuration options.

The exact division of duties varies by provider and service.

## 3. Shared responsibility
Cloud security is shared between the provider and customer. Providers generally secure the underlying facilities and cloud infrastructure. Customers remain responsible for the security tasks assigned to them, which can include identity permissions, data, application code, network rules, and configuration. Always check the provider's responsibility model for each service.

## 4. Core security controls
### Identity and access management (IAM)
- Use unique user accounts.
- Enable multi-factor authentication (MFA).
- Apply least privilege: grant only the permissions required.
- Prefer short-lived credentials and managed identities where supported.
- Review and remove unused accounts, keys, and permissions.

### Data protection
- Classify data by sensitivity.
- Encrypt data in transit using modern TLS.
- Encrypt sensitive data at rest.
- Restrict access to storage and databases.
- Keep secrets in a managed secrets store, not in source code.
- Set retention and secure deletion rules.

### Network security
- Avoid exposing management interfaces to the public internet.
- Restrict inbound and outbound traffic to what is necessary.
- Segment networks and workloads.
- Use secure private connectivity where appropriate.
- Review firewall and security-group rules regularly.

### Secure configuration and vulnerability management
- Use secure baseline configurations.
- Patch operating systems, libraries, containers, and applications.
- Remove unused services and default credentials.
- Scan dependencies and container images using approved tools.
- Track configuration changes.

### Logging and monitoring
- Enable audit logs for account, identity, network, and resource activity.
- Protect logs from unauthorized modification or deletion.
- Alert on suspicious sign-ins, privilege changes, and unusual resource activity.
- Establish a review and escalation process.

### Backup and recovery
- Back up important data and configurations.
- Protect backups with access controls and encryption.
- Keep copies isolated from ordinary production access where possible.
- Test restoration regularly and document recovery objectives.

### Incident response
- Define who receives alerts and who makes decisions.
- Document containment, investigation, recovery, and communication steps.
- Preserve relevant logs and evidence.
- Conduct a lessons-learned review after incidents.

## 5. Common cloud security risks
- Publicly exposed storage or databases.
- Excessive permissions and compromised credentials.
- Unpatched software and vulnerable dependencies.
- Weak network rules.
- Missing or incomplete audit logs.
- Inadequate backup and recovery testing.
- Misconfigured services and exposed secrets.

## 6. Conclusion
Cloud security is not a one-time setup. It requires secure design, careful configuration, monitoring, regular review, and clear responsibility between the provider and customer.

## References
1. AWS, **Security in IAM and AWS STS**: https://docs.aws.amazon.com/IAM/latest/UserGuide/security.html
2. UK National Cyber Security Centre, **Cloud security shared responsibility model**: https://www.ncsc.gov.uk/collection/cloud/understanding-cloud-services/cloud-security-shared-responsibility-model
3. Microsoft Learn, **Cloud security benchmark — Governance and Strategy**: https://learn.microsoft.com/security/benchmark/azure/mcsb-governance-strategy
4. Cloud Security Alliance, **Security Guidance for Cloud Computing**: https://cloudsecurityalliance.org/research/guidance/
