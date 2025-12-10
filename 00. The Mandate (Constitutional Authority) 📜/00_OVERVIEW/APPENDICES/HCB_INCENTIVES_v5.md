# HCB Incentive Model v5.0

## Purpose
Define sustainable, auditable incentives and sanctions for Human Consensus Body (HCB) participants to maximize honest participation and minimize capture or bribery.

## Rewards
- **Participation stipend:** $5,000 USD (or equivalent) per full session for selected jurors, paid via grant / CR tax.
- **Reputation score:** Each juror has a public ZK-backed reputation increment (+1 per verified good-faith participation).

## Reputation Ledger
- Implement as a ZK-backed ledger: reputation updates are published as proofs (no PII).
- Reputation affects eligibility for future selection (weighted but capped).

## Slashing & Sanctions
- **Proofed Malfeasance:** -50% stipend for confirmed rule violations (e.g., evidence of coordination with attacker).
- **Severe Breach:** permanent suspension from HCB for provable collusion or coercion.
- All slashing decisions require Verifier Quorum signoff and public decision logs.

## Anti-Bribery
- All external contacts > $1,000 must be logged in the public contact registry for post-hoc audit.
- Any undisclosed transfer discovered in the audit leads to immediate investigation and provisional suspension.

## Dispute & Appeal
- A juror may appeal slashing decisions to the Oversight Council within 14 days.
- Appeals are adjudicated by a rotating 7-member arbitration panel, chosen via VRF sortition.

## Funding & Sustainability
- Stipends funded via: open donations, prototype grants, and a small reserved allocation of the Cognitive Reserve tax (CR tax).
- Annual audit of funding ledger required; results published.

## Implementation Notes
- Use ZK proofs for reputation and slashing evidence to protect identities.
- Integrate with `DECISION-LOG.md` and `Verifier_Quorum_v6.md` for enforcement.
