# Azure Policy + Defender for Cloud Architecture
## TechPay Solutions

## Architecture Overview

Azure Resources (21 total)
│
├── rg-sentinel-lab
│ ├── law-sentinel-techpay
│ └── SecurityInsights
│
└── kv-techpay-secrets
│
▼
Azure Policy
│
├── Built-in Policies (1228)
│ ├── EU 2022/2555 NIS2 → 181 controls
│ ├── Spain ENS → 821 controls
│ └── Microsoft cloud → 226 controls
│
└── Custom Policies (1)
└── TechPay - Require Classification Tag
│
▼
Compliance Dashboard
│
├── 24% compliant (5/21 resources)
├── 81 non-compliant policies
└── 3 non-compliant initiatives
│
▼
Microsoft Defender for Cloud
│
├── Security recommendations
├── Secure Score
└── Remediation tasks
│
▼
GRC Analyst Review
│
├── Prioritize remediation
├── Document exceptions
└── Report to DPO + CISO


## Policy Enforcement Flow

New Azure resource created
↓
Azure Policy evaluates resource
↓
Compliant? → Resource deployed normally
↓
Non-compliant? → Audit log created
↓
Appears in Compliance dashboard
↓
GRC Analyst reviews and remediates
↓
DPO notified if GDPR-relevant gap


## GDPR Compliance Mapping
| GDPR Article | Azure Control |
|---|---|
| Art. 25 — Privacy by Design | Policy enforces secure defaults |
| Art. 32 — Security | Defender monitors security posture |
| Art. 33 — Breach notification | Defender alerts on incidents |
| Art. 5(1)(f) — Integrity | Policy enforces encryption tags |
