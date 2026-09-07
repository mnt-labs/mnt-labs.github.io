# Filters and exclusions

The grid shows every recorded change across every project you can browse.
Filters narrow it down. Every filter chip is either **is** or **is not**, so
you can include a set of projects, fields or people — or exclude them.

**Dimensions**

- **Project** — include or exclude any number of projects.
- **Field** — include or exclude any field, including status, assignee,
  priority, custom fields, and the lifecycle events *created* and *deleted*.
- **Person** — include or exclude whoever made the change.
- **Value** — text that must appear (or must not appear) in the old value,
  the new value, or either side. The same box takes a transition, see
  [Transitions](transitions.md).

Excludes combine with includes: "projects PAY and OPS, field is not
Description, person is not the automation account" is one filter.

**The count** in the toolbar is the number of rows the current filter
matches, and it updates as you change the filter. Next to it is how long
the query took.

**The date window**

Presets: Today, Yesterday, Last 7 days, Last 30 days, Last 90 days, This
month, Last month, and **Since install** (from the first record the app
holds). Or pick two dates. A preset is relative: a saved view with "Last 7
days" always shows the last seven days when it is reopened. Windows are
evaluated in UTC; an export prints the exact bounds it used.

**When the grid is empty, it says why**

- *Before the first record* — the window ends before the app was installed.
  Jira's History tab holds the past.
- *Your excludes removed every row* — the same filter without its excludes
  has rows. One click removes the excludes.
- *No value matched* — the same filter without its text filter has rows.
- *Nothing in this window* — try a wider preset.
- *Nothing you can browse matches* — see [First open](first-open.md).
- *Still looking* — a text filter over a wide window is being walked page
  by page; the grid shows what it has and keeps going.
