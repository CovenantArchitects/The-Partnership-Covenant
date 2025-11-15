# **Threat and Risk Model (TRM)**

The Partnership Covenant  
Version 1.0 — November 2025

## **1\. Introduction and Scope**

This Threat and Risk Model (TRM) identifies the primary, high-impact risks that threaten the foundational integrity and mission of The Partnership Covenant. All governance structures, policies (including the TSC Charter), and technical standards are designed explicitly to mitigate these specific threats.

Risk assessment is based on a three-axis score: **Impact (I)**, **Likelihood (L)**, and **Mitigation Gap (M)**. All scores are from 1 (Low) to 5 (Critical).

## **2\. Critical Governance Risks (Category A)**

These risks threaten the organizational structure and decision-making integrity, directly undermining all Four Pillars.

| Risk ID | Risk Name | Description | Pillars Violated | I/L/M | Mitigation Strategy |
| :---- | :---- | :---- | :---- | :---- | :---- |
| **A-01** | **Governance Capture** | A single entity, coalition, or institutional partner gains control of the TSC, compromising independence and impartiality. | All Four | 5/4/5 | TSC Selection Policy (Rotation/CoI), Veto Authority, public D\&I requirements. |
| **A-02** | **Policy Drift/Relaxation** | Gradual, subtle erosion or relaxation of core commitment standards (e.g., easing PII collection rules or reducing audit frequency) over time. | Transparency, Enforcement | 4/3/4 | Immutability of constitutional files (TSC Charter, TRM), public 30-day amendment period. |
| **A-03** | **Enforcement Failure** | Decisions and attestations made by the TSC or WGs are not cryptographically enforced or are ignored by core infrastructure operators. | Enforcement | 5/2/3 | Mandatory cryptographic signing of all decision logs (DECISION\_LOG\_TEMPLATE.md); hard-coded system checks. |
| **A-04** | **CoI Cover-up** | Failure to disclose or actively hiding conflicts of interest among key TSC or WG leadership, leading to biased technical decisions. | Algorithmic Justice, Transparency | 4/3/5 | Strict CoI Policy (disqualification), independent Ethics Review Board (ERB) authority. |

## **3\. Core Technical and Protocol Risks (Category B)**

These risks threaten the reliability, security, and integrity of the underlying technical standards and ledger.

| Risk ID | Risk Name | Description | Pillars Violated | I/L/M | Mitigation Strategy |
| :---- | :---- | :---- | :---- | :---- | :---- |
| **B-01** | **Protocol Subversion** | Introduction of technical code that covertly bypasses the provenance\_schema.json requirements (e.g., adding hidden metadata fields or changing hashing algorithms). | Provenance, Enforcement | 5/3/5 | Mandatory DSAC submission/review for all core changes; dual-signature code merging. |
| **B-02** | **Schema Breakage** | An approved change to the core schema is found to be non-backward compatible, leading to mass corruption of historical provenance data. | Provenance, Deep Safety | 3/4/2 | DSAC compatibility check; staged deployment and immutable archival of previous schema versions. |
| **B-03** | **Cryptographic Compromise** | The primary cryptographic primitive used for signing attestations is compromised (e.g., discovered vulnerability or key leakage). | Transparency, Enforcement | 5/1/2 | Multi-signature requirements; regular cryptographic rotation schedules; hardware security modules (HSM) for signing keys. |

## **4\. Societal and Algorithmic Risks (Category C)**

These risks relate to the output quality, fairness, and safety of models and data governed by the Covenant.

| Risk ID | Risk Name | Description | Pillars Violated | I/L/M | Mitigation Strategy |
| :---- | :---- | :---- | :---- | :---- | :---- |
| **C-01** | **Algorithmic Drift/Bias** | Technical standards permit the subtle inclusion or aggregation of data that introduces or amplifies disproportionate harm over time. | Algorithmic Justice, Deep Safety | 4/4/4 | Mandatory Algorithmic Justice Assessment in the DSAC Template; automated bias testing gates in CI/CD pipelines. |
| **C-02** | **PII Exposure via Metadata** | Technical standards, despite PII rules, allow for the deanonymization of data subjects through the composition of non-PII metadata fields. | Transparency | 4/3/3 | Expert review of all new metadata requirements; k-anonymity checks on aggregate metadata. |
| **C-03** | **Black Box Complexity** | Complexity in the system makes the process of verification and audit prohibitively expensive or time-consuming, effectively blocking external transparency. | Transparency | 3/4/2 | Commitment to simplified, open-source auditing tools; formal commitment to explainability in the CONTRIBUTING.md. |

## **5\. Risk Review and Update Cycle**

This TRM shall be formally reviewed and updated by the TSC at least **annually**, or immediately following any event scoring 4 or 5 on the Impact (I) axis. Any amendment must follow the Charter Amendment process outlined in the TSC Charter.