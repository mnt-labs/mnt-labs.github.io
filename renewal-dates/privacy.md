# Privacy policy — Renewal & Review Dates for Confluence

*MNT Labs, effective 2026-09-25. This policy covers the Confluence Cloud app
"Renewal & Review Dates for Confluence" (the app), published on the
Atlassian Marketplace by MNT Labs.*

## The short version

The app finds dates already written in your Confluence pages and reminds
people about them before they pass. Most of it runs inside your Atlassian
site. Two things leave it, and only when you ask for them: an email
reminder, and a Slack message. Both are described below by name.

MNT Labs has no servers, no analytics and no database of its own. We never
read your pages.

## What the app stores, and where

Everything the app keeps is in your site's Forge Storage, under Atlassian's
terms, and Atlassian deletes it when you uninstall the app.

**Detected dates**, stored as a content property on the page they were
found on: the date, the words next to it that name it, one sentence from
the page for context, and whether it is being watched. This is a copy of
what the page already says.

**Per-space settings** chosen by a space administrator: the notice periods,
the send hour and time zone, whether to comment on pages, and a Slack
webhook URL if one is configured.

**Per-person subscriptions**, created by each user for themselves: their
Atlassian account ID, the email address they typed, and their own notice
periods.

**A record of what was sent**: which date, on which day, through which
channel, and to which address. This is what answers "was anyone actually
told", which is the question that follows a missed renewal.

**The app's own environment identifier**, so a reminder can link back to the
page that turns it off.

The app stores Atlassian account IDs. It does not look up names or email
addresses from Confluence, and holds no permission that would let it.

## What the app reads

The app holds these permissions, and nothing more:

- read pages, spaces and content summaries, to find dates and to name the
  page a reminder is about
- read and write content properties, to record the dates it found
- write a comment, to post a reminder on the page and mention its author
- app storage

It deliberately does NOT hold `read:confluence-user`, the permission that
would give it every user's name and email address. When the app mentions
someone in a comment, it uses their Atlassian account ID and Confluence
resolves it. The app never learns who they are.

The app reads the body of a page to find dates in it. It does not store the
body.

## What leaves your Atlassian site

Two things, and only when you have asked for them.

**Email reminders, through Resend** (Resend Inc., resend.com). When someone
subscribes to email reminders, the app sends Resend the address they
entered, the page title, the date, and the sentence of context from the
page. Resend delivers the message and is our sub-processor for that. Nobody
subscribes by default: the app sends no email at all until a person enters
their own address.

**Slack messages, when a webhook is configured.** If a space administrator
pastes a Slack incoming webhook URL, the app posts the page title, the date
and a link to the page into that Slack channel. The webhook points at your
own Slack workspace; MNT Labs is not part of that exchange.

Nothing else leaves. There is no analytics, no telemetry, no error
reporting service, and no connection to any MNT Labs server, because there
is no MNT Labs server.

## Comments on pages

By default the app posts its reminder as a comment on the page itself and
mentions the page's author and last editor, so Confluence notifies the
people who can act. The comment is visible to everyone who can see the
page, and it contains the date and the page's own words, nothing more. A
space administrator can turn this off under Space settings.

## Retention

Detected dates live on the page as a content property and go when the page
or the app does. Subscriptions live until the person unsubscribes, which
removes the record rather than disabling it. The record of what was sent is
kept so the history stays answerable.

Uninstalling the app removes all of it: Atlassian deletes app storage and
the app's content properties when an app is uninstalled.

Resend holds sent email according to its own retention; see resend.com.

## Your rights

The data here is your Atlassian site's data, held under your agreement with
Atlassian. For a request about a specific person, write to
support@mnt-labs.com and tell us the site and the space; we will tell you
what the app holds and remove it.

## Changes

If this policy changes materially, the new version is published here with a
new effective date, and the listing is updated.

## Contact

support@mnt-labs.com
MNT Labs, 790 Rue William, Montréal, Quebec H3C 0Y4, Canada


[Documentation](index.md) · [Terms](terms.md) · [Support](../support.md) · [MNT Labs](../)
