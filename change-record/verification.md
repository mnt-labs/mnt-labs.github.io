# The verification report

Every record the app writes carries a hash over the previous record for
the same work item. The verification report re-walks those chains and
says whether they are intact. It is the page to read when someone asks
"can we trust this export".

**Where.** Manage apps → Change Record → Configure (Jira admins). It runs
weekly on its own, or now with *Verify now*. The result is also printed on
every XLSX export's settings sheet.

**What the summary means**

- *chain intact across N issues, M records* — every record's hash matched.
- *gaps filled* — records the app wrote from a later reconciliation because
  an event from Jira arrived late or not at all. They are ordinary records,
  marked by their source; the count is reported so it is not invisible.
- *redacted* — records whose values or actor were replaced because the
  person's Atlassian account was closed (see below). The record and its
  hash remain; only the content is replaced by a tombstone.
- *expired by retention* — records removed by the retention setting, with
  the trim marker still in the chain.
- *config chain* — the same walk over configuration-change records, if the
  toggle is on.
- *time budget reached; partial* — a very large site was not fully walked
  in one run; the next run continues.

**A break** names the first work item and record where a hash did not
match. It means a stored record differs from what was hashed when it was
written. The app itself never rewrites a record, so a break is something to
investigate, not to repair from within the app: there is no "fix" button,
by design.

**Tamper-evident, not tamper-proof.** The chain shows whether stored
records have changed. It does not prevent a site admin with storage access
from changing them, and the app makes no claim that it does. It is a
footnote to the record, not a certification.

**Closed accounts.** Weekly, the app asks Atlassian which accounts it
holds references to have been closed. For each closed account it redacts
the person and any field value that may contain personal data, in place,
leaving a tombstone the chain still hashes over. Display names are never
stored; they are resolved when shown.
