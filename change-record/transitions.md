# Transitions

A transition is a change from one specific value to another: every time a
status went from *In Review* to *Done*, or an assignee changed from one
person to another.

**Shorthand.** In the value box, type the two values separated by an arrow:

```
To Do -> Done
```

Press Enter or Run. The filter then matches rows whose old value contains
the left side and whose new value contains the right side. Either side may
be left empty: `-> Done` finds every change *into* Done from anywhere.

**The two boxes.** The same filter is available as two fields, "old value
contains" and "new value contains", for values that themselves contain an
arrow.

**Observed transitions.** The grid's Status column filter lists the
status transitions actually present in the rows loaded, as "From → To"
with counts, so you can pick one rather than type it.

**Saved views and share links carry the transition** with the rest of the
filter, and the export's settings sheet prints it under *Old value* and
*New value*.

Matching is "contains", case-insensitive, on the stored text of the value.
A status is stored by its name, a person by their account ID (shown as a
name); to match a person in a transition, filter on the Person dimension
instead.
