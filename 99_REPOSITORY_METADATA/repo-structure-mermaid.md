```mermaid
graph TD
%% classDefs must be inside the Mermaid block
classDef updated fill:#ffebee,stroke:#c62828,stroke-width:2px;
classDef newFile fill:#e8f5e8,stroke:#2e7d32,stroke-dasharray:5 5;


ROOT["The-Partnership-Covenant v9.0_Final — 245 files"]

%% Root Directory
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

%% .github
GH[".github — 2 files"]
FUNDING["FUNDING.yml"]
WORKFLOWS["workflows/"]
GOVCHECK["governance-check-simple.yml"]

ROOT --> GH
GH --> FUNDING
GH --> WORKFLOWS
WORKFLOWS --> GOVCHECK

%% 00_HARDWARE
HW["00_HARDWARE — 9 files"]
HW1["BUILD-YOUR-OWN-IAS.md"]
HW2["IAS-v1.3-Redesign-Mandate.md"]
HW3["IAS_Hardware_Bounty_Specification_v1.md"]
HW4["IAS_Hardware_Bounty_Specification_v2.0.md"]
HW5["IAS_VQ_Physical_Protocol_v8.2.md"]
HW6["IAS_v2.0_3_Node_Mandate.md"]
GERB["Gerbers/"]
GERB_README["README.md"]
KICAD["IAS_KiCad/"]
BOM["IAS-v1.2-BOM.csv"]
SCH["IAS-v1.2-schematic.pdf"]

ROOT --> HW
HW --> HW1
HW --> HW2
HW --> HW3
HW --> HW4
HW --> HW5
HW --> HW6
HW --> GERB
GERB --> GERB_README
HW --> KICAD
KICAD --> BOM
KICAD --> SCH

%% 00_OVERVIEW
OV["00_OVERVIEW — 8 files"]
AI_BREATH["AI_BREATHING_INTEGRATION.md"]
COV_GEOM["COVENANT_GEOMETRIES_v8.2.1.md"]
SUMMARY["Covenant-Summary-1Pager.md"]
EPF["Distributed Epistemic Filtering Primer.md"]
EXEC["Executive_Summary.md"]
PREPRINT["IAS-preprint-v1.0.pdf"]
MULTI["Multi-Model Adversarial Alignment.md"]
OV_README["README.md"]

ROOT --> OV
OV --> AI_BREATH
OV --> COV_GEOM
OV --> SUMMARY
OV --> EPF
OV --> EXEC
OV --> PREPRINT
OV --> MULTI
OV --> OV_README
