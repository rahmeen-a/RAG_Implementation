# Historical Incident INC-2026-0114

## Incident summary

INC-2026-0114 affected RR-ISL-009 at POP-ISL-03. The primary symptom was ISIS adjacency flap: IGP adjacency repeatedly changes state. The incident was classified as P1 and lasted approximately 112 minutes.

## Observed evidence

Engineers correlated the alarm with device state, interface state, peer/session behavior, and nearby alarms. The investigation considered whether the anomaly was causal or consequential. Relevant device platform was Cisco NCS5508 running IOS-XR 7.8.x. Historical notes recorded the root-cause category as physical_optical.

## Investigation path

The first checks were alarm timing, recent changes, topology neighbors, and performance baseline deviation. A recent change record near the investigation window was CHG-2026-0036 on EDGE-KAR-072; engineers verified whether it was actually related rather than assuming temporal proximity meant causation. Peer-side state and interface evidence were used to narrow the hypothesis.

## Resolution and reusable lesson

Confirmed root cause: Optical degradation. Resolution: replace optic / clean connector. The incident was marked confirmed. Reusable RCA lesson: correlate the protocol symptom with lower-layer transport, recent configuration, resource state, and service topology before assigning the fault to the protocol itself.
