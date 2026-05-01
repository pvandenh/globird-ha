## What's Changed

**Fix: `Billing Period Days` was off by one (issue #1)**
The sensor was counting today as a full day, but GloBird's usage and cost data only covers through end of yesterday. That meant `Billing Period Days` always read one day higher than the data actually backed — e.g. on day 5 of a billing period it would show 5, while `Billing Period Cost` and the daily usage sensors only had 4 days of data behind them. The sensor now reports the number of completed days since the latest invoice issue date, so it lines up with the data the rest of the integration is showing. Note: this will read one lower than the "Number of Days" field shown in the GloBird app, which includes today.

*Update available via HACS*
