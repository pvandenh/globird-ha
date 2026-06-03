## What's Changed

**Keep recent usage and cost attributes recorder-safe**
Recent Usage Total and Recent Cost Total now publish compact attributes instead of attaching the full returned daily and register payloads to every Home Assistant state update. This prevents recorder warnings about attributes exceeding Home Assistant's 16 KB state limit while preserving the sensor totals, latest dates, recent rows, and truncation counts.

**Preserve full payloads in diagnostics**
The full cached GloBird usage and cost snapshots remain available through Home Assistant diagnostics with sensitive fields redacted, so troubleshooting detail is still accessible without bloating recorder state attributes.

*Update available via HACS*
