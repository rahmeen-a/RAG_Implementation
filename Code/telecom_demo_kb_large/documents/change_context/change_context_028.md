# RCA Change Context: BGP-policy

## Change record

CHG-2026-0044 is a synthetic BGP-policy change associated with PE-FAI-068 at POP-FAI-03. The change was scheduled for approximately 54 minutes and has status completed.

## Why it matters to RCA

Recent changes are a high-value causal signal because they provide an explicit event near the beginning of an incident. Temporal proximity is not sufficient; the changed object must also plausibly explain the observed symptom.

## Before and after checks

Compare device state before and after the change when snapshots exist. For routing changes, compare peers, policies and route counts. For interfaces or optics, compare link state and counters. For monitoring changes, compare polling load and process CPU.

## Rollback reasoning

Rollback is appropriate only when evidence supports the change as causal and policy permits it. A rollback that restores service is strong causal evidence, but the permanent corrective action should still document why the change produced the failure.

## Data retention

Keep change ID, operator, timestamps, device/object, intended outcome, observed outcome, and configuration diff. These fields should be queryable structurally while explanatory notes can be indexed semantically.
