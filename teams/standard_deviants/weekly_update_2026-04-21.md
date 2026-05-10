# Weekly Update — 2026-04-21

**Team:** Standard Deviants
**Product:** HAUNT — social events app for NYC

## What we built last week and why

Map screen is done (Leaflet on web, native maps on iOS/Android with category filtering and event pins), and the Venue screen now shows upcoming events at a given venue. We extended the scraper pipeline with SeatGeek and a few NYC-specific sources (Oh My Rockness, The Skint) to thicken the long-tail event data we flagged two weeks ago. The biggest internal lift was wiring up the `/api/metrics` endpoint and getting GA4 + Amplitude installed with funnel events firing on every step of the acquisition + signup + activation flow — not just "signup completed." We needed that granularity before the Reddit Ads ran or we'd be flying blind on where people drop.

Demand gen launched for real: the Reddit Ads campaign went live across r/nyc, r/AskNYC, r/Columbia and the NYC events subs at $15/day, and the personal-graph DMs are mid-cycle.

## What we're building this week and why

The Going-Out Status toggle and the "Who's Out" screen — the original wedge feature. Feature freeze is **April 23**, so this is the last week we can ship anything new. Anything not done by Thursday becomes post-Demo-Day. Also bug-bashing onboarding because the small-N testing already exposed a confusing first minute.

## Current user count

11 signups, 6 active users (per our `/api/metrics` definition: did at least one meaningful action — log, message, or going-out toggle), 1 friend cluster.

## Biggest blocker

The feature freeze deadline. We have to land Going-Out Status this week or drop it entirely from the Demo Day story, and it's the most distinctive thing in the product. Trading off polish on the existing screens vs. shipping the new feature is the daily tension.
