# Historical Incident INC-2026-0113

## Incident summary

INC-2026-0113 affected RR-LAH-010 at POP-LAH-01. The primary symptom was BGP flapping: peer repeatedly resets and returns to Established. The incident was classified as P3 and lasted approximately 24 minutes.

## Observed evidence

Engineers correlated the alarm with device state, interface state, peer/session behavior, and nearby alarms. The investigation considered whether the anomaly was causal or consequential. Relevant device platform was Juniper PTX10008 running Junos 23.2R1. Historical notes recorded the root-cause category as capacity.

## Investigation path

The first checks were alarm timing, recent changes, topology neighbors, and performance baseline deviation. A recent change record near the investigation window was CHG-2026-0083 on EDGE-PES-047; engineers verified whether it was actually related rather than assuming temporal proximity meant causation. Peer-side state and interface evidence were used to narrow the hypothesis.

## Resolution and reusable lesson

Confirmed root cause: Sustained resource exhaustion. Resolution: rebalance or increase capacity. The incident was marked confirmed. Reusable RCA lesson: correlate the protocol symptom with lower-layer transport, recent configuration, resource state, and service topology before assigning the fault to the protocol itself.
