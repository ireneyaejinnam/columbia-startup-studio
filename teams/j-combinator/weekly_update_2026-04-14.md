# Sift — Weekly Update
**Week of April 14, 2026**

---

## What We Built Last Week and Why

- **Adaptive taste profile** — the recommendation engine now updates in real time as users swipe. Every like, dislike, save, and "going" adjusts category weights (0.3–2.0 multipliers), tag weights, borough weights, and price preferences stored in both AsyncStorage (instant, offline) and Supabase (cross-device sync). We built this because a static onboarding profile goes stale fast — the feed needs to reflect what you actually engage with, not just what you said you liked on day one.
- **AI event discovery pipeline** — Claude Sonnet discovers events via web search every 3 days; GPT-4o-mini enriches each one with structured metadata (title, category, dates, venue, price, image, tags). This runs automatically via GitHub Actions and feeds a separate `ai_events` table that merges with scraper events in the app. We added this because scrapers only find events from sources they know about — the AI pipeline surfaces niche and emerging events that don't show up on Ticketmaster.
- **Hook text generation** — GPT-4o-mini writes a one-line "hook" for every event card. Events without compelling copy don't get tapped. This runs as part of the AI pipeline cron.
- **Vibe scoring** — each scraper event gets a 1–10 quality/relevance score via GPT-4o-mini. We use this to suppress low-quality events before they reach the feed.
- **Sessions support** — multi-date and multi-location events now store individual occurrences (`sessions` JSONB column). This was needed for theater runs, museum exhibitions, and recurring events that span weeks.

## What We're Building This Week and Why

- **User-contributed events** — let users submit an event URL (Instagram post, Eventbrite link, etc.) and have the app extract and add it. This expands coverage beyond what any pipeline can find and gives power users a reason to stay engaged.
- **Per-event interaction tracking** — a `user_event_interactions` table to track impressions, skips, saves, going, and shares per user per event. This feeds the recommendation engine with richer signals than just category weights.
- **Gesture tutorial overlay** — a first-use overlay showing swipe gestures. User testing showed many users didn't know they could swipe left to discard.
- **Plan tab drag-to-reorder** — let users reorder their saved events. Came out of user testing feedback.

## Current User Count

Live at [https://sift-mobile-two.vercel.app/api/user-count](https://sift-mobile-two.vercel.app/api/user-count)

## Biggest Blocker

**Session persistence bug** — logging in and closing/reopening the app sends users back to the login screen. Root cause: onboarding and guest flags were stored as in-memory variables that reset on every app restart. Supabase correctly restores the session but the routing logic fails. Fix in progress.
