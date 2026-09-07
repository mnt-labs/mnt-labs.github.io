# Install

**Who installs:** a Jira site admin, from the Marketplace listing. There is
nothing to configure afterwards. The app starts recording the moment it is
installed.

**Where it appears**

- **Apps → Change Record** — the cross-project grid: every recorded change,
  filterable, exportable.
- **A "Change Record" tab on each work item** — that item's records only.
- **Manage apps → Change Record → Configure** (Jira admins only) — retention,
  the configuration-changes toggle, the verification report, the erasure
  status.

**What it records:** every field change on every work item, from the moment
of install forward, plus the creation and deletion of work items. Each record
carries the project, the work item, the field, the old value, the new value,
who made the change (as an Atlassian account ID, resolved to a display name
when shown) and when.

**What it does not record:** anything that happened before the install.
Jira's own History tab on each work item holds the past. The app never
backfills, so the first record you will see is the first change after the
install (the grid's "Since install" preset starts there).

**Free and paid**

| | Free (sites up to 10 users) | Paid |
|---|---|---|
| Grid, filters, exclusions, saved and shared views | yes | yes |
| Export size | up to 500 rows | up to 100,000 rows per file |
| Scheduled delivery | no | daily or weekly |
| Retention | 90 days, fixed | chosen by an admin: 30 to 730 days, or keep everything |
| Verification report | yes | yes |

The cap on a paid export is 100,000 rows per file. A wider window exports in
parts: narrow the date window and run it again.

**Permissions the app asks for:** read access to work items and their
history, read access to the site's audit log for the optional configuration
record, and permission to read your list of browsable projects on your
behalf. It has no permission to write anything in Jira.

**Nothing leaves your site.** The app runs entirely on Atlassian's
infrastructure ("Runs on Atlassian"). It has no external services, no
analytics, and no network egress of any kind. Records are stored in Forge
Storage inside your Atlassian site.
