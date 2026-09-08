# Privacy Policy — Where The Money Went (publishing tool)

Effective date: 7 September 2026

I'm Pranay Sethi. This page covers the private, personal-use software tool I
wrote and run myself to manage my own YouTube channel, **Where The Money
Went**. It is not a public product, not distributed to anyone else, and not
installed by anyone but me. This policy exists because Google's API Services
User Data Policy requires one for any app that requests access to Google
user data — even a single-developer, single-user tool like this one.

## Who this covers

Just me. I am the only person who uses this tool, the only owner of the
YouTube channel it publishes to, and the only holder of the Google account
and Cloud project the credentials belong to. There are no other users, no
sign-ups, and no accounts of any kind.

## What data the tool accesses, and why

The tool requests four Google API scopes, each used only against my own
channel:

- **`yt-analytics.readonly`** — reads my own channel's private analytics
  (views, watch time, subscriber gain/loss, traffic sources) so I can decide
  what to make next. The tool never writes analytics data.
- **`youtube.readonly`** — reads my own channel's and videos' public
  metadata (titles, stats, privacy status) so the tool can check its own
  prior work before acting again.
- **`youtube.force-ssl`** — updates video privacy status, titles,
  descriptions, tags, captions, thumbnails, playlist membership, and channel
  branding (banner, watermark, keywords) on my own channel only. Every write
  is read-modify-write against my own existing settings.
- **`youtube.upload`** — uploads new episodes of my own series to my own
  channel.

## How data is stored

Everything stays local to my own machine:

- OAuth tokens are cached in a `secrets/` directory that is excluded from
  version control and never transmitted anywhere except to Google's own
  token endpoint, to refresh the token.
- Analytics numbers I pull are stored in a local SQLite database that only I
  query, on my own machine.
- Nothing is uploaded to a server I run, shared with a third party, or used
  to build any kind of profile beyond my own channel's numbers.

## Data sharing and sale

I do not sell, rent, trade, or share any data obtained through the Google
APIs with any third party, for advertising or any other purpose. The only
"sharing" that happens is the intended one: publishing my own videos to my
own public YouTube channel, which I do deliberately, by hand, one episode at
a time.

## Limited Use disclosure

This application's use and transfer to any other app of information
received from Google APIs adheres to the [Google API Services User Data
Policy](https://developers.google.com/terms/api-services-user-data-policy),
including the Limited Use requirements.

**UNVERIFIED — exact wording.** I was not able to confirm the verbatim
required phrasing of this sentence against Google's current developer
policy page (fetch attempts returned summarized, non-verbatim text). The
sentence above is the commonly published template used by other developers
to satisfy this requirement; re-check it against
<https://developers.google.com/terms/api-services-user-data-policy> before
this page is treated as final, and correct the wording if it differs.

## Data deletion

Since all data lives only on my own machine, I control deletion directly:

- I can delete the local `secrets/` directory (removing the cached OAuth
  token) and the local SQLite database at any time, which removes all data
  this tool has stored.
- I can revoke this app's access to my Google account entirely at
  <https://myaccount.google.com/permissions>, which stops all future access
  immediately.

There is no other copy of this data anywhere else to delete, because none
was ever made.

## Changes to this policy

If what the tool does changes — a new scope, a new kind of data, a new
storage location — I will update this page to match before making that
change live.

## Contact

Pranay Sethi — pranaysethi19@gmail.com
