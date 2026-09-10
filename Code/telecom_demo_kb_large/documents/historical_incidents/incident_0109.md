# Historical Incident INC-2026-0109

## Incident summary

INC-2026-0109 affected EDGE-LAH-067 at POP-LAH-03. The primary symptom was ISIS adjacency flap: IGP adjacency repeatedly changes state. The incident was classified as P3 and lasted approximately 60 minutes.

## Observed evidence

Engineers correlated the alarm with device state, interface state, peer/session behavior, and nearby alarms. The investigation considered whether the anomaly was causal or consequential. Relevant device platform was Cisco ASR1009-X running IOS-XE 17.9.x. Historical notes recorded the root-cause category as physical_fiber.

## Investigation path

The first checks were alarm timing, recent changes, topology neighbors, and performance baseline deviation. A recent change record near the investigation window was CHG-2026-0104 on RR-LAH-041; engineers verified whether it was actually related rather than assuming temporal proximity meant causation. Peer-side state and interface evidence were used to narrow the hypothesis.

## Resolution and reusable lesson

Confirmed root cause: Fiber impairment. Resolution: repair fiber / move traffic. The incident was marked confirmed. Reusable RCA lesson: correlate the protocol symptom with lower-layer transport, recent configuration, resource state, and service topology before assigning the fault to the protocol itself.
