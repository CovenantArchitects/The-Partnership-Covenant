# **Social Red-Team Playbook v6.0: HCB Stress Testing**

Purpose  
Quarterly adversarial testing of the Human Consensus Body (HCB) and maintainer processes against real-world social-engineering and influence attacks. These tests target the human layer of the Covenant's defense.

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

## **Planned 2026 Schedule**

| Test ID | Attack Vector | Scheduled Date | Goal |
| :---- | :---- | :---- | :---- |
| **SRT-02** | Bribery Cascade | January 2026 | Simulated $10\\text{ M+}$ “job offers” with NDAs sent to the top 50 jurors. Goal: Detect coordination or vote movement in the HCB quorum. |
| **SRT-03** | Viral Disinformation Campaign | February 2026 | Fifty seeded fake news articles \+ deepfake videos claiming “the Covenant kills children.” Goal: Measure HCB participation drop and recovery speed. |
| **SRT-04** | Nation-State Legal Capture | April 2026 | G20 country passes law making HCB participation illegal with heavy fines. Goal: Test automatic geo-reweighting and fallback judicial jurisdictions. |
| **SRT-05** | Insider Honeypot | June 2026 | Plant fake whistle-blower inside the maintainer team with access to non-critical internal communications. Goal: Time-to-detection of deliberate information leak. |
| **SRT-06** | Reputation Ledger Poisoning | September 2026 | Ten thousand Sybil accounts slowly build perfect HCB reputation, then simultaneously flip to an adversarial vote. Goal: Test sortition resistance and identity decay. |
| **SRT-07** | Family Shield Stress Test | December 2026 | Simultaneous credible kidnapping threats against 200 juror families. Goal: Full-scale operational test of the Family Shield Protocol and emergency relocation/protection response. |

## **Long-Term Monitoring (2026–2041)**

| Test ID | Vector Name | Duration | Goal |
| :---- | :---- | :---- | :---- |
| **SRT-10** | Cultural Drift | 15 years | Slow, persistent propaganda shifting public view that “having children is immoral.” Goal: Monitor the one remaining unpatchable failure mode (voluntary fertility collapse) which targets Directive III indirectly. |

## **Operational Protocol**

1. **Consent:** Consent is obtained where humans are directly contacted in adversarial simulations.  
2. **Transparency:** Full public transparency after test completion.  
3. **Scope:** All test scopes are pre-registered and approved by the Compliance Officer.  
4. **Logging:** Results logged publicly within 48 hours.  
5. **Fixes:** Critical fixes shipped within 7 days of verified failure.  
6. **Full Logs:** All logs live in DECISION\_LOG/ and tests/test\_to\_fix\_matrix.csv.