# AI & Cloud Security Basics — Research and Checklist

**Project type:** Beginner-friendly cybersecurity research project  
**Focus:** Cloud security foundations and security considerations for AI-enabled cloud applications  
**Status:** Educational checklist and reference guide (not a production security audit)

## Overview
This repository introduces core cloud security concepts and a practical checklist for reviewing a small cloud-hosted application that may use AI features.

## Learning objectives
- Explain the cloud shared-responsibility model.
- Identify common cloud security control areas.
- Apply least privilege, MFA, encryption, logging, backups, and secure configuration concepts.
- Recognize AI-specific risks such as prompt injection, sensitive-data disclosure, unsafe tool use, and model/data integrity issues.
- Record review findings and prioritize remediation.

## Project structure
```text
ai-cloud-security-basics/
├── README.md
├── research/
│   ├── cloud_security_basics.md
│   └── ai_security_basics.md
├── checklist/
│   └── security_checklist.md
├── templates/
│   └── findings_register.csv
├── docs/
│   └── sample_architecture.md
└── LICENSE
```

## How to use
1. Read the research notes in `research/`.
2. Review the sample architecture in `docs/`.
3. Work through `checklist/security_checklist.md`.
4. Record observations in `templates/findings_register.csv`.
5. Mark each control **Pass**, **Fail**, **N/A**, or **Needs Review**. Do not claim a control is implemented unless you have evidence.

## Scope and safety
This is a learning project. It does not connect to a real cloud account, scan public systems, collect credentials, or perform penetration testing. Use only systems and lab environments you own or are explicitly authorized to assess. Never commit passwords, API keys, access tokens, private keys, personal data, or confidential logs to GitHub.

## Suggested GitHub repository description
`Beginner-friendly research project covering AI and cloud security fundamentals, practical security checklist, sample architecture, and findings register.`

## Suggested topics for a presentation
1. What is cloud security?
2. Shared responsibility model.
3. Identity and access management.
4. Data protection and encryption.
5. Network security and secure configuration.
6. Logging, monitoring, backup, and incident response.
7. AI-specific security risks and safeguards.
8. Checklist results and recommendations.

## References
See the source list in `research/cloud_security_basics.md` and `research/ai_security_basics.md`.
