# Configuration changes (optional)

Off by default. A Jira admin turns it on under Manage apps → Change Record
→ Configure: *Record configuration changes*.

**What it records.** Changes to workflows, workflow schemes, permission
schemes, custom fields, and the other administrative objects Jira's audit
log covers, read from the site's audit log once an hour. Each record says
what changed, who changed it and when, in the same grid under the
**Configuration changes** tab, with its own hash chain and its own line in
the verification report.

**Who sees it.** Jira administrators only. The tab is not shown to other
users, and shared views and share links never include configuration
records.

**From when.** From the first hourly read after the toggle is switched on.
Nothing earlier is fetched.

**What each record holds.** What Jira's audit log reports for the event:
the summary, the category, the object (type and name), who, when, and the
changed values the log lists as field, from and to. The audit log does not
carry a full copy of a workflow or scheme before and after, so neither
does the record. The app reads the audit log and writes nothing to it.

**Turning it off** stops new records. Existing configuration records stay
until retention expires them.
