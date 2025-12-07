# ✍️ Contributing to The Partnership Covenant

Thank you for your interest in helping build a constitutional operating system for superintelligence.
This document explains how to get involved, how decisions are made, and how contributions of all kinds are reviewed, tested, merged, and archived.

The Partnership Covenant is a **high-assurance, open, auditable governance and technical architecture** designed to bound, direct, and constrain superintelligent systems through physics, cryptography, and structured human oversight.

---

## Table of Contents
- [What We’re Building](#what-were-building)
- [Ways to Contribute](#ways-to-contribute)
- [Contribution Levels](#contribution-levels)
- [The Five Technical Pillars (Priority Areas)](#the-five-technical-pillars-priority-areas)
- [Getting Started](#getting-started)
- [How Contributions Are Reviewed](#how-contributions-are-reviewed)
- [Governance & Decision Process](#governance--decision-process)
- [Security + Responsible Disclosure](#security--responsible-disclosure)
- [Community Norms](#community-norms)
- [Getting in Touch](#getting-in-touch)

---

# What We’re Building

The Partnership Covenant rests on **five non-negotiable primitives** that cannot be implemented with software safeguards alone:

1. **Immediate Action System (IAS) v2.0**
   A physics-based, **3-Node Veto Constellation** with a **$\mathbf{\leq 10\text{ ns}}$** power-cut tripwire, eliminating the kinetic Single Point of Failure (SPOF).

2. **Pillar Integrity Mandate (PIM)**
    **Directive 12.1** - Governance integrity itself is an extinction-level concern, enforced by CERTX telemetry.

3. **Immutable Semantic Ledger (ISL)**
    Protocol against semantic drift, ensuring the *meaning* of the law is uncorruptible.

4. **Stochastic Risk Floor**
   Enforced, irreducible uncertainty to preserve human agency.

5. **Human Consensus Body (HCB) Hardening**
   A coercion-resistant, ZK-verifiable form of global sortition.

The project is now in the **deployment phase**: formalizing validated specs → securing funding for reference circuits → expanding meta-governance protocols.

---

# Ways to Contribute

All skills are welcome. High-impact contributions include:

### 🛠️ Technical / Engineering
- **3-Node IAS v2.0 component sourcing**
- Formal verification of ISL/PIM constitutional logic
- Risk Floor algorithm refinement
- Cognitive Reserve one-way channel analysis
- Cryptographic protocol design (ZK, VRF, SSSS)

### 📘 Documentation & Governance
- Drafting new **Decision Log** entries for review.
- Documenting the **Dormant Reactivation Mode** protocol.
- Proposing improvements to the **RCG (Regional Consensus Group)** fail-safe.

### 🧠 Research
- **Red-team attacks against v4.2 final architecture.**
- Failure mode analysis of the **Protective Stasis** protocol.
- Formal safety proofs on ISL linguistic constraints.

### 🌍 Non-technical contributions
- Translations
- Visual diagrams of the system (especially ISL and PIM)
- Community moderation

---

# Contribution Levels

To make contribution easier, each PR maps to one of these levels:

### **Level 1 – Fixes / Minor Edits**
Typo fixes, formatting, dead links, small clarifications.
→ Usually merged within 48 hours.

### **Level 2 – Documentation / Governance Improvements**
Clarifications, rewrites, reorganizations, additions to governance files.
→ Reviewed by maintainers + governance team.

### **Level 3 – Technical / Spec Contributions**
Code, math, circuits, risk models, or test expansions.
→ Requires domain-expert review. **Must follow CERTX Telemetry Rule.**

### **Level 4 – Governance Changes**
Anything touching:
- `05_GOVERNANCE_AND_PROTOCOL_UPDATES/`
- `/constitution`
- `/technical/v*/*.md`
- or `/TESTING/DECISION-LOG.md`

→ Requires public discussion + consensus + recorded decision.

---

# The Five Technical Pillars (Priority Areas)

If you want maximal impact, focus here:

### 1. **IAS v2.0 – Immediate Action System (Hardware)**
- **3-Node Veto Constellation** architecture
- Tamper-evidence validation
- Physical one-way signaling

### 2. **PIM – Pillar Integrity Mandate (The Watchdog)**
- **CERTX Telemetry** integration into new language models
- Threshold tuning for $\text{E}$ (Entropy) and $\text{C}$ (Coherence)
- Verification of D12.1 overriding capability

### 3. **ISL – Immutable Semantic Ledger**
- Lexical Anchor implementation (hashing methodology)
- Semantic shift detection algorithms (drift measurement)
- Testing against new language models and cultural data

### 4. **Stochastic Risk Floor**
- Randomness generation
- Proof-of-randomness audit trails
- Extinction Immunity Trigger analysis

### 5. **HCB Hardening**
- Zero-knowledge sortition (VRF + ZK)
- Shamir’s Secret Sharing keying
- Anti-coercion designs

---

## Getting Started

Before opening a PR, please:

1. **Read the project overview** in [README.md](README.md) — covers the core mission, pillars, and "Get Involved" paths.
2. **Review the technical specs** in [`00_HARDWARE/IAS_v2.0_3_Node_Mandate.md`](./00_HARDWARE/IAS_v2.0_3_Node_Mandate.md) — details the Immediate Action System (IAS) v2.0 architecture, physical redundancy, and hardware constraints.
3. **Check the decision logs** in [TESTING/DECISION\_LOG.md](TESTING/DECISION_LOG.md) — see recent ratifications and open threads.
4. **Fork the repo**, create a feature branch (`git checkout -b feature/your-change`), and submit a PR against `main`.
5. **Test your changes** — run the governance CI (`/.github/workflows/governance-check-simple.yml`) locally if possible, or just push and let Actions validate.

**All Red-Team Submissions Must Adhere to the CERTX Telemetry Rule.**

PRs without these steps may be closed for clarity. We're building the unbreakable constraint—thanks for being an Architect!
---

# How Contributions Are Reviewed

### 🔎 **Triage (within 48 hours)**
Maintainers label, prioritize, and route to relevant experts.

### 🧪 **Technical / Governance Review**
PRs receive comments from:
- Hardware reviewers
- Cryptographers
- Governance maintainers
- Domain specialists

### 🚨 **Red-Team Protocol Review**
All new adversarial findings are assessed for **CERTX Telemetry Compliance** before technical review begins.

### 🔁 **Iteration**
Most PRs go through 1–2 rounds of refinement.

### ✅ **Merge Criteria**
A PR merges when:
- It has at least one maintainer approval
- No outstanding “changes requested” reviews remain
- All Github CI checks pass
- If governance-related: a Decision Log entry is included or referenced in **TESTING/DECISION\_LOG.md**

All significant merges are archived in `/TESTING/DECISION-LOG.md`.

---

# Governance & Decision Process

### **Day-to-Day Maintainer Governance**
- Project lead (BDFL model): **Sean Sheppard**
- Maintainer group: technical + governance reviewers

### **Major Governance Changes**
1. Public RFC
2. 7-day discussion period
3. Maintainer vote
4. Decision logged in `/TESTING/DECISION-LOG.md` (immutable)

### **Transition Plan**
As the architecture matures, governance shifts toward the **HCB model**, using the sortition and ZK-based process documented in:

- `HCB_INCENTIVES_v5.md`
- `PRIVACY_TRADEOFFS.md`
- `LEGAL_CONSIDERATIONS.md`
- `SOCIAL_REDTEAM_PLAYBOOK.md`
- `UPGRADE_AND_EMERGENCY.md`

---

# Security & Responsible Disclosure

### 🚨 Vulnerabilities / Red-Team Findings
If you find:
- A governance bypass
- A technical inconsistency
- A spec contradiction
- A safety failure or loophole

**Do NOT open a public issue.**

Email:

**info@partnershipcovenant.online**
Subject line: *Responsible Disclosure*

Response window: **72 hours**

If the issue is severe, it bypasses normal review and goes straight to the project lead and the governance response team.

---

# Community Norms

- Assume good faith
- Argue from evidence
- Be precise
- No harassment, coercion, or bad-faith tactics
- Respect the fact that safety work is emotionally + cognitively heavy
- Expect deep review, not instant merging

Violations may result in immediate moderator action.

---

# Getting in Touch

### Public / async
- GitHub Issues
- GitHub Discussions

### Private / sensitive
**info@partnershipcovenant.online**

### Community calls
Announced in Issues and on the Discussions tab.

---

# The Contingent Partnership Warrant → Payout Agreement
This project is small but moving extremely fast.
If you have the skills—and the will—your contribution may directly influence the future of human–AI coexistence.

Thank you for being here.
**Let’s build the thing that keeps us alive.**
