```mermaid
%% The-Partnership-Covenant Repository Structure — Final v9.0 (245 files)

classDef updated fill:#ffebee,stroke:#c62828,stroke-width:2px;
classDef newFile fill:#e8f5e8,stroke:#2e7d32,stroke-dasharray: 5 5;

graph TD
    ROOT[The-Partnership-Covenant<br/><small>v9.0_Final — 245 files</small>]

    %% Root
    ROOT --> R1[Root Directory<br/>9 files]
    R1 --> LICENSE[LICENSE]:::newFile
    R1 --> README[README.md]:::updated
    R1 --> CONTRIBUTING[CONTRIBUTING.md]:::updated

    %% Main Folders
    ROOT --> HW[00_HARDWARE<br/>9 files]
    ROOT --> OV[00_OVERVIEW<br/>8 files]
    ROOT --> RV[00_ROADMAP_AND_VALIDATION<br/>8 files]
    ROOT --> SP[00_SPECS<br/>2 files]
    ROOT --> FD[01_FINAL_DELIVERABLES<br/>12 files]:::updated
    ROOT --> CA[02_CORE_ARCHITECTURE_AND_APPENDICES<br/>44 files]:::updated
    ROOT --> PE[03_PUBLIC_ENGAGEMENT_DRAFTS<br/>23 files]
    ROOT --> PD[04_PUBLIC_DOCS<br/>46 files]:::updated
    ROOT --> GP[05_GOVERNANCE_AND_PROTOCOL_UPDATES<br/>47 files]:::updated
    ROOT --> RW[06_RATIFICATION_WORKSHOP<br/>7 files]
    ROOT --> ML[10_METADATA_AND_LOGS<br/>2 files]
    ROOT --> RM[99_REPOSITORY_METADATA<br/>7 files]:::updated
    ROOT --> DL[DECISION_LOG<br/>25 files]:::updated
    ROOT --> RT[RED_TEAM<br/>7 files]
    ROOT --> GH[.github<br/>2 files]

    %% New & Updated Files
    subgraph "New & Updated Files"
        FD --> FD1{The_Partnership_Covenant_V4.1.1.md}:::newFile
        CA --> CA1{CORE_DIRECTIVES.md}:::newFile
        CA --> CA2{ENFORCEMENT_LAYER.md}
        PD --> PD1{CERTX_TELEMETRY_PROTOCOL.md}:::newFile
        PD --> PD2{Governance/SEMANTIC_PROTOCOL.md}:::newFile
        GP --> GP1{FINAL_v4.2_REPORT.md}:::newFile
        RM --> RM1{repo-structure-txt.md}:::newFile
        DL --> DL1{DECISION_LOG.md}:::newFile
        RT --> RT1{TEST_LOG_R41-R44.md}:::newFile
        RT --> RT2{SOCIAL_REDTEAM_PLAYBOOK_v6.0.md}:::newFile
    end

    click ROOT "https://github.com/CovenantArchitects/The-Partnership-Covenant"
