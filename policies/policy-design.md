# Azure Policy Design — TechPay Solutions

## Custom Policy: Require Resource Classification Tag

### Overview
This policy audits all Azure resources that are missing 
a Classification tag. Tags are used to identify the 
sensitivity level of data processed by each resource.

### Policy Rule
- **Condition**: Resource does not have a 'Classification' tag
- **Effect**: Audit — flags non-compliant resources
- **Scope**: Azure subscription 1

### Classification Tag Values
| Tag Value | Meaning | Example Resources |
|---|---|---|
| Public | Non-sensitive data | Static websites |
| Internal | Internal business data | Internal APIs |
| Confidential | Personal data (GDPR) | Customer databases |
| Highly-Confidential | Payment/AML data | Payment processing |

### Why This Policy Matters
Without classification tags:
- Security team cannot identify sensitive resources
- DLP policies cannot be applied automatically
- Incident response is slower — unknown data sensitivity
- GDPR Art. 32 compliance is harder to demonstrate

### Effect Options Explained
| Effect | What It Does |
|---|---|
| Audit | Flags non-compliant but allows creation |
| Deny | Blocks creation of non-compliant resources |
| Modify | Automatically adds the tag |

We use **Audit** for initial rollout — after 30 days 
switch to **Deny** once all teams are aware.

### GDPR Connection
- **Art. 25** — Privacy by Design: classify data at resource creation
- **Art. 32** — Security: know what data each resource holds
- **Art. 30** — ROPA: tags support data mapping and inventory
