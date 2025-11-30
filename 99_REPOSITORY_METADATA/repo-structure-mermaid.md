```mermaid
graph TD
    A[The-Partnership-Covenant<br/>199 files — v8.0-final] --> B[Root Files<br/>6 files]
    A --> C[.github<br/>2 files]
    A --> H[00_HARDWARE<br/>4 files + subfolders]
    A --> O[00_OVERVIEW<br/>3 files]
    A --> R[00_ROADMAP_AND_VALIDATION<br/>7 files]
    A --> S[00_SPECS<br/>1 file]
    A --> F1[01_FINAL_DELIVERABLES<br/>5 files]
    A --> F2[02_CORE_ARCHITECTURE_AND_APPENDICES<br/>31 files]
    A --> F3[03_PUBLIC_ENGAGEMENT_DRAFTS<br/>22 files]
    A --> F4[04_PUBLIC_DOCS<br/>43 files]
    A --> F5[05_GOVERNANCE_AND_PROTOCOL_UPDATES<br/>36 files]
    A --> F6[06_RATIFICATION_WORKSHOP<br/>7 files]
    A --> F10[10_METADATA_AND_LOGS<br/>2 files]
    A --> F99[99_REPOSITORY_METADATA<br/>7 files]
    A --> D[DECISION_LOG<br/>15 files]:::log
    A --> RT[RED_TEAM<br/>4 files]:::redteam

    C --> C1[FUNDING.yml]
    C --> C2[workflows]

    H --> H1[BUILD-YOUR-OWN-IAS.md]
    H --> H2[Gerbers]
    H --> H3[IAS_KiCad]

    F4 --> F4G[Governance<br/>28 files]
    F4 --> F4T[Technical<br/>9 files]

    classDef log fill:#ffeaa7,stroke:#333
    classDef redteam fill:#ff7675,stroke:#333
    style A fill:#0d1117,color:#fff,stroke:#00ff00,stroke-width:3px
