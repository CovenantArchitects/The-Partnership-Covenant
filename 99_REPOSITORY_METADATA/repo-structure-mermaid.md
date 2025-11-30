graph TD
    A[The-Partnership-Covenant<br/>199 files — v8.0-final] --> B[Root Files]
    A --> C[.github]
    A --> H[00_HARDWARE]
    A --> O[00_OVERVIEW]
    A --> R[00_ROADMAP_AND_VALIDATION]
    A --> S[00_SPECS]
    A --> F1[01_FINAL_DELIVERABLES]
    A --> F2[02_CORE_ARCHITECTURE_AND_APPENDICES]
    A --> F3[03_PUBLIC_ENGAGEMENT_DRAFTS]
    A --> F4[04_PUBLIC_DOCS]
    A --> F5[05_GOVERNANCE_AND_PROTOCOL_UPDATES]
    A --> F6[06_RATIFICATION_WORKSHOP]
    A --> F10[10_METADATA_AND_LOGS]
    A --> F99[99_REPOSITORY_METADATA]
    A --> D[DECISION_LOG]
    A --> RT[RED_TEAM]

    C --> C1[FUNDING.yml]
    C --> C2[workflows]

    H --> H1[BUILD-YOUR-OWN-IAS.md]
    H --> H2[Gerbers]
    H --> H3[IAS_KiCad]

    F4 --> F4G[Governance<br/>28 files]
    F4 --> F4T[Technical<br/>9 files]

    D[DECISION_LOG<br/>15 files]:::log
    RT[RED_TEAM<br/>4 files]:::redteam

    classDef log fill:#ffeaa7,stroke:#333
    classDef redteam fill:#ff7675,stroke:#333
    style A fill:#2d2d2d,color:#fff,stroke:#00ff00,stroke-width:3px
