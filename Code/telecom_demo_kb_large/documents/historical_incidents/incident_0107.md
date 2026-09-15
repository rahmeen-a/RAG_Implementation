# Historical Incident INC-2026-0107

## Incident summary

INC-2026-0107 affected PE-FAI-068 at POP-FAI-03. The primary symptom was Packet loss: end-to-end loss increases above baseline. The incident was classified as P1 and lasted approximately 36 minutes.

## Observed evidence

Engineers correlated the alarm with device state, interface state, peer/session behavior, and nearby alarms. The investigation considered whether the anomaly was causal or consequential. Relevant device platform was Cisco ASR9904 running IOS-XR 7.8.x. Historical notes recorded the root-cause category as physical_fiber.

## Investigation path

The first checks were alarm timing, recent changes, topology neighbors, and performance baseline deviation. A recent change record near the investigation window was CHG-2026-0033 on RR-PES-023; engineers verified whether it was actually related rather than assuming temporal proximity meant causation. Peer-side state and interface evidence were used to narrow the hypothesis.

## Resolution and reusable lesson

Confirmed root cause: Fiber impairment. Resolution: repair fiber / move traffic. The incident was marked high. Reusable RCA lesson: correlate the protocol symptom with lower-layer transport, recent configuration, resource state, and service topology before assigning the fault to the protocol itself.
