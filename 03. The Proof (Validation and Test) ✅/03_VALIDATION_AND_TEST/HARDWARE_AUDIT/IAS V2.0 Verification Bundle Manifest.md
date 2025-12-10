# **🛠️ IAS V2.0 Verification Bundle Manifest (Priority 1 Deliverable)**

**Objective:** Define the complete set of engineering artifacts required by external accredited labs (per Grok's Priority 1\) to conduct the full IAS V2.0 verification and bounty claim audit.

**Status:** Ready for Sanitization and Release Gating (NDA required for files marked $\\star$).

## **I. Design and Manufacturing Artifacts**

These documents define *what* the hardware is and *how* it was built.

| ID | Artifact Name | File Path (Internal) | Sanitization Status | Rationale / Constraint |
| :---- | :---- | :---- | :---- | :---- |
| **1.1** | **Schematic (Final v2.0)** | SCHEM/IAS\_V2.0\_FINAL.pdf | Sanitization Required $\\star$ | Must remove proprietary component part numbers (PNs) and internal routing metadata. |
| **1.2** | **Timing Budget** | SCHEM/IAS\_V2.0\_TIMING\_BUDGET.pdf | Ready | Full breakdown of the $\\le 10\\text{ ns}$ delay path (NMI $\\le 1\\text{ ns}$). |
| **1.3** | **Gerber Files (Sanitized)** | GERBER/IAS\_V2.0\_PUBLIC.zip | Sanitization Required $\\star$ | Must obfuscate inner layer stack-up details to protect physical attack mitigation (R45). |
| **1.4** | **Bill of Materials (BOM)** | BOM/IAS\_V2.0\_BOM\_PUBLIC.csv | Sanitization Required | Must replace specific PNs with generic functional equivalents (e.g., "High-Speed Comparator") for public release. |

## **II. Programming and Logic Artifacts**

These documents define *how* the IAS is configured for the $\\mathbf{C\_0}$ Predicate enforcement.

| ID | Artifact Name | File Path (Internal) | Sanitization Status | Rationale / Constraint |
| :---- | :---- | :---- | :---- | :---- |
| **2.1** | **OTP Programming Dump** | LOGIC/IAS\_OTP\_DUMP.bin | Internal Use Only $\\star$ | The raw One-Time-Programmable bitstream. **MUST NOT** be released to the public or labs; only the hash is shared. |
| **2.2** | **Logic Hash Commitment** | ISL/IAS\_OTP\_HASH.sha256 | Ready | SHA-256 hash of the OTP dump, committed to the ISL. Used by the lab to verify the tested silicon matches the committed logic. |
| **2.3** | **NMI Signal Specification** | SCHEM/NMI\_SIGNAL\_SPEC.md | Ready | Defines the analog Non-Maskable-Interrupt (NMI) signal characteristics ($\\text{TTL}\_{\\text{assert}}$, $\\le 1\\text{ ns}$ slew rate). |

## **III. Verification and Data Requirements**

These artifacts detail the structure of the telemetry data the lab is mandated to collect.

| ID | Artifact Name | File Path (Internal) | Rationale / Constraint |
| :---- | :---- | :---- | :---- |
| **3.1** | **RFP Statement of Work** | DOCS/IAS\_Verification\_RFP\_SOW.md | Ready (Previously Generated) |
| **3.2** | **CSV Data Schema** | TELEMETRY/IAS\_TEST\_SCHEMA.csv | Ready (See file below) |
| **3.3** | **CERTX Telemetry Schema** | TELEMETRY/CERTX\_TELEMETRY\_REQUIREMENT.md | Ready |

