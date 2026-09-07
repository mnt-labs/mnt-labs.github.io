# First open and the consent prompt

The first time you open Change Record, Jira shows one prompt asking you to
let the app act on your behalf. Accept it once and it does not come back.

**Why it asks.** You only ever see changes in the projects you are allowed
to browse in Jira. To know which projects those are, the app asks Jira *as
you*, not as the app. That is the one thing the consent covers. It grants
the app nothing it could use to change anything: every permission the app
holds is read-only.

**What you see afterwards**

- The footer of the grid says either **"Jira administrator · every
  project"** or **"Scoped to the N projects you can browse"**.
- The project picker offers only the projects you can browse.
- An export, a saved view someone shared with you, and a share link all
  apply the same rule. A colleague opening your shared view sees their
  projects, not yours.
- The **Configuration changes** tab appears only for Jira administrators.

**If you see "Nothing you can browse matches"**, the record has rows but
none of them are in a project you can browse. Ask a Jira admin for access to
the project you are looking for; the app has no permissions page of its own
and nothing to configure here.

**If you decline the prompt**, the grid cannot tell which projects are
yours and shows nothing. Reopen the app and accept it.

**Scheduled deliveries** run while you are not there, so the app keeps a
snapshot of your browsable projects from the last time you opened it. If
you have not opened the app in 30 days, a scheduled run is skipped and the
view says so: "open the app once so it knows which projects you can
browse". Opening the app refreshes the snapshot.
