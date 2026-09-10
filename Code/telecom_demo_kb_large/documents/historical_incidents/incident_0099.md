# Historical Incident INC-2025-0099

## Incident summary

INC-2025-0099 affected P-MUL-013 at POP-MUL-01. The primary symptom was High CPU: CPU remains above operational baseline. The incident was classified as P1 and lasted approximately 90 minutes.

## Observed evidence

Engineers correlated the alarm with device state, interface state, peer/session behavior, and nearby alarms. The investigation considered whether the anomaly was causal or consequential. Relevant device platform was Cisco NCS5508 running IOS-XR 7.8.x. Historical notes recorded the root-cause category as configuration.

## Investigation path

The first checks were alarm timing, recent changes, topology neighbors, and performance baseline deviation. A recent change record near the investigation window was CHG-2026-0117 on PE-ISL-051; engineers verified whether it was actually related rather than assuming temporal proximity meant causation. Peer-side state and interface evidence were used to narrow the hypothesis.

## Resolution and reusable lesson

Confirmed root cause: Incorrect routing or interface configuration. Resolution: rollback/fix configuration. The incident was marked confirmed. Reusable RCA lesson: correlate the protocol symptom with lower-layer transport, recent configuration, resource state, and service topology before assigning the fault to the protocol itself.
