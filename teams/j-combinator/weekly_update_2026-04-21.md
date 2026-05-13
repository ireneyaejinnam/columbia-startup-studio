# Sift — Weekly Update
**Week of April 21, 2026**

---

## What We Built Last Week and Why

- **User-contributed events via URL submission** — users can paste any event URL (Instagram, Eventbrite, Luma, etc.) into the app. The `/api/submit-event` endpoint fetches metadata from the URL, extracts structured event data via GPT-4o-mini, matches against existing events to avoid duplicates, and routes it to the right table. We built this because our pipelines can't see everything — word-of-mouth events shared via Instagram or group chats are exactly the kind of thing Sift should surface, and users are the best source for those.
- **Per-event interaction tracking** — `user_event_interactions` table now records impressions, skips, saves, going, and shares per user per event. Permanently hidden events (hard dislike) never resurface. This gives the recommendation engine event-level signal, not just category-level signal.
- **Neutral skip ("not now")** — a third swipe state beyond like/dislike. "Not now" temporarily suppresses an event with a `suppressed_until` timestamp so it can resurface later. We added this because hard-dismissing an event because you're busy this weekend is different from not being interested — conflating the two was hurting recommendation quality.
- **Gesture tutorial overlay** — a 4-second animated overlay on first use showing left-swipe to discard and right-swipe to save. Dismissed automatically or on tap. Added because Round 2 user testing showed ~40% of new users didn't discover swipe gestures on their own.
- **Plan tab drag-to-reorder** — users can now drag events into their preferred order within a day. Saves persist to Supabase via `user_plan_event_orders`. Added based on direct user feedback that the fixed order felt limiting.
- **Session persistence fix** — moved onboarding and guest flags from in-memory variables to AsyncStorage so they survive app restarts. Users no longer get kicked to the login screen on reopen.

## What We're Building This Week and Why

- **Committed event tracking** — mark when a user has actually clicked through to buy tickets (`committed` flag on `going_events`). This distinguishes "interested" from "actually going" and gives us a meaningful conversion metric beyond just saves.
- **Share sheet and deep links** — let users share events via a link that deep-links back into the app. Sharing is our primary organic growth mechanism.
- **Merged event feed** — unify scraper events and AI-discovered events into a single ranked feed. Right now they're in separate tables; users shouldn't need to know the difference.

## Current User Count

Live at [https://sift-mobile-two.vercel.app/api/user-count](https://sift-mobile-two.vercel.app/api/user-count)

## Biggest Blocker

**Image quality on AI-discovered events** — the 5-stage image fallback pipeline (validate → og:image → Tavily → LLM → Unsplash) still leaves some events with broken or irrelevant images. Working on improving the Tavily search query construction to get better image matches.
