# Privacy policy — Change History for Jira

*MNT Labs, effective 2026-09-07. This policy covers the Jira Cloud app
"Change History for Jira — Filter, Report & Export" (the app), published on
the Atlassian Marketplace by MNT Labs.*

## The short version

The app runs entirely inside your Atlassian site. It has no servers of its
own, no analytics, and no network connection to anything outside Atlassian.
MNT Labs never receives, sees or stores your data. Everything the app keeps
is in your site's Forge Storage, under Atlassian's terms, and is deleted
when you uninstall the app.

## What the app stores, and where

The app is built on Atlassian Forge and carries Atlassian's "Runs on
Atlassian" designation, which means it uses only Atlassian-hosted compute
and storage and egresses no data. Inside your site's Forge Storage it keeps:

- **Change records:** for each change to a work item after the app was
  installed, the project key, the work item key, the field, the old value,
  the new value, the time, and the Atlassian account ID of the person who
  made the change. Field values may contain personal data if your team
  types it into a field.
- **Configuration change records**, only if a Jira administrator switches
  them on: entries from your site's audit log (summary, category, object,
  changed values, time, account ID).
- **Saved views, export jobs and their files**, created by your users, with
  the account ID of the owner. Export files are kept for 7 days.
- **A per-user list of the projects that user can browse**, refreshed each
  time the user opens the app, so that the app can show them only those
  projects.
- **Settings** chosen by your administrators (retention, the configuration
  toggle).

The app stores Atlassian account IDs, never names or email addresses.
Display names are looked up from Jira at the moment they are shown.

## What the app reads

The app holds read-only permissions: to read work items and their change
history, to read the site's audit log for the optional configuration
record, and to read, on each user's behalf, the list of projects that user
can browse. It has no permission to change anything in Jira.

## What leaves your site

Nothing. The app makes no requests to any service outside Atlassian, sends
no email, has no webhooks, and contains no analytics or telemetry. Exports
are files your users download themselves from inside the app.

## Retention and deletion

Records are kept for the retention period set by your administrator: 90
days on the free tier, or a period between 30 days and "keep everything"
on the paid tier. Records older than the period are deleted inside your
site's storage. Uninstalling the app deletes everything it stored, under
Atlassian's Forge Storage rules.

## Closed Atlassian accounts

Once a week the app asks Atlassian which of the account IDs it references
belong to accounts that have been closed. For each closed account it
redacts, in place, the account ID and any stored field value that may
contain that person's data, leaving a marker so that the app's integrity
check still works. This is how the app meets Atlassian's user privacy
requirements for apps.

## Data controller and processor

Your organisation is the controller of the data in your Atlassian site.
Atlassian processes it as the host of Forge Storage under your agreement
with Atlassian. MNT Labs does not process, access or hold your data at any
point; the app's code runs in Atlassian's infrastructure on your site's
data alone.

## Support requests

If you contact us, we keep your message and our reply for as long as it is
useful to answer you, and nothing else.

## Changes to this policy

Changes are published on this page with a new effective date. A change that
would let the app send data outside your site would be a change to the app
itself, and would be announced in the app's release notes before it ships.

## Contact

MNT Labs, support@mnt-labs.com. See [Support](../support.md).
