# Sift — Weekly Update
**Week of April 28, 2026**

---

## What We Built Last Week and Why

- **Merged event feed** — scraper events and AI-discovered events now flow through a single unified feed. Migration `010_merge_ai_events.sql` consolidates both tables so the app queries one source with a `source_type` column (`scraper` vs `ai_discovery`). We did this because maintaining two separate query paths was creating inconsistencies in scoring and filtering — users shouldn't see a different quality of event depending on which pipeline found it.
- **Committed event tracking** — `going_events` now has a `committed` boolean that flips when a user clicks through to buy tickets. This is a meaningful conversion signal — "saved" is intent, "committed" is action.
- **Share sheet** — users can now share events via a generated link. The `/api/submit-event` endpoint handles inbound shared links, extracts the event, and routes the recipient into the app. Share events are tracked as `share_tap`, `shared_link_opened`, and `share_intent_received` in analytics. Sharing is our primary zero-cost acquisition channel.
- **Custom list ordering** — users can reorder their saved lists (not just events within a list). Sort order persists to Supabase. Small UX detail but came up repeatedly in user testing.
- **AI event name dedup with source URL** — added `source_url` unique constraint to `ai_event_name_list` so we don't re-enrich the same event URL across pipeline runs. Reduces LLM costs and prevents duplicate events.

## What We're Building This Week and Why

- **App Store submission** — submitting to Apple App Store this week. We have enough core functionality to get real users outside our test group, and real usage data is more valuable than another week of features.
- **Analytics expansion** — adding `dau_last_14`, funnel breakdown, and cohort retention to the `/api/metrics` endpoint. The basic signups/active_users numbers aren't enough to understand what's happening with users week over week.
- **taste profile v2** — expanding taste profiles with tag weights, borough weights, and price preferences. The current category-only model is too coarse.

## Current User Count

Live at [https://sift-mobile-two.vercel.app/api/user-count](https://sift-mobile-two.vercel.app/api/user-count)

## Biggest Blocker

**App Store review** — first submission. No blockers yet but App Store review turnaround is unpredictable. Have contingency plans to distribute via TestFlight if review is delayed.
