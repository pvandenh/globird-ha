## What's Changed

**Refresh GloBird costs every poll**
Usage, cost, and weather detail now refresh on every normal 30-minute coordinator update instead of waiting for a separate 6-hour detail refresh window. This lets Home Assistant pick up GloBird's daily backend cost updates much sooner while still falling back to cached service detail if a portal endpoint has a temporary failure.

**Expose newer usage registers and cost categories**
The integration now preserves every usage register returned by the portal in sensor attributes, treats any `B*` register as solar export, and exposes cost category totals such as `ZEROHERO Credit` and `Super Export top up`. This keeps Home Assistant closer to the current GloBird portal view for controlled load, climate, solar export, and newer feed-in credit categories.

**Add expected monthly cost**
A new `Expected Monthly Cost` sensor projects the current calendar-month cost from completed daily cost rows. The sensor attributes include cost-to-date, completed days, days in month, latest data day, and the calculation used so the estimate is transparent.

*Update available via HACS*
