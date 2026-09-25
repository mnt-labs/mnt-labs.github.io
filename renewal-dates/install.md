# Install

Install the app. There is no setup step, and no configuration screen to
work through before anything happens.

## What happens immediately

Any page carrying a date is read as it is created or edited, and the dates
in it are watched. Nothing is typed twice: the app reads the page, not a
form.

## Who hears about it first

**Whoever wrote the page.** The app posts its reminder as a comment on the
page itself and mentions the author and the last editor, so Confluence
notifies them the way it notifies anyone else.

That happens with nothing configured, which is the point. Slack and email
are additions to it, not prerequisites.

A space administrator can turn page comments off under *Space settings →
Renewal & Review Dates*.

## What the app asks for

Permission to read pages and spaces, to write a content property recording
the dates it found, and to write a comment.

It deliberately does not ask for `read:confluence-user`, the permission
that would hand it every user's name and email address. When it mentions
someone, it uses their Atlassian account id and Confluence resolves it.


[Documentation](index.md) · [Privacy policy](privacy.md) · [Terms](terms.md) · [MNT Labs](../)
