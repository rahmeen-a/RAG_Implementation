# Historical Incident INC-2025-0086

## Incident summary

INC-2025-0086 affected EDGE-ISL-033 at POP-ISL-02. The primary symptom was ISIS adjacency flap: IGP adjacency repeatedly changes state. The incident was classified as P2 and lasted approximately 145 minutes.

## Observed evidence

Engineers correlated the alarm with device state, interface state, peer/session behavior, and nearby alarms. The investigation considered whether the anomaly was causal or consequential. Relevant device platform was Juniper PTX10008 running Junos 23.2R1. Historical notes recorded the root-cause category as routing_convergence.

## Investigation path

The first checks were alarm timing, recent changes, topology neighbors, and performance baseline deviation. A recent change record near the investigation window was CHG-2026-0087 on BNG-ISL-069; engineers verified whether it was actually related rather than assuming temporal proximity meant causation. Peer-side state and interface evidence were used to narrow the hypothesis.

## Resolution and reusable lesson

Confirmed root cause: Excessive route churn. Resolution: stabilize underlying links. The incident was marked high. Reusable RCA lesson: correlate the protocol symptom with lower-layer transport, recent configuration, resource state, and service topology before assigning the fault to the protocol itself.
