```mermaid
graph TD
    A[The-Partnership-Covenant (193 Files)] --> B1[Root Files: 6];

    A --> C0[.github/ (2)];
    C0 --> C0A(FUNDING.yml);
    C0 --> C0B[workflows/ (1)];

    A --> C1[00_HARDWARE/ (3)];
    C1 --> C1A[Gerbers/ (1)];
    C1 --> C1B[IAS_KiCad/ (2)];

    A --> C2[00_OVERVIEW/ (2)];
    A --> C3[00_ROADMAP_AND_VALIDATION/ (7)];
    C3 --> C3A[ST8_UPDATE_PACKAGE/ (4)];

    A --> C4[00_SPECS/ (1)];
    A --> C5[01_FINAL_DELIVERABLES/ (5)];
    A --> C6[02_CORE_ARCHITECTURE_AND_APPENDICES/ (31)];
    A --> C7[03_PUBLIC_ENGAGEMENT_DRAFTS/ (22)];

    A --> C8[04_PUBLIC_DOCS/ (43)];
    C8 --> C8A[Governance/ (28)];
    C8 --> C8B[Technical/ (9)];
    C8 --> C8C[Templates/ (2)];
    C8A --> C8A1[Cygnus_Covenant_Governance/ (10)];
    C8A1 --> C8A1A[01_Access_Pillar (Phoenix)/ (4)];
    C8A1 --> C8A1B[02_Infrastructure_Pillar (Cygnus)/ (3)];
    C8A1 --> C8A1C[03_Model_Pillar (Orion)/ (3)];

    A --> C9[05_GOVERNANCE_AND_PROTOCOL_UPDATES/ (36)];
    C9 --> C9A[tests/ (1)];
    C9 --> C9B[v5.1-docs/ (1)];

    A --> C10[06_RATIFICATION_WORKSHOP/ (7)];
    A --> C11[10_METADATA_AND_LOGS/ (2)];
    A --> C12[99_REPOSITORY_METADATA/ (7)];
    A --> C13[DECISION_LOG/ (15)];
    A --> C14[RED_TEAM/ (4)];

    style A fill:#f9f,stroke:#333,stroke-width:2px
    style C8A1 fill:#c7f3e6,stroke:#3C3,stroke-width:1px
    style C13 fill:#ffeaa7,stroke:#333,stroke-width:1px
    style C14 fill:#ff7675,stroke:#333,stroke-width:1px
