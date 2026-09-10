# Site Operations Note: HVAC temperature excursion at POP-MUL-02

## Site event

Hvac Temperature Excursion was recorded at POP-MUL-02. The site is a synthetic core POP serving POP-MUL-02 Core/Edge POP.

## Potential network symptoms

A site event can create multiple downstream alarms including link-down, device-unreachable, BGP neighbor-down, packet loss, latency increase, or service degradation. The first alarm in the chain is not always the physical root cause.

## Correlation guidance

Check facility timestamps against network alarms and device telemetry. For power events, examine reboot signatures and device uptime. For fiber activity, inspect optical alarms and interface errors. For planned maintenance, verify an approved change or maintenance window.

## Service impact

Determine which services depend on the affected site, devices, and transport paths. Redundant services should be checked separately from single-homed services.

## RCA lesson

Site and facilities context should be treated as a first-class evidence source for POP incidents. A network-only knowledge base can incorrectly classify a facility fault as independent device failures.
