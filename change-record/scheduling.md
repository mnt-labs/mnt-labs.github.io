# Scheduling (paid)

A saved view can be delivered on a schedule: **daily** or **weekly**. A
daily run exports the last day; a weekly run exports the last seven days,
regardless of the view's own window.

**Where it goes.** The app sends nothing anywhere. Each run produces a file
inside the app, and the view lists its runs with the row count, format and
the start of the SHA-256 digest; a run with no changes says "no changes".
The list keeps 30 days of runs. Nothing leaves your Atlassian site, so
there is no email, webhook or destination to configure, and no address
that could be wrong.

**Whose access applies.** A scheduled run uses the project access of the
person who owns the view, as last seen when they opened the app. If the
owner has not opened the app in 30 days the run is skipped and the view
says: "open the app once so it knows which projects you can browse". If
none of the view's projects are ones the owner can browse, the run is
skipped and says that instead.

**Size.** A run is an ordinary export and has the same cap: 100,000 rows
per file. A daily or weekly window on one site is normally far below it.

**Turning it off.** Set the view's schedule to none. Deleting the view also
stops it. Schedules belong to the view's owner; a view shared with the site
can be scheduled only by its owner.

**Free tier.** Scheduling is a paid feature. On the free tier the option is
shown but disabled.
