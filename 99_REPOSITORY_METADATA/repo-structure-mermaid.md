```mermaid
graph TD
    A[The-Partnership-Covenant<br>227 Files] --> F1[BUILD_YOUR_OWN_IAS.md]
    A --> F2[CERN-OHL-S-2.0.md]
    A --> F3[CONTRIBUTING.md]
    A --> F4[FUTURE_WORK.md]
    A --> D0[.github]
    A --> D1[00_HARDWARE]
    A --> D2[00_OVERVIEW]
    A --> D3[00_ROADMAP_AND_VALIDATION]
    A --> D4[01_FINAL_DELIVERABLES]
    A --> D5[02_CORE_ARCHITECTURE_AND_APPENDICES]
    A --> D6[03_PUBLIC_ENGAGEMENT_DRAFTS]
    A --> D7[04_PUBLIC_DOCS]
    A --> D8[05_GOVERNANCE_AND_PROTOCOL_UPDATES]
    A --> D9[06_RATIFICATION_WORKSHOP]
    A --> D10[DECISION_LOG]
    A --> D11[RED_TEAM]
    A --> D12[99_REPOSITORY_METADATA]
    A --> D13[00_SPECS]
    A --> D14[10_METADATA_AND_LOGS]

    D0 --> D0_1[workflows]
    D1 --> D1_1[IAS_VQ_Physical_Protocol_v8.2.md]
    D1 --> D1_2[IAS-v1.3-Redesign-Mandate.md]
    D7 --> D7_1[Governance]
    D7 --> D7_2[Technical]
    D7_1 --> D7_1_1[Cygnus_Covenant_Governance]
    D7_1_1 --> D7_1_1_1[01_Access_Pillar Phoenix]
    D7_1_1 --> D7_1_1_2[02_Infrastructure_Pillar Cygnus]
    D7_1_1 --> D7_1_1_3[03_Model_Pillar Orion]
    D3 --> D3_1[ST8_UPDATE_PACKAGE]
    D8 --> D8_1[tests]
    D8 --> D8_2[v5.1-docs]

    classDef highlight fill:#ff7675,color:#fff,stroke:#333
    class D10,D11 highlight
    style A fill:#0d1117,color:#fff,stroke:#00ff00,stroke-width:3px
