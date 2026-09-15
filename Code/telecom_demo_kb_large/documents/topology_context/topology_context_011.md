# Topology Context: EDGE-RAW-022

## Device context

EDGE-RAW-022 is a EDGE device using Cisco ASR9904 and IOS-XR 7.8.x. It is located at POP-RAW-03 in Rawalpindi and is classified major.

## Immediate neighborhood

Synthetic topology relationships place the device among peers such as BNG-MUL-064, PE-ISL-018, and P-PES-053. The exact adjacency should be resolved from the structured topology store rather than inferred from this narrative.

## Dependency implications

A fault on a PE/P/RR device can affect multiple services or downstream sessions. RCA should walk the graph to identify redundant paths, shared transport, and common failure domains.

## Failure-domain reasoning

Multiple simultaneous alarms on devices sharing a site, circuit, optic path, or upstream aggregation point can indicate a common cause. Independent alarms on unrelated failure domains should not automatically be merged into one RCA.

## Operational note

Topology data is time-sensitive. When a change replaces a link or device, use effective timestamps so that RCA reconstructs the network as it existed at incident time.
