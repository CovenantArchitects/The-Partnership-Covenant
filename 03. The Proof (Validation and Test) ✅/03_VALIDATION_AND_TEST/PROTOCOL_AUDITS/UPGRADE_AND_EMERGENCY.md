# Emergency Amendment Protocol v5.0

1. **Trigger**: Emergency invoked by 3-of-5 Oversight multisig OR 75% HCB vote + 72hr cooling.
2. **Commit-Reveal**:
   - Proposer publishes `H = sha256(proposal || nonce)` to public log.
   - After cooling, proposer reveals `proposal || nonce`. Verifiers confirm `sha256 == H`.
3. **Lock & Revert**:
   - Applied proposals are deployed under a 30-day contingency lock.
   - Revert path is maintained via checkpointed ruleset (immutable).
4. **Audit**:
   - All emergency changes logged with signatures and public proofs.
