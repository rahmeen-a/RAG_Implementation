# Historical Incident INC-2025-0007

## Incident summary

INC-2025-0007 affected P-KAR-043 at POP-KAR-03. The primary symptom was High CPU: CPU remains above operational baseline. The incident was classified as P2 and lasted approximately 81 minutes.

## Observed evidence

Engineers correlated the alarm with device state, interface state, peer/session behavior, and nearby alarms. The investigation considered whether the anomaly was causal or consequential. Relevant device platform was Juniper MX480 running Junos 23.2R1. Historical notes recorded the root-cause category as configuration.

## Investigation path

The first checks were alarm timing, recent changes, topology neighbors, and performance baseline deviation. A recent change record near the investigation window was CHG-2026-0067 on RR-LAH-010; engineers verified whether it was actually related rather than assuming temporal proximity meant causation. Peer-side state and interface evidence were used to narrow the hypothesis.

## Resolution and reusable lesson

Confirmed root cause: Incorrect routing or interface configuration. Resolution: rollback/fix configuration. The incident was marked high. Reusable RCA lesson: correlate the protocol symptom with lower-layer transport, recent configuration, resource state, and service topology before assigning the fault to the protocol itself.
