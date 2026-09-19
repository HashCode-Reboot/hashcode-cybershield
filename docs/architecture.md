# Architecture — CyberShield

```mermaid
flowchart TB
 A[Assets] --> I[Inventory]
 I --> C[Collectors]
 C --> N[Normalization]
 N --> D[Detection Engine]
 TI[Threat Intelligence] --> D
 V[Vulnerability Scanner] --> R[Risk]
 D --> R
 R --> AL[Alerts]
 AL --> IR[Response Playbooks]
 IR --> AUD[Audit / Lessons]
 AUD --> D
```

## Principes

Architecture modulaire, agents légers, chiffrement en transit et au repos, RBAC, journalisation, signatures/version des règles et déploiement progressif.

Le projet est défensif : aucune automatisation offensive non autorisée ne fait partie du périmètre.