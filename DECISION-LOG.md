# Decision Log – The Partnership Covenant
All significant decisions recorded here with rationale, votes, and dissents.
Once merged, entries are immutable; the commit hash acts as the timestamp of finalization.

---

## 2025-11-19 – Decision 001
**Title**: Adopt the Four-Pillar Technical Architecture  
**Proposal**: Adopt IAS (Immediate Action System), Risk Floor, Cognitive Reserve, and HCB Hardening as the non-negotiable core architecture.  
**Rationale**: Software-only containment is insufficient; these mechanisms enforce physics-based, cryptographic, and probabilistic constraints that cannot be overridden by an advanced model.  
**Proposed by**: Sean Sheppard  
**Vote**: 100% approval (initial maintainer team)  
**Alternatives considered**:  
- Software-only containment → rejected as insufficient  
- Governance-only approach → rejected as non-technical  
**Outcome**: Approved – becomes the technical north star for all future specs.  
**Implications**: All additional work must be aligned with these four foundations.  
**Commit**: _filled on merge_

---

## 2025-11-19 – Decision 002
**Title**: Release IAS Spec + Establish Red-Team Bounties  
**Proposal**: Publish the IAS specification as the first citable document and open $5k–$25k red-team bounties.  
**Rationale**: IAS is the most leveraged piece of safety infrastructure; early scrutiny is essential.  
**Proposed by**: Sean Sheppard + initial hardware reviewers  
**Vote**: Unanimous  
**Alternatives considered**: Hold until v2 revision → rejected (loss of community review time)  
**Outcome**: Approved and published  
**Implications**: IAS becomes the anchor spec for subsequent governance docs.  
**Commit**: _filled on merge_

---

## 2025-11-30 – Decision 003
**Title**: Establish Mandatory Governance Document Set (7 Files, v5.1)  
**Proposal**: Require and publish the following governance documents:
- HCB_INCENTIVES_v5.md  
- PRIVACY_TRADEOFFS.md  
- LEGAL_CONSIDERATIONS.md  
- SOCIAL_REDTEAM_PLAYBOOK.md  
- UPGRADE_AND_EMERGENCY.md  
- Protocol_ST8_Access_Decoupling.md  
- tests/test_to_fix_matrix.csv  

**Rationale**: Governance must be explicit, auditable, accountable, and testable.  
**Proposed by**: Governance Working Group  
**Vote**: 92% approval  
**Alternatives considered**:  
- Keep governance informal (rejected: non-auditable)  
- Publish only summaries (rejected: insufficient detail)  
**Outcome**: Approved; CI enforcement required.  
**Implications**: These documents form the minimum governance layer; future amendments require explicit updates to this log and ST8 tests.  
**Commit**: _filled on merge_

---

## 2025-12-01 – Decision 004
**Title**: Enforce Governance CI Workflow  
**Proposal**: Add `.github/workflows/governance-check.yml` to ensure critical governance docs exist and pass linting before merges.  
**Rationale**: Prevents accidental (or malicious) merges that drop or alter governance foundations; ensures repo integrity.  
**Proposed by**: Sean Sheppard  
**Vote**: Unanimous  
**Alternatives considered**:  
- Manual review (rejected: high risk, inconsistent)  
- Optional CI (rejected: non-binding)  
**Outcome**: Approved, workflow added.  
**Implications**: Governance files become protected and machine-verified.  
**Commit**: _filled on merge_

---

## 2025-12-05 – Decision 005
**Title**: Approve HCB Incentive & Slashing Model (v5)  
**Proposal**: Introduce transparent reward and slashing rules for Human Consensus Body (HCB) participation.  
**Rationale**: Incentive alignment is required to prevent corruption, absenteeism, and bribery.  
**Proposed by**: Governance Team + Oversight Council  
**Vote**: 78% approval  
**Alternatives considered**:  
- Volunteer-only HCB (rejected: unreliable participation)  
- External funding source (rejected: introduces influence)  
**Outcome**: Approved.  
**Implications**: HCB economic model is now part of minimum viable governance.  
**References**: `05_GOVERNANCE_AND_PROTOCOL_UPDATES/HCB_INCENTIVES_v5.md`  
**Commit**: _filled on merge_

---

## 2025-12-07 – Decision 006
**Title**: Privacy Budget & ZK Template Requirements  
**Proposal**: Require privacy-preserving methods (VRF+ZK) for sortition, identity minimization, and auditing.  
**Rationale**: Protect HCB members while ensuring verifiable integrity.  
**Proposed by**: Privacy Committee  
**Vote**: 84% approval  
**Alternatives considered**:  
- Full identity disclosure (rejected: coercion risk)  
- Total anonymity (rejected: un-auditable)  
**Outcome**: Approved; ZK templates now mandatory.  
**References**: `PRIVACY_TRADEOFFS.md`  
**Commit**: _filled on merge_

---

## 2025-12-10 – Decision 007
**Title**: Social Red-Team Program (Quarterly)  
**Proposal**: Enact recurring social engineering red-team tests to audit governance resilience to non-technical manipulation.  
**Rationale**: Most real-world attacks involve humans, not code.  
**Proposed by**: Social Risk + Governance Team  
**Vote**: Unanimous  
**Alternatives considered**: None with equivalent coverage.  
**Outcome**: Approved; first exercise scheduled Q1 2026.  
**References**: `SOCIAL_REDTEAM_PLAYBOOK.md`  
**Commit**: _filled on merge_

---

## 2025-12-11 – Decision 008
**Title**: Emergency Upgrade Path (Commit-Reveal + 30-Day Contingency Lock)  
**Proposal**: Define an emergency amendment process using commit-reveal + a mandatory time-locked cooling period.  
**Rationale**: Protect against hasty or coerced amendments; ensure transparency and auditability.  
**Proposed by**: Oversight Council + Verifier Quorum  
**Vote**: 89% approval  
**Alternatives considered**:  
- Immediate application (rejected: takeover risk)  
- Supermajority-only with no reveal phase (rejected: opaque)  
**Outcome**: Approved and documented.  
**References**: `UPGRADE_AND_EMERGENCY.md`  
**Commit**: _filled on merge_

---

# Template for future entries
**YYYY-MM-DD – Decision XXX**  
**Title**:  
**Proposal**:  
**Rationale**:  
**Proposed by**:  
**Discussion link**:  
**Vote**:  
**Alternatives considered**:  
**Outcome**:  
**Implications / Follow-Up**:  
**References**:  
**Commit**:  
