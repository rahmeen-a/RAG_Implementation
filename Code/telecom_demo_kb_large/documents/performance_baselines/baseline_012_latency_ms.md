# Performance Baseline Note: latency_ms

## Baseline definition

The synthetic baseline for latency_ms on PE-LAH-026 is based on a rolling operational window. Typical central behavior is around 5, while the upper normal range approaches 35. Investigation should begin around 80, with context from the current workload.

## Why the baseline matters

A fixed universal threshold can generate misleading RCA conclusions. The same CPU value may be normal for one device during convergence and abnormal for another under steady state. Baselines should be evaluated by time window, role, and workload.

## Temporal correlation

Compare the metric before, during, and after the incident. Determine which event moved first: physical alarm, route churn, configuration change, process CPU, or service degradation. Temporal ordering helps separate cause from consequence.

## Cross-metric correlation

For network RCA, combine latency_ms with interface errors, link state, BGP/IGP changes, route counts, packet loss, latency, and recent changes when available. A single metric rarely provides enough evidence.

## RCA interpretation

A deviation should be treated as supporting evidence. The final root cause should be tied to a concrete mechanism, observed correlation, and recovery behavior after remediation.
