# AI & Cloud Security Review Checklist

**Project / environment:** ____________________  
**Reviewer:** ____________________  
**Review date:** ____________________

For each item, record **Pass**, **Fail**, **N/A**, or **Needs Review**, and include evidence. This checklist is a starting point, not a certification or guarantee of security.

## A. Governance and inventory
- [ ] Cloud accounts, subscriptions, projects, and regions are documented.
- [ ] Important assets and data owners are identified.
- [ ] Provider/customer responsibilities are documented for each service.
- [ ] Security contacts and incident escalation paths are defined.
- [ ] Data classification and retention requirements are documented.

## B. Identity and access
- [ ] MFA is enabled for privileged and interactive accounts.
- [ ] Each person uses an individual account.
- [ ] Least-privilege permissions are applied.
- [ ] Privileged access is limited and reviewed.
- [ ] Unused accounts, keys, and permissions are removed.
- [ ] Secrets are stored in an approved secrets manager, not source code.
- [ ] Short-lived credentials or managed identities are used where possible.

## C. Data protection
- [ ] Sensitive data is identified and classified.
- [ ] Data in transit is protected with TLS.
- [ ] Sensitive data at rest is encrypted.
- [ ] Storage and database access is restricted.
- [ ] Public access is disabled unless explicitly required and approved.
- [ ] Backups are protected and restoration is tested.
- [ ] Retention and secure deletion rules are defined.

## D. Network and infrastructure
- [ ] Network access follows deny-by-default / minimum-required principles.
- [ ] Management interfaces are not unnecessarily public.
- [ ] Workloads are segmented where appropriate.
- [ ] Firewall and security-group rules are reviewed.
- [ ] Systems and dependencies receive security updates.
- [ ] Unused ports, services, and default accounts are disabled.
- [ ] Configuration changes are tracked.

## E. Logging and response
- [ ] Audit logging is enabled for important cloud activity.
- [ ] Logs are access-controlled and protected from tampering.
- [ ] Alerts exist for suspicious sign-ins and privilege changes.
- [ ] Monitoring responsibilities and review frequency are defined.
- [ ] An incident response plan is documented.
- [ ] Recovery and backup restoration procedures are tested.

## F. AI application controls (if AI is used)
- [ ] AI use cases, models, data sources, and limitations are documented.
- [ ] Prompts, files, retrieved content, and model outputs are treated as untrusted.
- [ ] Application authorization is enforced independently of model responses.
- [ ] AI agents and tools have only task-required permissions.
- [ ] Sensitive actions require human approval where appropriate.
- [ ] Inputs and outputs are validated before downstream use.
- [ ] Tests cover prompt injection and sensitive-data disclosure.
- [ ] AI logs avoid unnecessary secrets and personal data.
- [ ] Model, data, and dependency changes are reviewed.
- [ ] Unexpected AI behavior is monitored and can be escalated.

## G. Findings summary
- **Total controls reviewed:** ______
- **Pass:** ______
- **Fail:** ______
- **Needs Review:** ______
- **N/A:** ______

## Prioritization guide
- **High:** exposed sensitive data, public administrative access, compromised credentials, or excessive privileged access.
- **Medium:** missing monitoring, incomplete patching, weak backup testing, or incomplete AI output validation.
- **Low:** documentation gaps or improvements that do not create an immediate exposure.

Record each finding in `templates/findings_register.csv`. Assign an owner and target date. Re-test after remediation.
