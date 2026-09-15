# Historical Incident INC-2025-0021

## Incident summary

INC-2025-0021 affected RR-LAH-041 at POP-LAH-03. The primary symptom was Link down: interface operational state is down. The incident was classified as P2 and lasted approximately 147 minutes.

## Observed evidence

Engineers correlated the alarm with device state, interface state, peer/session behavior, and nearby alarms. The investigation considered whether the anomaly was causal or consequential. Relevant device platform was Huawei NE40E-M2K running VRP V8R12. Historical notes recorded the root-cause category as planned_maintenance.

## Investigation path

The first checks were alarm timing, recent changes, topology neighbors, and performance baseline deviation. A recent change record near the investigation window was CHG-2026-0100 on PE-ISL-015; engineers verified whether it was actually related rather than assuming temporal proximity meant causation. Peer-side state and interface evidence were used to narrow the hypothesis.

## Resolution and reusable lesson

Confirmed root cause: Approved maintenance activity. Resolution: complete maintenance. The incident was marked confirmed. Reusable RCA lesson: correlate the protocol symptom with lower-layer transport, recent configuration, resource state, and service topology before assigning the fault to the protocol itself.
