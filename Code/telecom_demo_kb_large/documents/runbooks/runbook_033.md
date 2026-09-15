# Runbook: BGP hold timer expiry

## Purpose

This runbook describes a repeatable NOC investigation for BGP hold timer expiry. It is designed to separate the observed alarm from the underlying fault and to preserve evidence.

## Initial checks

Confirm the affected object, timestamp, alarm code, severity, and service. Identify the device role, platform, site, immediate neighbors, and whether the problem is isolated or widespread. Check whether there are simultaneous alarms that could indicate a common upstream cause.

## Topology and dependency checks

Walk the topology from the affected interface or device to its peer, transport path, site, and dependent service. Look for redundancy and determine whether alternate paths are healthy. A fault on an aggregation node may produce many downstream symptoms.

## State and telemetry checks

Compare the current state with the device baseline. Check CPU, memory, interface counters, optical values, route/session counts, or protocol state as applicable. Trend the metric around the event rather than relying on one point-in-time value.

## Change and historical checks

Search approved and emergency changes in the preceding 60 minutes and, when relevant, the preceding 24 hours. Search historical incidents with the same symptom, platform, site, peer, and reset reason. Prefer incidents with confirmed root causes over tickets that were simply closed.

## RCA and closure

Do not close the investigation on the first plausible explanation. Require evidence that distinguishes the leading hypothesis from competing causes. Record root-cause category, evidence, corrective action, service impact, and verification after recovery.
