# Historical Incident INC-2025-0082

## Incident summary

INC-2025-0082 affected BNG-PES-039 at POP-PES-02. The primary symptom was High memory: memory usage is persistently above baseline. The incident was classified as P1 and lasted approximately 81 minutes.

## Observed evidence

Engineers correlated the alarm with device state, interface state, peer/session behavior, and nearby alarms. The investigation considered whether the anomaly was causal or consequential. Relevant device platform was Huawei NE40E-X8 running VRP V8R12. Historical notes recorded the root-cause category as software.

## Investigation path

The first checks were alarm timing, recent changes, topology neighbors, and performance baseline deviation. A recent change record near the investigation window was CHG-2026-0110 on PE-LAH-026; engineers verified whether it was actually related rather than assuming temporal proximity meant causation. Peer-side state and interface evidence were used to narrow the hypothesis.

## Resolution and reusable lesson

Confirmed root cause: Software defect or process instability. Resolution: restart/upgrade per advisory. The incident was marked high. Reusable RCA lesson: correlate the protocol symptom with lower-layer transport, recent configuration, resource state, and service topology before assigning the fault to the protocol itself.
