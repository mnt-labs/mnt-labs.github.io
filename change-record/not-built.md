# What is deliberately not built

These are decisions, not gaps. Each keeps the app read-only, keeps your
data on your site, or keeps the app simple enough to work without a support
desk. Asking will not change them; this page saves you the message.

**Restore, undelete, revert, bulk edit.** The app never writes to a work
item, a field, a workflow or a user. It records who deleted a work item and
when; bringing it back is a task for Jira itself or for a tool that
accepts write permissions.

**Backfill of history before the install.** The record starts at install.
Jira's History tab on each work item holds everything before that. A
backfill would be a copy of Jira's changelog, taken at high load, with no
way to prove it complete.

**A template editor.** Every export has one fixed shape. The day the
columns are editable, every site has its own report to support.

**Email, Slack, webhooks, or any destination.** Nothing leaves your
Atlassian site. Scheduled runs produce a file inside the app; you download
it. There is no address to get wrong and no third party to trust.

**Alerts on changes.** The app is a record, not a monitor.

**An API, a Confluence macro, a dashboard gadget.** Export the file and use
it where you need it.

**A permissions page.** You see the projects you can browse in Jira, and
nothing else. There is nothing to configure and no way to widen it.

**Compliance certificates or attestations.** The app gives you a filtered,
verifiable record. Whether it satisfies an auditor is between you and the
auditor; the app does not claim SOX, SOC 2, ISO, NIS2, DORA or any other
conformity on your behalf.

**Tamper-proof storage.** The hash chain shows whether stored records have
changed since they were written. It does not stop a site admin with storage
access from changing them, and the app does not say it does.

**Storing people's names.** Only Atlassian account IDs are stored; names
are looked up when shown. When an account is closed, the app redacts what
it holds for that person.

**Anything that needs a call to set up.** If a feature would need us to
configure it with you, it is not in the app.
