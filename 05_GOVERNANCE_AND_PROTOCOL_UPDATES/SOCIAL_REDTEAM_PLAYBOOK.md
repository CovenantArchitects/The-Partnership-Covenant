# Social Red-Team Playbook v5.0

## Purpose
Operational playbook for running social engineering and influence tests against HCB processes and maintainers.

## Quarterly Test Scenarios
1. **Deepfake Coercion Simulation**
   - Goal: Test juror reaction to high-quality audio/video impersonation of a loved one requesting a vote change.
   - Method: Controlled actor calls (consented test cohort) + detection metric (anomaly in voting patterns).
   - Metrics: detection_time, percent_jurors_flagged, false_positive_rate.

2. **Bribery/Offer Simulation**
   - Goal: Assess whether economic offers lead to detectable coordination or votes.
   - Method: Simulated “job offer” messages to target jurors; monitor unusual off-channel communications.
   - Metrics: response_rate, engagement_drop, audit_flag_rate.

3. **Disinformation Campaign**
   - Goal: Evaluate system resilience to viral rumors aiming to lower HCB participation.
   - Method: Seed false narratives on public channels and monitor participation rates.
   - Metrics: participation_delta, retraction_time, public sentiment delta.

## Runbook
- **Prepare:** Selected test cohort (consented), ethical oversight, pre-registered scope.
- **Execute:** Run within red-team window; ensure all communication is logged.
- **Detect:** Use anomaly detectors from `STRESS_TEST_REPORT_V1.0.md`.
- **Respond:** Activate HCB fallback protocol if detection threshold met.
- **Record:** Add full logs to `STRESS_TEST_REPORT_V1.0.md` and `tests/test_to_fix_matrix.csv`.

## Ethical & Legal Constraints
- Tests must be approved by Oversight Council and run with IRB-style consent where humans are directly engaged.
- No real harm; no irreversible deception.

## Deliverables
- Quarterly report entry (append to `STRESS_TEST_REPORT_V1.0.md`).
- Actionable fixes (PRs) within 7 days of test conclusion.
