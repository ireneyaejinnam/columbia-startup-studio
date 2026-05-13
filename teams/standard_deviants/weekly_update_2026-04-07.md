# Weekly Update — 2026-04-07

**Team:** Standard Deviants
**Product:** HAUNT — social events app for NYC

## What we built last week and why

Most of the sprint went into the foundation that everything else hangs off of. We finished the Supabase schema (16 tables — events, profiles, friendships, friend groups, event logs, chat, etc.) with RLS policies and indexes, plus a trigger that auto-creates a profile on signup so we don't have to do that bookkeeping in the client. Auth (sign up, email confirmation, sign in, sign out) is shipped end-to-end. The Explore screen — the asymmetric grid of NYC events with category + date filtering and pagination — is functional with real scraped data flowing in. We also got the Ticketmaster, Dice, and Eventbrite scrapers running with shared dedup/upsert logic, which means the "browse real events" promise from the MVP doc is real, not faked.

We picked these to do first because nothing else in the app works without auth + an event catalog + a way to view events. Everything social we want to build assumes those three are stable.

## What we're building this week and why

The Feed screen (paginated friend activity), the Event Detail screen with community logs, and the log-an-event flow (rating, notes, companion tagging, visibility control). This is the "social signal" half of the product — the part that actually differentiates us from Eventbrite. We need it live before our personal-graph DM push lands so testers have something to log against.

## Current user count

2 — pre-launch internal testing (founding team only).

## Biggest blocker

Event data coverage is uneven across categories. Music/concerts is dense (Ticketmaster + Dice fill it well), but nightlife, comedy, and community events are thin because we don't have great sources for them yet. We're triaging by adding Meetup + a few NYC-specific scrapers, but the long tail of niche sources is going to be ongoing work.
