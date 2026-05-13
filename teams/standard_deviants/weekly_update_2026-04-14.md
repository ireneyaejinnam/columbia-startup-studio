# Weekly Update — 2026-04-14

**Team:** Standard Deviants
**Product:** HAUNT — social events app for NYC

## What we built last week and why

Feed, Event Detail, and the log-an-event flow shipped — users can now rate (1–10), add notes, tag companions, and choose who sees the log (private / friends / public). Profile screen is up too: stats, taste tags, going-out status badge, and event log history. We also got Chat working — real-time DMs via Supabase Realtime with event sharing, unread indicators, and a friend picker for new conversations. The 5-tab navigation (Explore, Map, Feed, Chat, Profile) is wired up with the stack navigator on top so deep links into events and venues work cleanly.

We pushed Chat earlier than originally planned because peer review feedback from Mar 26 made it clear that "share an event to a friend" was the natural next action after browsing — without it, the social loop didn't close.

## What we're building this week and why

Map screen polish (Leaflet on web, react-native-maps native), Venue detail pages, and starting on the Going-Out Status toggle — the "looking to go out tonight" nudge system that was the original product thesis. We're also kicking off the personal-graph DM campaign described in `20260402/growth_strategy.md`: 30 DMs across the founding team over 5 days, plus the first Reddit Ads creative going through review.

## Current user count

5 signups (3 active) — first wave of personal-graph DMs going out this week.

## Biggest blocker

Cold-start. The product's value is unlocked when you have friends on it, so isolated signups don't experience the actual product. We're trying to solve this with the "share with one friend group" ask attached to every personal DM, but we don't yet know how well that converts.
