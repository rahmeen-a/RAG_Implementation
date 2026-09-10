# Historical Incident INC-2025-0030

## Incident summary

INC-2025-0030 affected PE-FAI-078 at POP-FAI-02. The primary symptom was ISIS adjacency flap: IGP adjacency repeatedly changes state. The incident was classified as P1 and lasted approximately 25 minutes.

## Observed evidence

Engineers correlated the alarm with device state, interface state, peer/session behavior, and nearby alarms. The investigation considered whether the anomaly was causal or consequential. Relevant device platform was Cisco ASR1009-X running IOS-XE 17.9.x. Historical notes recorded the root-cause category as physical_optical.

## Investigation path

The first checks were alarm timing, recent changes, topology neighbors, and performance baseline deviation. A recent change record near the investigation window was CHG-2026-0107 on PE-MUL-040; engineers verified whether it was actually related rather than assuming temporal proximity meant causation. Peer-side state and interface evidence were used to narrow the hypothesis.

## Resolution and reusable lesson

Confirmed root cause: Optical degradation. Resolution: replace optic / clean connector. The incident was marked high. Reusable RCA lesson: correlate the protocol symptom with lower-layer transport, recent configuration, resource state, and service topology before assigning the fault to the protocol itself.
