# Demo KB Chunking Guide

The corpus is intentionally written as moderately sized operational documents rather than tiny FAQ entries.

Recommended first experiment:
- chunk size: 350–500 tokens
- overlap: 50–80 tokens
- preserve document/category/title metadata
- keep structured IDs in metadata
- optionally create one embedding namespace per document category

Recommended metadata:
- category
- document_id/path
- device_id when available
- site_id when available
- vendor/platform/version when available
- alarm_code when available
- root_cause_category when available
- source_type
- synthetic=true

For RCA retrieval, use metadata filters before semantic ranking where possible.
Example:
vendor=Cisco AND platform=ASR1009-X AND category IN (historical_incidents, known_errors, vendor_troubleshooting)

Do not embed structured topology JSON as ordinary prose and expect the vector index to replace graph traversal.
Use the graph/DB for entity and relationship retrieval.
