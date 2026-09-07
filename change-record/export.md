# Export and the settings sheet

Any filter, saved view or shared view can be exported as **CSV** or
**XLSX**.

**How it runs.** The export is prepared on Atlassian's infrastructure, not
in your browser: the grid shows progress, and a download button appears
when the file is ready. You can keep working, or close the tab and come
back. Large exports on a busy site take longer because the app waits its
turn for storage reads rather than failing.

**Size.** One export renders up to **100,000 rows**. If the window holds
more, the export stops with a clear message instead of a half file: narrow
the date window and export the parts. On the free tier an export is capped
at 500 rows.

**What is in the file.** One row per recorded change, with these columns:
When (UTC), Issue, Project, Field, Field id, From, To, By, By (account
id), Source, Redacted, Seq, Hash. Creation and deletion appear as records
whose field is *created* or *deleted*. Columns are fixed; there is no
template to edit, so every export from every site has the same shape.

**How long the file waits.** A finished export stays downloadable inside
the app for 7 days; after that, run it again.

**The "Export settings" sheet.** Every XLSX carries a second worksheet
that says what produced the file, so a reader six months later does not
have to guess. Its rows:

- Generated at (UTC), Requested by, Format, Rows
- Window from, Window to, Window preset (a relative preset shows the exact
  bounds this run used)
- Projects, fields and people included and excluded
- Value, Old value, New value filters
- Scoped to — "every project", "the projects listed", or "the N projects
  the requester can browse"
- Tier, Records start (the app's first record on this site), Retention
- Chain verification — the last verification result and when it ran
- Produced by — the app version, and the line "inside this Atlassian site;
  nothing left it"

A CSV has no second sheet; the same rows are shown in the app under the
download and are kept with the export job.

**The digest.** Under the download the app prints the file's SHA-256. See
[The file digest](digest.md).

**Names.** People are stored as Atlassian account IDs and shown by display
name at export time. A person whose Atlassian account has since been
closed appears as redacted; see [Verification](verification.md).
