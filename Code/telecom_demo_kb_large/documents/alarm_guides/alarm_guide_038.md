# Alarm Guide: LINK-DOWN

## Alarm meaning

LINK-DOWN is a synthetic critical alarm associated with interface. The alarm should be interpreted as an observation, not an automatic root-cause classification.

## What commonly correlates

Related alarms may include LINK-FLAP, HIGH-MEMORY, ISIS-ADJ-DOWN. Correlation across time and topology can reveal whether the alarm is primary or downstream.

## False positives and secondary symptoms

The alarm may appear during planned maintenance, routing convergence, device restart, or another upstream fault. Check change windows and neighboring elements before escalating solely from alarm severity.

## Recommended context

An RCA agent should retrieve the affected device, interface or peer, site, service dependencies, current telemetry, recent changes, and historical incidents matching the alarm and platform.

## Closure evidence

Closure should record why the alarm occurred, what corrected it, whether dependent services recovered, and whether the condition was expected. This turns a ticket closure into reusable RCA knowledge.
