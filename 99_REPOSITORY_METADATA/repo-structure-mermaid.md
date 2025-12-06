```mermaid
graph TD
    A[The-Partnership-Covenant] --> B(Root: 8 Files)
    A --> C[.github/: 2 Files]
    A --> D(00_HARDWARE/: 9 Files)
    A --> E(00_OVERVIEW/: 8 Files)
    A --> F(00_ROADMAP_AND_VALIDATION/: 8 Files)
    A --> G(00_SPECS/: 2 Files)
    A --> H(01_FINAL_DELIVERABLES/: 12 Files)
    A --> I(02_CORE_ARCHITECTURE_AND_APPENDICES/: 43 Files)
    A --> J(03_PUBLIC_ENGAGEMENT_DRAFTS/: 23 Files)
    A --> K(04_PUBLIC_DOCS/: 45 Files)
    A --> L(05_GOVERNANCE_AND_PROTOCOL_UPDATES/: 41 Files)
    A --> M(06_RATIFICATION_WORKSHOP/: 7 Files)
    A --> N(10_METADATA_AND_LOGS/: 2 Files)
    A --> O(99_REPOSITORY_METADATA/: 7 Files)
    A --> P(DECISION_LOG/: 23 Files)
    A --> Q(RED_TEAM/: 6 Files)

    C --> C1(workflows/)

    D --> D1(Gerbers/)
    D --> D2(IAS_KiCad/)

    F --> F1(ST8_UPDATE_PACKAGE/)

    K --> K1(Governance/)
    K --> K2(Technical/)
    K --> K3(Templates/)
    K1 --> K1_1(Cygnus_Covenant_Governance/)
    K1_1 --> K1_1_1("01_Access_Pillar (Phoenix)/")
    K1_1 --> K1_1_2("02_Infrastructure_Pillar (Cygnus)/")
    K1_1 --> K1_1_3("03_Model_Pillar (Orion)/")

    L --> L1(tests/)
    L --> L2(v5.1-docs/)
