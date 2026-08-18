# azure-policy-defender-cloud
Azure Policy governance and Microsoft Defender for Cloud security posture lab for TechPay Solutions
# Azure Policy + Defender for Cloud Lab — TechPay Solutions

## Project Overview
This project implements Azure Policy governance and Microsoft 
Defender for Cloud security posture management for a fictional 
fintech company — TechPay Solutions S.L. It covers compliance 
standard activation, custom policy creation, and gap analysis 
against NIS2, Spain ENS and SWIFT frameworks.

## What This Project Covers
- 4 compliance standards activated in Defender for Cloud
- Custom Azure Policy for data classification enforcement
- Real compliance gap analysis (24% overall compliance)
- Remediation task identification and prioritization
- GDPR mapping to Azure governance controls

## Compliance Standards Activated
| Standard | Recommendations | Compliance |
|---|---|---|
| EU 2022/2555 (NIS2) | 181 | 24% |
| Spain ENS | 821 | 25% |
| Microsoft Cloud Security | 226 | 0% |
| SWIFT CSP-CSCF | 44 | Under evaluation |

## Custom Policy Created
**TechPay - Require Resource Classification Tag**
- Audits resources missing a Classification tag
- Supports GDPR Art. 25 (Privacy by Design)
- Foundation for automated DLP enforcement

## Key Findings
- 21 Azure resources evaluated
- 5 compliant (24%), 16 non-compliant (76%)
- 81 non-compliant policies identified
- Priority remediation: logging, encryption, MFA

## GDPR Compliance
| Article | Implementation |
|---|---|
| Art. 25 — Privacy by Design | Classification tag policy |
| Art. 32 — Security measures | Defender security standards |
| Art. 33 — Breach notification | Defender alerts |
| Art. 5(1)(f) — Integrity | Policy enforcement |

## Tools & Technologies
- Microsoft Defender for Cloud
- Azure Policy
- NIS2 / Spain ENS / SWIFT CSP-CSCF compliance frameworks
- Azure Compliance Dashboard

## Related Projects
- [Microsoft Sentinel Lab](https://github.com/Andrea1864/siem-microsoft-sentinel)
- [Azure Key Vault Lab](https://github.com/Andrea1864/azure-key-vault-secrets-management)
- [Microsoft Purview Lab](https://github.com/Andrea1864/microsoft-purview-data-protection)
- [TechPay GDPR ROPA](https://github.com/Andrea1864/gdpr-ropa-fintech)

## Author
Andrea Castillo — Law Graduate | Cybersecurity & GRC Specialist  
