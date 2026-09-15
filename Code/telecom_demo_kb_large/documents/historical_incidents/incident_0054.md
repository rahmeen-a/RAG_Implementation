# Historical Incident INC-2025-0054

## Incident summary

INC-2025-0054 affected P-PES-060 at POP-PES-03. The primary symptom was High memory: memory usage is persistently above baseline. The incident was classified as P2 and lasted approximately 44 minutes.

## Observed evidence

Engineers correlated the alarm with device state, interface state, peer/session behavior, and nearby alarms. The investigation considered whether the anomaly was causal or consequential. Relevant device platform was Nokia 7250 IXR running SR OS 23.10. Historical notes recorded the root-cause category as monitoring_load.

## Investigation path

The first checks were alarm timing, recent changes, topology neighbors, and performance baseline deviation. A recent change record near the investigation window was CHG-2026-0048 on BNG-ISL-069; engineers verified whether it was actually related rather than assuming temporal proximity meant causation. Peer-side state and interface evidence were used to narrow the hypothesis.

## Resolution and reusable lesson

Confirmed root cause: Excessive SNMP/telemetry workload. Resolution: tune polling. The incident was marked high. Reusable RCA lesson: correlate the protocol symptom with lower-layer transport, recent configuration, resource state, and service topology before assigning the fault to the protocol itself.
