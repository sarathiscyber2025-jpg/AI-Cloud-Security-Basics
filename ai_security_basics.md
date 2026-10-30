# AI Security Basics — Research Notes

## 1. Why AI security matters
AI-enabled applications may process user prompts, documents, business data, and outputs from external tools. This creates security concerns in addition to ordinary application and cloud risks. AI security should be considered throughout design, development, deployment, and operation.

## 2. AI-specific risks
- **Prompt injection:** untrusted text may try to override the application's intended instructions.
- **Sensitive-data disclosure:** prompts, retrieved documents, logs, or generated responses may reveal information that should remain private.
- **Excessive agency:** an AI agent may have more tool or account permissions than its task requires.
- **Insecure output handling:** model output may be treated as trusted input by another component without validation.
- **Data poisoning or integrity problems:** manipulated or poor-quality data may affect model behavior.
- **Supply-chain risk:** compromised libraries, models, plugins, or datasets may introduce vulnerabilities.
- **Insufficient monitoring:** unexpected model behavior or misuse may go unnoticed.

## 3. Recommended safeguards
- Treat prompts, uploaded files, retrieved content, and model output as untrusted input.
- Enforce authorization in application code; do not rely on the model to decide access rights.
- Give each AI service or agent only the minimum permissions it needs.
- Require human approval for sensitive or high-impact actions.
- Do not place secrets or personal data in prompts unless there is a justified, approved need.
- Apply data minimization, retention limits, and access controls to AI logs.
- Validate and safely handle model output before using it in commands, queries, or downstream systems.
- Test for prompt injection, data leakage, and unsafe tool use in an authorized test environment.
- Monitor usage, errors, access patterns, and policy violations.
- Document the model, data sources, intended use, limitations, and review process.

## 4. AI + cloud security layers
1. **Infrastructure:** isolate workloads, patch systems, and restrict network access.
2. **Identity and data:** authenticate users and services, authorize each request, and encrypt data.
3. **AI application:** validate inputs and outputs, apply safety controls, restrict tools, and monitor behavior.

## 5. Conclusion
AI features do not replace ordinary security controls. They make identity, data governance, application validation, monitoring, and human oversight especially important.

## References
1. AWS Security Blog, **The AWS AI Security Framework**: https://aws.amazon.com/blogs/security/the-aws-ai-security-framework-securing-ai-with-the-right-controls-at-the-right-layers-at-the-right-phases/
2. UK Government, **Code of Practice for the Cyber Security of AI**: https://www.gov.uk/government/publications/ai-cyber-security-code-of-practice/code-of-practice-for-the-cyber-security-of-ai
3. Cloud Security Alliance, **Security Guidance for Cloud Computing**: https://cloudsecurityalliance.org/research/guidance/
