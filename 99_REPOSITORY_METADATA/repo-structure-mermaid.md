# Repository Structure — Mermaid Diagram
**v8.0-final-full-source — 25 November 2025 — UNKILLABLE**

```mermaid
flowchart TB
    %% Style definitions
    classDef core fill:#ff4500, color:#fff, stroke:#fff
    classDef public fill:#00ff00, color:#000, stroke:#000
    classDef gov fill:#ffd700, color:#000, stroke:#000
    classDef meta fill:#333, color:#fff, stroke:#999

    %% Root
    Root[The-Partnership-Covenant-main]:::core

    %% Core Architecture
    subgraph core_arch ["Core Architecture"]
        direction TB
        Root --> A[.github]
        Root --> B[00_ROADMAP_AND_VALIDATION]
        Root --> C[00_SPECS]
        Root --> D[01_FINAL_DELIVERABLES]
        Root --> E[02_CORE_ARCHITECTURE_AND_APPENDICES]
    end

    %% Public & Technical
    subgraph public_tech ["Public & Technical"]
        direction TB
        Root --> F[03_PUBLIC_ENGAGEMENT_DRAFTS]
        Root --> G[04_PUBLIC_DOCS]:::public
        G --> G1[Governance<br>28 files]
        G --> G2[Technical<br>9 specs + schemas]
        G --> G3[Templates]
    end

    %% Governance & Ratification
    subgraph gov_rat ["Governance & Ratification"]
        direction TB
        Root --> H[05_GOVERNANCE_AND_PROTOCOL_UPDATES<br>39 updates + red-team]:::gov
        Root --> I[06_RATIFICATION_WORKSHOP<br>7 documents]
        Root --> J[DECISION_LOG<br>5 dated logs]
        Root --> K[DECISION-LOG.md]
    end

    %% Metadata
    subgraph metadata ["Metadata"]
        direction TB
        Root --> L[10_METADATA_AND_LOGS]:::meta
        Root --> M[99_REPOSITORY_METADATA]:::meta
        Root --> N[CHANGELOG_v6.8.md]
        Root --> O[CONTRIBUTING.md]
        Root --> P[README.md]
        Root --> Q[Support_Us.md]
    end

    %% Clickable links
    click D "./01_FINAL_DELIVERABLES"
    click E "./02_CORE_ARCHITECTURE_AND_APPENDICES"
    click G "./04_PUBLIC_DOCS"
    click H "./05_GOVERNANCE_AND_PROTOCOL_UPDATES"
    click J "./DECISION_LOG"

    %% Apply core styling to critical folders
    class D,E,G,H,J core
