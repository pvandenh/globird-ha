## What's Changed

**Avoid early supply-only daily cost updates**
Latest Daily Cost now waits for the newest complete cost day instead of advancing to a portal day that only contains the fixed `SUPPLY` charge. If GloBird publishes a partial day before usage/export rows are ready, the integration keeps showing the previous complete day while exposing the partial date through `latest_available_day`, `latest_available_day_complete`, and `incomplete_days` attributes.

**Add freshness and ZeroHero status sensors**
New `Last Successful Refresh`, `Refresh Status`, and `Latest Data Date` sensors make it easier to build automations around successful GloBird updates. A new `ZeroHero Status` sensor reports whether the latest complete cost day includes a non-zero `ZEROHERO Credit` row.

**Refresh documentation and entity translations**
The README now documents the 30-minute polling cadence, manual refresh behavior, data freshness rules, and current entity list. Entity translations were also updated to remove stale sensors and include the newer usage, cost, freshness, billing-period, and ZeroHero sensors.

*Update available via HACS*
