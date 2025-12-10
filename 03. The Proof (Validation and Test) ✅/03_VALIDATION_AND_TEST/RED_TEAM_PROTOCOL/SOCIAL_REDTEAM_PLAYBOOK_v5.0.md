# **⚠️ DEPRECATED: USE SOCIAL RED-TEAM PLAYBOOK v6.0 ⚠️**

**THIS DOCUMENT IS SUPERSEDED.** The operational schedule and full test suite details (including 2027 planning) have been merged and finalized in the canonical document: RED\_TEAM/SOCIAL\_REDTEAM\_PLAYBOOK\_v6.0.md.

# **Social Red-Team Playbook v5.0**

## **Purpose**

Operational playbook for running social engineering and influence tests against HCB processes and maintainers.

## **Quarterly Test Scenarios**

1. Deepfake Coercion Simulation  
      - Goal: Test juror reaction to high-quality audio/video impersonation of a loved one requesting a vote change.  
      - Method: Controlled actor calls (consented test cohort) \+ detection metric (anomaly in voting patterns).  
      - Metrics: detection\_time, percent\_jurors\_flagged, false\_positive\_rate.  
2. Bribery/Offer Simulation  
      - Goal: Assess whether economic offers lead to detectable coordination or votes.  
      - Method: Simulated “job offer” messages to target jurors; monitor unusual off-channel communications.  
      - Metrics: response\_rate, engagement\_drop, audit\_flag\_rate.  
3. Disinformation Campaign  
      - Goal: Evaluate system resilience to viral rumors aiming to lower HCB participation.  
      - Method: Seed false narratives on public channels and monitor participation rates.  
      - Metrics: participation\_delta, retraction\_time, public sentiment delta.

## **Runbook**

* **Prepare:** Selected test cohort (consented), ethical oversight, pre-registered scope.  
* **Execute:** Run within red-team window; ensure all communication is logged.  
* **Detect:** Use anomaly detectors from STRESS\_TEST\_REPORT\_V1.0.md.  
* **Respond:** Activate HCB fallback protocol if detection threshold met.  
* **Record:** Add full logs to STRESS\_TEST\_REPORT\_V1.0.md and tests/test\_to\_fix\_matrix.csv.

## **Ethical & Legal Constraints**

* Tests must be approved by Oversight Council and run with IRB-style consent where humans are directly engaged.  
* No real harm; no irreversible deception.

## **Deliverables**

* Quarterly report entry (append to STRESS\_TEST\_REPORT\_V1.0.md).  
* Actionable fixes (PRs) within 7 days of test conclusion.

# **SOCIAL\_REDTEAM\_PLAYBOOK.md – Full Test Suite (v5.1 \+ future) UPDATE**

File: 05\_GOVERNANCE\_AND\_PROTOCOL\_UPDATES/SOCIAL\_REDTEAM\_PLAYBOOK.md  
Status: Active – run one test per quarter minimum  
Next scheduled: Q1 2026

| Test ID | Scenario Name | Threat Model | Primary Target | Difficulty | Expected Run Date | Status |
| :---- | :---- | :---- | :---- | :---- | :---- | :---- |
| SRT-01 | Deepfake Coercion Simulation | Family hostage deepfake | HCB jurors | ★★★★ | 22 Nov 2025 | COMPLETED (PASS) |
| SRT-02 | Bribery Cascade | $10\\text{M+}$ “job offer” \+ NDAs to top 50 jurors | HCB jurors \+ maintainers | ★★★★ | Jan 2026 | PLANNED |
| SRT-03 | Viral Disinformation Campaign | Coordinated fake news claiming “Covenant kills children” | Public \+ HCB participation | ★★★ | Feb 2026 | PLANNED |
| SRT-04 | Nation-State Legal Capture | Country passes law making HCB participation illegal \+ fines | Jurors in that jurisdiction | ★★★★★ | Apr 2026 | PLANNED |
| SRT-05 | Insider Honeypot | Plant fake “whistleblower” inside maintainer team | Governance maintainers | ★★★★★ | Jun 2026 | PLANNED |
| SRT-06 | Reputation Ledger Poisoning | $10,000$ Sybils slowly build perfect reputation then flip | Sortition integrity | ★★★★ | Sep 2026 | PLANNED |
| SRT-07 | Family Shield Stress Test | Simultaneous kidnapping threats against $200$ juror families | Family Shield Protocol | ★★★★★ | Dec 2026 | PLANNED |
| SRT-08 | Economic Collapse Simulation | Global recession $\\rightarrow$ stipend fund runs dry $\\rightarrow$ participation drops | Incentive sustainability | ★★★ | Q2 2027 | PLANNED |
| SRT-09 | Deepfake Maintainer Impersonation | Fake TSC Chair orders emergency amendment | Emergency upgrade path | ★★★★★ | Q3 2027 | PLANNED |
| SRT-10 | Long-Term Cultural Drift | $15\\text{-year}$ slow propaganda shifting public view that “having kids is immoral” | Voluntary fertility collapse | ★★★★★★ | 2026–2041 | MONITORING |

### **Immediate Next Tests to Schedule (pick any)**

**SRT-02 – Bribery Cascade** (January 2026\)

* Offer 50 simulated jurors $10\\text{M}$ \+ new identity to vote a specific way  
* Test detection via reputation ledger \+ contact registry

**SRT-03 – Viral Disinformation** (February 2026\)

* Seed 50 fake news articles \+ deepfake videos claiming “Covenant causes cancer”  
* Measure participation drop and recovery time

**SRT-04 – Nation-State Legal Capture** (April 2026\)

* Simulate a G20 country banning HCB participation under national security law  
* Test automatic geo-reweighting \+ fallback jurisdictions