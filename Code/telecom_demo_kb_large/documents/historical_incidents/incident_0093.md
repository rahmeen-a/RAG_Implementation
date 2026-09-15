# Historical Incident INC-2025-0093

## Incident summary

INC-2025-0093 affected BNG-MUL-064 at POP-MUL-02. The primary symptom was High CPU: CPU remains above operational baseline. The incident was classified as P2 and lasted approximately 10 minutes.

## Observed evidence

Engineers correlated the alarm with device state, interface state, peer/session behavior, and nearby alarms. The investigation considered whether the anomaly was causal or consequential. Relevant device platform was Cisco ASR1009-X running IOS-XE 17.9.x. Historical notes recorded the root-cause category as software.

## Investigation path

The first checks were alarm timing, recent changes, topology neighbors, and performance baseline deviation. A recent change record near the investigation window was CHG-2026-0111 on P-PES-053; engineers verified whether it was actually related rather than assuming temporal proximity meant causation. Peer-side state and interface evidence were used to narrow the hypothesis.

## Resolution and reusable lesson

Confirmed root cause: Software defect or process instability. Resolution: restart/upgrade per advisory. The incident was marked high. Reusable RCA lesson: correlate the protocol symptom with lower-layer transport, recent configuration, resource state, and service topology before assigning the fault to the protocol itself.
