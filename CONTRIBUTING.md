# Contributing to The Partnership Covenant

Thank you for your interest in helping build a constitutional operating system for superintelligence.  
This document explains how to get involved, how decisions are made, and how contributions of all kinds are reviewed, tested, merged, and archived.

The Partnership Covenant is a **high-assurance, open, auditable governance and technical architecture** designed to bound, direct, and constrain superintelligent systems through physics, cryptography, and structured human oversight.

---

## Table of Contents
- [What We’re Building](#what-were-building)
- [Ways to Contribute](#ways-to-contribute)
- [Contribution Levels](#contribution-levels)
- [The Four Technical Pillars](#the-four-technical-pillars)
- [Getting Started](#getting-started)
- [How Contributions Are Reviewed](#how-contributions-are-reviewed)
- [Governance & Decision Process](#governance--decision-process)
- [Security + Responsible Disclosure](#security--responsible-disclosure)
- [Community Norms](#community-norms)
- [Getting in Touch](#getting-in-touch)

---

# What We’re Building

The Partnership Covenant rests on **four non-negotiable primitives** that cannot be implemented with software safeguards alone:

1. **Immediate Action System (IAS)**  
   A physics-based, 10 ns, out-of-band power-cut tripwire.

2. **Stochastic Risk Floor**  
   Enforced, irreducible uncertainty to preserve human agency.

3. **Cognitive Reserve**  
   Physically partitioned compute + irreversible IP boundaries.

4. **Human Consensus Body (HCB) Hardening**  
   A coercion-resistant, ZK-verifiable form of global sortition.

The project is currently in the **hardening phase**:  
turning designs into specs → reference circuits → governance protocols → verification tests.

---

# Ways to Contribute

All skills are welcome. High-impact contributions include:

### 🛠️ Technical / Engineering
- Hardware tripwire design (IAS)
- Formal verification / stochastic modeling
- Risk Floor algorithm refinement
- Cognitive Reserve one-way channel analysis
- Cryptographic protocol design (ZK, VRF, SSSS)

### 📘 Documentation & Governance
- Fix inaccuracies or unclear language in governance docs
- Improve or extend protocol documentation
- Draft new test cases for `/tests/test_to_fix_matrix.csv`
- Propose process improvements

### 🧠 Research
- Threat models, red-team writeups
- Stress tests against v5.1 governance assumptions
- Formal safety proofs or failure mode analysis

### 🌍 Non-technical contributions
- Translations
- Non-technical summaries
- Visual diagrams of the system
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
→ Requires domain-expert review.

### **Level 4 – Governance Changes**
Anything touching:  
- `05_GOVERNANCE_AND_PROTOCOL_UPDATES/`  
- `/constitution`  
- `/technical/v*/*.md`  
- or `/DECISION-LOG.md`

→ Requires public discussion + consensus + recorded decision.

---

# The Four Technical Pillars (Priority Areas)

If you want maximal impact, focus here:

### 1. **IAS – Immediate Action System (Hardware)**
- Tripwire architecture
- Component selection
- Tamper-evidence validation
- Physical one-way signaling

### 2. **Stochastic Risk Floor**
- Randomness generation
- Noise shaping
- Proof-of-randomness audit trails
- Extinction Immunity Trigger analysis

### 3. **Cognitive Reserve**
- IP isolation mechanisms
- Compute cuts / “energy budget partitioning”
- One-way message channel protocol

### 4. **HCB Hardening**
- Zero-knowledge sortition (VRF + ZK)
- Shamir’s Secret Sharing keying
- Deliberation protocols
- Anti-coercion designs

---

## Getting Started

Before opening a PR, please:

1. **Read the project overview** in [README.md](README.md) — covers the core mission, pillars, and "Get Involved" paths.
2. **Review the technical specs** in [04_PUBLIC_DOCS/Technical/ias-spec.md](04_PUBLIC_DOCS/Technical/ias-spec.md) — details the Immediate Action System (IAS) architecture, tamper detection, and hardware constraints.
3. **Check the decision logs** in [DECISION_LOG/](DECISION_LOG/) — see recent ratifications and open threads (e.g., Directive XXIV on anti-coercion).
4. **Fork the repo**, create a feature branch (`git checkout -b feature/your-change`), and submit a PR against `main`.
5. **Test your changes** — run the governance CI (`/.github/workflows/governance-check-simple.yml`) locally if possible, or just push and let Actions validate.

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

### 🔁 **Iteration**
Most PRs go through 1–2 rounds of refinement.

### ✅ **Merge Criteria**
A PR merges when:
- It has at least one maintainer approval  
- No outstanding “changes requested” reviews remain  
- All Github CI checks pass  
- If governance-related: a Decision Log entry is included or referenced

All significant merges are archived in `/DECISION-LOG.md`.

---

# Governance & Decision Process

### **Day-to-Day Maintainer Governance**
- Project lead (BDFL model): **Sean Sheppard**
- Maintainer group: technical + governance reviewers

### **Major Governance Changes**
1. Public RFC  
2. 7-day discussion period  
3. Maintainer vote  
4. Decision logged in `/DECISION-LOG.md` (immutable)

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
