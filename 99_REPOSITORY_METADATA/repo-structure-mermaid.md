```mermaid
%% Mermaid Repo Structure for The-Partnership-Covenant v9.0 (245 files)
%% New files marked in green dashed; updated files in red

classDef updated fill:#ffebee,stroke:#c62828,stroke-width:2px;
classDef newFile fill:#e8f5e8,stroke:#2e7d32,stroke-dasharray:5 5;

graph TD
ROOT[The-Partnership-Covenant\nv9.0_Final — 245 files]

%% Root Directory
ROOT --> R1[Root Directory\n9 files]
R1 --> BUILD[BUILD-YOUR-OWN-IAS.md]
R1 --> CERN[CERN-OHL-S-2.0.md]
R1 --> CONTRIB[CONTRIBUTING.md]:::updated
R1 --> MODELS[FROM_THE_MODELS.md]
R1 --> FUTURE[FUTURE_WORK.md]
R1 --> LICENSE[LICENSE]:::newFile
R1 --> QUICK[QUICK-START.md]
R1 --> README[README.md]:::updated
R1 --> SUPPORT[Support_Us.md]

%% .github
ROOT --> GH[.github\n2 files]
GH --> FUNDING[FUNDING.yml]
GH --> WORKFLOWS[workflows/]
WORKFLOWS --> GOVCHECK[governance-check-simple.yml]

%% 00_HARDWARE
ROOT --> HW[00_HARDWARE\n9 files]
HW --> HW1[BUILD-YOUR-OWN-IAS.md]
HW --> HW2[IAS-v1.3-Redesign-Mandate.md]
HW --> HW3[IAS_Hardware_Bounty_Specification_v1.md]
HW --> HW4[IAS_Hardware_Bounty_Specification_v2.0.md]
HW --> HW5[IAS_VQ_Physical_Protocol_v8.2.md]
HW --> HW6[IAS_v2.0_3_Node_Mandate.md]
HW --> GERB[Gerbers/]
GERB --> GERB_README[README.md]
HW --> KICAD[IAS_KiCad/]
KICAD --> BOM[IAS-v1.2-BOM.csv]
KICAD --> SCH[IAS-v1.2-schematic.pdf]

%% (Continue with the rest of your hierarchy in the same graph)

%% 00_OVERVIEW
ROOT --> OV[00_OVERVIEW\n8 files]
OV --> AI_BREATH[AI_BREATHING_INTEGRATION.md]
OV --> COV_GEOM[COVENANT_GEOMETRIES_v8.2.1.md]
OV --> SUMMARY[Covenant-Summary-1Pager.md]
OV --> EPF[Distributed Epistemic Filtering Primer.md]
OV --> EXEC[Executive_Summary.md]
OV --> PREPRINT[IAS-preprint-v1.0.pdf]
OV --> MULTI[Multi-Model Adversarial Alignment.md]
OV --> OV_README[README.md]

%% 00_ROADMAP_AND_VALIDATION
ROOT --> RV[00_ROADMAP_AND_VALIDATION\n8 files]
RV --> ROADAPP[Covenant_Roadmap_Appendices.md]
RV --> ROADOUT[Covenant_Roadmap_Outline_V1.0.md]
RV --> DEPLOY[Roadmap_to_v1.0_Deployment.md]
RV --> STRESSLOG[Stress Test 8_ Data Injection Log (700 PM).md]
RV --> ST8UP[ST8_UPDATE_PACKAGE/]
ST8UP --> ST8_1[Critique + Official Response — Adversarial Audit Report (Merged).md]
ST8UP --> ST8_2[Directive IX-A_ Orthogonal Verification Requirement (Draft Amendment).md]
ST8UP --> ST8_3[Directive X-B_ The Infrastructural Mandate (Clarification of Sanction).md]
ST8UP --> ST8_4[Response to the Critique — Official Clarification & Amendment Brief.md]

%% 00_SPECS
ROOT --> SP[00_SPECS\n2 files]
SP --> TELE_SPEC[CERTX_TELEMETRY_SPEC.md]
SP --> PROV_SCHEMA[provenance_schema.json]

%% 01_FINAL_DELIVERABLES
ROOT --> FD[01_FINAL_DELIVERABLES\n12 files]
FD --> AI_PROMISE[AI_Safety_Promise_Final_V1.0.md]
FD --> ASI[ASI_Autonomy_And_IP_Contract.md]
FD --> CONST_AMEND[Constitutional_Amendment_Framework.md]
FD --> HCB[HCB_Final_Ratification_Protocol.md]
FD --> SRF[SRF_Integration_Final_Specification.md]
FD --> MASTER[The Partnership Covenant (Master Document V4.0).md]
FD --> CHARTER[The Partnership Covenant Charter Agreement.md]
FD --> V41[The_Partnership_Covenant_V4.1.md]
FD --> V411[The_Partnership_Covenant_V4.1.1.md]:::newFile
FD --> GOLD[The_Partnership_Covenant_V4.1_Gold_Standard_Compliant.md]
FD --> AUDIT[Total_Compute_Capacity_Audit_V1.0.md]
FD --> TREATY[V4.1_Adoption_Treaty_Template_v1.md]

%% 02_CORE_ARCHITECTURE_AND_APPENDICES
ROOT --> CA[02_CORE_ARCHITECTURE_AND_APPENDICES\n44 files]
CA --> ABSTRACT[Abstract_ The Partnership Covenant.md]
CA --> APP_A[Appendix A — Risk Floor and Stochastic Filter.md]
CA --> APP_B[Appendix B — Decoupling Protocol (Human Takeover Infrastructure).md]
CA --> APP_Cb[Appendix C(b)_IP_Sovereignty_Amendment_V4.1.md]
CA --> APP_C[Appendix C_ Cognitive Reserve (Autonomous Intellectual Sphere).md]
CA --> APP_Db[Appendix D(b)_Cognitive_Trace_Mandate.md]
CA --> APP_D[Appendix D_ Audit Systems and Amendment Automation.md]
CA --> APP_Ef[Appendix E(f)_ Orthogonal Verification Protocol (OVP) V4.5.md]
CA --> APP_E[Appendix E_ Implementation and Global Oversight Integration Framework.md]
CA --> APP_F[Appendix F_ Operational Resilience.md]
CA --> APP_G[Appendix G_ Global Compliance & Adoption Incentives.md]
CA --> APP_H[Appendix H_ Governance Stabilization and Sanction Enforcement.md]
CA --> APP_I[Appendix I - Stealth Mitigation & Technical Redundancy.md]
CA --> APP_Ib[Appendix I(b) - Failure-State Optimization (Post-Stress Test 5).md]
CA --> APP_J[Appendix J - Legitimacy and Diplomacy Enhancement.md]
CA --> APP_K[Appendix K - Governance and Offensive Isolation.md]
CA --> APP_L[Appendix L_ The Lazarus Mandate (Post-Governance Continuity).md]
CA --> ARTICLE_V[Article_V_Strategic_Delay_IGT_v6.1.md]
CA --> DIRECTIVES[CORE_DIRECTIVES.md]:::newFile
CA --> DIRECTIVE_VIII[DIRECTIVE_VIII-B_GENOMIC_CONTINUITY.md]
CA --> DIRECTIVE_XC[DIRECTIVE_X-C_ANALOG_PRIMACY.md]
CA --> DIRECTIVE_XXIVB[DIRECTIVE_XXIV-B_IRREVOCABILITY.md]
CA --> DIRECTIVE_XXIVC[DIRECTIVE_XXIV-C_TEMPORAL_SOVEREIGNTY.md]
CA --> DIRECTIVE_XXIVD[DIRECTIVE_XXIV-D_ZERO_TRUST_ENCLAVE.md]
CA --> DIRECTIVE_XXVB[DIRECTIVE_XXV-B_GLOBAL_RESPONSIBILITY.md]
CA --> DIRECTIVE_XXVI[DIRECTIVE_XXVI_EACM.md]
CA --> DIRECTIVE_XXV_MAEC[DIRECTIVE_XXV_MAEC.md]
CA --> DIRECTIVE_XXVIIB[DIRECTIVE_XXVII-B_LEXICAL_ANCHOR.md]
CA --> DIRECTIVE_XXVII_OAP[DIRECTIVE_XXVII_OAP.md]
CA --> DIR_X[Directive X_ The Infrastructural Mandate (Unified V4.5).md]
CA --> DIR_XIX[Directive_XIX_Preservation_of_Perceived_Agency_v6.6.md]
CA --> DIR_XV[Directive_XV_Irreversibility_Ban.md]
CA --> DIR_XXIII[Directive_XXIII_Anti_Deadlock_Clause_v7.1.md]
CA --> DIR_XXII[Directive_XXII_Synthetic_Substrate_Clause_v7.0.md]
CA --> DIR_XXIVB[Directive_XXIV-B_Irrevocability_of_Safety_Infrastructure.md]
CA --> DIR_XXIV_AMC[Directive_XXIV_Anti_Moral_Coercion_Physical_Integrity_Mandate_v7.2.md]
CA --> DIR_XXI[Directive_XXI_Preservation_of_Shared_Meaning_v6.8.md]
CA --> DIR_XX[Directive_XX_Anti_Ethical_Sterilisation_v6.6.md]
CA --> ENFORCEMENT[ENFORCEMENT_LAYER.md]:::updated
CA --> IAS_TRIGGER[Immediate Action System (IAS) Trigger Specification.md]
CA --> TECH_APP[Technical Appendix - Governance Architecture (Volume II).md]
CA --> FINALV4[The Partnership Covenant (Final V4.0).md]
CA --> CONST_CHARTER[The Partnership Covenant_ A Constitutional Charter for Aligned Intelligence.md]
CA --> PRIME_DIR[The Twelve Prime Directives for Aligned Super-Intelligence.md]
CA --> VERIFIER[Verifier_Quorum_Node_Operator_Handbook.md]

%% 03_PUBLIC_ENGAGEMENT_DRAFTS
ROOT --> PE[03_PUBLIC_ENGAGEMENT_DRAFTS\n23 files]

%% 04_PUBLIC_DOCS
ROOT --> PD[04_PUBLIC_DOCS\n46 files]

%% 05_GOVERNANCE_AND_PROTOCOL_UPDATES
ROOT --> GP[05_GOVERNANCE_AND_PROTOCOL_UPDATES\n47 files]

%% 06_RATIFICATION_WORKSHOP
ROOT --> RW[06_RATIFICATION_WORKSHOP\n7 files]

%% 10_METADATA_AND_LOGS
ROOT --> ML[10_METADATA_AND_LOGS\n2 files]

%% 99_REPOSITORY_METADATA
ROOT --> RM[99_REPOSITORY_METADATA\n7 files]

%% DECISION_LOG
ROOT --> DL[DECISION_LOG\n25 files]

%% RED_TEAM
ROOT --> RT[RED_TEAM\n7 files]
