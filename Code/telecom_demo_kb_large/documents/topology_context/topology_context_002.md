# Topology Context: PE-RAW-005

## Device context

PE-RAW-005 is a PE device using Huawei NE40E-X8 and VRP V8R12. It is located at POP-RAW-03 in Rawalpindi and is classified critical.

## Immediate neighborhood

Synthetic topology relationships place the device among peers such as EDGE-KAR-072, EDGE-PES-071, and PE-MUL-001. The exact adjacency should be resolved from the structured topology store rather than inferred from this narrative.

## Dependency implications

A fault on a PE/P/RR device can affect multiple services or downstream sessions. RCA should walk the graph to identify redundant paths, shared transport, and common failure domains.

## Failure-domain reasoning

Multiple simultaneous alarms on devices sharing a site, circuit, optic path, or upstream aggregation point can indicate a common cause. Independent alarms on unrelated failure domains should not automatically be merged into one RCA.

## Operational note

Topology data is time-sensitive. When a change replaces a link or device, use effective timestamps so that RCA reconstructs the network as it existed at incident time.
