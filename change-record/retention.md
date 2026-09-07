# Retention

Retention is how long the app keeps a record before it expires.

| Tier | Retention |
|---|---|
| Free | 90 days, fixed |
| Paid | chosen by a Jira admin: 30, 90, 180, 365 or 730 days, or keep everything |

**Default on the paid tier: keep everything.** An admin changes it under
Manage apps → Change Record → Configure. A new setting applies at the next
daily run, not instantly.

**What expiry does.** Records older than the retention are removed per work
item, oldest first. Each trimmed work item keeps a marker saying that
records before a certain point were expired by retention, so the
verification report can still confirm the remaining chain is intact and
report how many records expired. Expiry is a deletion inside your own
site's storage; nothing is copied anywhere first.

**Moving from free to paid** keeps whatever the free tier still holds and
stops the 90-day expiry from the next daily run. Records that already
expired under the free tier are gone; the app cannot backfill them and does
not read Jira's history to recreate them.

**Moving from paid to free** returns the site to the 90-day rule at the
next daily run.

**Retention and the settings sheet.** Every XLSX export prints the
retention in effect when it was produced, so a file states its own
completeness.
