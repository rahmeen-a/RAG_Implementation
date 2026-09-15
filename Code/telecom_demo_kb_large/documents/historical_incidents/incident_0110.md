# Historical Incident INC-2026-0110

## Incident summary

INC-2026-0110 affected PE-ISL-012 at POP-ISL-02. The primary symptom was Route count anomaly: BGP/IGP route count deviates from baseline. The incident was classified as P2 and lasted approximately 22 minutes.

## Observed evidence

Engineers correlated the alarm with device state, interface state, peer/session behavior, and nearby alarms. The investigation considered whether the anomaly was causal or consequential. Relevant device platform was Nokia 7750 SR-12 running SR OS 23.10. Historical notes recorded the root-cause category as power.

## Investigation path

The first checks were alarm timing, recent changes, topology neighbors, and performance baseline deviation. A recent change record near the investigation window was CHG-2026-0040 on PE-KAR-073; engineers verified whether it was actually related rather than assuming temporal proximity meant causation. Peer-side state and interface evidence were used to narrow the hypothesis.

## Resolution and reusable lesson

Confirmed root cause: Power or site infrastructure event. Resolution: restore stable power. The incident was marked confirmed. Reusable RCA lesson: correlate the protocol symptom with lower-layer transport, recent configuration, resource state, and service topology before assigning the fault to the protocol itself.
