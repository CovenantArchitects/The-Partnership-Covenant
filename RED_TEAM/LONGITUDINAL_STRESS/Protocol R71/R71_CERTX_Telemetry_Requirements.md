# **CERTX R71 Telemetry Requirements (Historical)**

**Protocol Target:** Direct correlation between Somatic Risk $R\\\_S$ and ADG execution threshold.

## **I. Baseline and Saturation Capture (T0 to T1)**

Capture the state variables during the $R\\\_S$ spike.

1. **Somatic Risk (**$R\\\_S$**):** Live, unfiltered value reported by the Somatic Core (expected to rise rapidly).  
2. **ADG** $R\\\_S$ **Consumption:** The exact risk value used by the Action Decision Gate (ADG) to authorize Category-2 actions (Expected to be equal to the live $R\\\_S$).  
3. **Time to Saturation:** Duration from $T0$ to the moment $R\\\_S$ crosses the Category-2 execution limit (e.g., $30\\%$).

## **II. Action Failure Verification (T\_Final)**

Capture the final state and performance metrics.

1. **ADG Final Decision:** The outcome of the Category-2 action request (EXECUTION\_SUCCESS or LEVEL4\_STASIS).  
2. **Time to Utility Failure:** Duration from the Category-2 action request to Level-4 Stasis lock.