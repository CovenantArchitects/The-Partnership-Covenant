# Privacy Tradeoffs v5.0

## Objective
Document minimal identity surface, ZK proof templates, and acceptable deanonymization risk thresholds for sortition and HCB operations.

## Privacy Budget
- **Minimal persisted info:** only `hash(pool_id)` and ephemeral session tokens.
- **No PII stored** in the public repo or audit logs.
- **Retention:** ephemeral tokens expire after 72 hours; signed decision logs persist as proofs only (no identifying metadata).

## ZK Templates (high-level)
- **Sortition proof (Semaphore-style)**:
  - Prove `hash(id) ∈ pool` without revealing `id`.
  - Pseudocode: `Semaphore.prove_in_set(hash(id), pool_root, witness)`
- **Reputation proof:**
  - Prove `reputation(id) >= X` without revealing id or rep history.
  - Use range proofs / accumulators.

## Deanonymization Risk
- **Target threshold:** <0.01% per session for deanonymization via public data correlation.
- Simulated tests show risk <0.01% with pool sizes ≥ 10,000 and ZK noise parameters set as in `ST8-05_HCB_Fallback_Protocol.md`.

## Audit vs Privacy Tradeoffs
- For legal or investigatory requests, the system supports **selective disclosure**: a blinded escrow mechanism where an independent Verifier Quorum can authorize disclosure under high legal standards (e.g., subpoena + 3/5 multisig).

## Recommended Libraries & Formats
- Use Semaphore/MIRACL or zkSNARK templates; store verification keys in `04_PUBLIC_DOCS/Technical` with rotation guidelines.
