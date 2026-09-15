# Historical Incident INC-2026-0102

## Incident summary

INC-2026-0102 affected EDGE-MUL-031 at POP-MUL-02. The primary symptom was BGP flapping: peer repeatedly resets and returns to Established. The incident was classified as P1 and lasted approximately 86 minutes.

## Observed evidence

Engineers correlated the alarm with device state, interface state, peer/session behavior, and nearby alarms. The investigation considered whether the anomaly was causal or consequential. Relevant device platform was Juniper MX480 running Junos 23.2R1. Historical notes recorded the root-cause category as physical_fiber.

## Investigation path

The first checks were alarm timing, recent changes, topology neighbors, and performance baseline deviation. A recent change record near the investigation window was CHG-2026-0023 on PE-MUL-001; engineers verified whether it was actually related rather than assuming temporal proximity meant causation. Peer-side state and interface evidence were used to narrow the hypothesis.

## Resolution and reusable lesson

Confirmed root cause: Fiber impairment. Resolution: repair fiber / move traffic. The incident was marked confirmed. Reusable RCA lesson: correlate the protocol symptom with lower-layer transport, recent configuration, resource state, and service topology before assigning the fault to the protocol itself.
