# Historical Incident INC-2025-0035

## Incident summary

INC-2025-0035 affected PE-ISL-016 at POP-ISL-01. The primary symptom was Link down: interface operational state is down. The incident was classified as P1 and lasted approximately 122 minutes.

## Observed evidence

Engineers correlated the alarm with device state, interface state, peer/session behavior, and nearby alarms. The investigation considered whether the anomaly was causal or consequential. Relevant device platform was Nokia 7750 SR-7 running SR OS 23.10. Historical notes recorded the root-cause category as software.

## Investigation path

The first checks were alarm timing, recent changes, topology neighbors, and performance baseline deviation. A recent change record near the investigation window was CHG-2026-0005 on PE-LAH-077; engineers verified whether it was actually related rather than assuming temporal proximity meant causation. Peer-side state and interface evidence were used to narrow the hypothesis.

## Resolution and reusable lesson

Confirmed root cause: Software defect or process instability. Resolution: restart/upgrade per advisory. The incident was marked high. Reusable RCA lesson: correlate the protocol symptom with lower-layer transport, recent configuration, resource state, and service topology before assigning the fault to the protocol itself.
