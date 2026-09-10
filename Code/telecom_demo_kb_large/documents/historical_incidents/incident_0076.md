# Historical Incident INC-2025-0076

## Incident summary

INC-2025-0076 affected P-PES-032 at POP-PES-03. The primary symptom was BGP flapping: peer repeatedly resets and returns to Established. The incident was classified as P1 and lasted approximately 36 minutes.

## Observed evidence

Engineers correlated the alarm with device state, interface state, peer/session behavior, and nearby alarms. The investigation considered whether the anomaly was causal or consequential. Relevant device platform was Nokia 7250 IXR running SR OS 23.10. Historical notes recorded the root-cause category as hardware.

## Investigation path

The first checks were alarm timing, recent changes, topology neighbors, and performance baseline deviation. A recent change record near the investigation window was CHG-2026-0007 on PE-LAH-077; engineers verified whether it was actually related rather than assuming temporal proximity meant causation. Peer-side state and interface evidence were used to narrow the hypothesis.

## Resolution and reusable lesson

Confirmed root cause: Hardware component failure. Resolution: replace failed component. The incident was marked confirmed. Reusable RCA lesson: correlate the protocol symptom with lower-layer transport, recent configuration, resource state, and service topology before assigning the fault to the protocol itself.
