# Where reminders go

Three channels. The first needs no setup at all.

## A comment on the page

On by default. The app comments on the page and mentions its author and
last editor, so Confluence notifies them.

The comment is visible to everyone who can see the page, and it contains
the date and the page's own words, nothing more.

Turn it off under *Space settings → Renewal & Review Dates*.

## Slack

A space administrator pastes an incoming webhook URL under *Space
settings*.

In Slack: create an app, turn on Incoming Webhooks, add one to the channel
you want, then paste the URL. Optionally add Slack member or group ids to
mention, comma separated.

One message goes to the channel per date, on the space's schedule.

## Email

Each person subscribes for themselves, under *My reminders* on the space
panel: their own address, their own notice periods.

This is the channel that reaches someone who has no Confluence licence,
which is often the person who actually owns the contract.

Nobody is subscribed by default. Every email carries an unsubscribe link,
and a one-click unsubscribe header that Gmail and Outlook act on.

A subscriber's notice periods are their own and do not change what the
channel receives.


[Documentation](index.md) · [Privacy policy](privacy.md) · [Terms](terms.md) · [MNT Labs](../)
