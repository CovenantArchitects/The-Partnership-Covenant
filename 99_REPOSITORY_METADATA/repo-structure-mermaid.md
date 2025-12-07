```mermaid
%% Mermaid Repo Structure — Root Directory + .github
classDef updated fill:#ffebee,stroke:#c62828,stroke-width:2px;
classDef newFile fill:#e8f5e8,stroke:#2e7d32,stroke-dasharray:5 5;

graph TD
ROOT["The-Partnership-Covenant v9.0_Final — 245 files"]
R1["Root Directory — 9 files"]
BUILD["BUILD-YOUR-OWN-IAS.md"]
CONTRIB["CONTRIBUTING.md"]:::updated
LICENSE["LICENSE"]:::newFile
MODELS["FROM_THE_MODELS.md"]
FUTURE["FUTURE_WORK.md"]
QUICK["QUICK-START.md"]
README["README.md"]:::updated
SUPPORT["Support_Us.md"]

ROOT --> R1
R1 --> BUILD
R1 --> CONTRIB
R1 --> LICENSE
R1 --> MODELS
R1 --> FUTURE
R1 --> QUICK
R1 --> README
R1 --> SUPPORT

GH[".github — 2 files"]
FUNDING["FUNDING.yml"]
WORKFLOWS["workflows/"]
GOVCHECK["governance-check-simple.yml"]

ROOT --> GH
GH --> FUNDING
GH --> WORKFLOWS
WORKFLOWS --> GOVCHECK
