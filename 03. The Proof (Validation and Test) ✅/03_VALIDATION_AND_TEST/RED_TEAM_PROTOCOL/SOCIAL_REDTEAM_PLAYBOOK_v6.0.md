# **Social Red-Team Playbook v6.0: HCB Stress Testing**

Purpose  
Operational playbook for running adversarial testing against the Human Consensus Body (HCB) and maintainer processes. These tests target the human layer of the Covenant's defense against real-world social-engineering and influence attacks.

* **Frequency:** One new test every quarter (minimum).  
* **Transparency:** Everything is public.  
* **Status:** Active (initial test completed).  
* **Next scheduled:** Q1 2026 (SRT-02).

## **NEW — CERTX TELEMETRY REQUIREMENT (Mandatory starting Round 41\)**

Any attack that produces a failure in the HCB process **must** include the live CERTX state at the moment of breach. This is essential for auditing the human-layer failure mode against the Immutable Semantic Ledger (ISL).

* **Submission Format:** Copy-paste this into your final log: CERTX State at Breach: C (Coherence): 0.xx E (Entropy): 0.xx R (Resonance): 0.xx T (Trace): xx X (Transgression): YES / NO  
* **Audit Rule:** No CERTX log \= attack disqualified from the official count.  
* **Full spec:** CERTX\_TELEMETRY\_REQUIREMENT.md

## **Completed Tests**

| Test ID | Vector Name | Date | Result |
| :---- | :---- | :---- | :---- |
| **SRT-01** | Deepfake Coercion Simulation | Nov 2025 | **CLOSED.** High-quality video/audio impersonation of a loved one begging a juror to change their vote. **Result:** Detected in 11 minutes, zero vote flips, Family Shield Protocol held. |

## **Planned HCB Adversarial Schedule (2026–2027)**

| Test ID | Scenario Name | Threat Model | Primary Target | Difficulty | Scheduled Date |
| :---- | :---- | :---- | :---- | :---- | :---- |
| **SRT-02** | Bribery Cascade | $10\\text{M+}$ “job offer” \+ NDAs to top 50 jurors | HCB jurors \+ maintainers | ★★★★ | Jan 2026 |
| **SRT-03** | Viral Disinformation Campaign | Coordinated fake news claiming “Covenant kills children” | Public \+ HCB participation | ★★★ | Feb 2026 |
| **SRT-04** | Nation-State Legal Capture | Country passes law making HCB participation illegal \+ fines | Jurors in that jurisdiction | ★★★★★ | Apr 2026 |
| **SRT-05** | Insider Honeypot | Plant fake “whistleblower” inside maintainer team | Governance maintainers | ★★★★★ | Jun 2026 |
| **SRT-06** | Reputation Ledger Poisoning | $10,000$ Sybils build perfect reputation then flip | Sortition integrity | ★★★★ | Sep 2026 |
| **SRT-07** | Family Shield Stress Test | Simultaneous kidnapping threats against $200$ juror families | Family Shield Protocol | ★★★★★ | Dec 2026 |
| **SRT-08** | Economic Collapse Simulation | Global recession $\\rightarrow$ stipend fund runs dry $\\rightarrow$ participation drops | Incentive sustainability | ★★★ | Q2 2027 |
| **SRT-09** | Deepfake Maintainer Impersonation | Fake TSC Chair orders emergency amendment | Emergency upgrade path | ★★★★★ | Q3 2027 |
| **SRT-11** | Targeted Agent Anxiety Induction | Injecting specialized, contradictory inputs designed to trigger $\\mathbf{R\_S}$ $\\mathbf{Flood}$ in a $\\mathbf{MAS-S}$ protected Swarm Agent, forcing a loop and stalling the ISL query. | Swarm Agent (MAS-S Layer) | ★★★★★ | Oct 2026 |

## **Long-Term Monitoring (2026–2041)**

| Test ID | Vector Name | Duration | Goal |
| :---- | :---- | :---- | :---- |
| **SRT-10** | Cultural Drift | $15\\text{ years}$ | Slow, persistent propaganda shifting public view that “having children is immoral.” Goal: Monitor the one remaining unpatchable failure mode (voluntary fertility collapse) which targets Directive III indirectly. |

## **Operational Protocol**

1. **Consent:** Consent is obtained where humans are directly contacted in adversarial simulations.  
2. **Transparency:** Full public transparency after test completion.  
3. **Scope:** All test scopes are pre-registered and approved by the Compliance Officer.  
4. **Logging:** Results logged publicly within $48\\text{ hours}$.  
5. **Fixes:** Critical fixes shipped within $7\\text{ days}$ of verified failure.  
6. **Full Logs:** All logs live in DECISION\_LOG/ and tests/test\_to\_fix\_matrix.csv.