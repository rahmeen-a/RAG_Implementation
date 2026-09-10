# Postmortem INC-2026-0153

## Executive summary

INC-2026-0153 occurred on BNG-LAH-029 in POP-LAH-01. The incident presented as Link down. Service impact was assessed using the service dependency map, not only the alarm severity.

## Timeline

The investigation established the order of events: initial anomaly, correlated alarms, supporting telemetry, configuration/change checks, hypothesis testing, corrective action, and service restoration. This ordering matters because a metric that rises after another fault may be a consequence rather than a root cause.

## Root cause analysis

The confirmed root cause was Fiber impairment. Engineers ruled out at least one competing explanation using timing, topology, device state, or change history. The final classification was physical_fiber.

## Corrective action

The immediate corrective action was repair fiber / move traffic. Follow-up work should include validation that the triggering condition does not recur, review of monitoring thresholds, and documentation of the affected asset, peer, service, and change context.

## Lessons learned

Future investigations should search for the same symptom on the same platform, look for similar incidents, check the preceding 60-minute change window, and compare observed performance against baseline. The postmortem is more useful to an RCA agent when it records evidence and exclusions, not just the final answer.
