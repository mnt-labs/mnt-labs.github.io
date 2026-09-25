# What counts as a date

The app reads the page, not a form. It recognises:

| Shape | Example |
|---|---|
| A sentence | `The agreement expires on 31 December 2026` |
| A key/value table row | `Renewal deadline` / `2026-09-12` |
| A register: one row per item, a column of dates | `Aurora Cleaning` … `2026-11-03` |
| A Confluence date picker | the inserted date element |
| A task due date | `Renew the policy before <date>` |

Day-first and month-first formats, written months in English and French,
and the ISO form. A date whose day and month are both plausible is flagged
as ambiguous rather than guessed at.

## What it ignores

Dates in the past. Version numbers that look like dates (`2.10.2025`).
Tasks that are already ticked: reminding someone about work they finished
is the fastest way to have an app muted.

## What it decides on its own

A date next to words like *expires*, *renewal* or *review due* is watched
straight away.

A date with nothing to say what it is appears as a suggestion, and one
click starts watching it.

A date next to *signed* or *effective* is read as a past event, not a
deadline, so a contract's signature date does not become a reminder.

## Labels

The words next to the date become its name. In a register the row is named
by its first cell, so a reminder says "Aurora Cleaning" rather than the
name of the column or of whoever owns the line.


[Documentation](index.md) · [Privacy policy](privacy.md) · [Terms](terms.md) · [MNT Labs](../)
