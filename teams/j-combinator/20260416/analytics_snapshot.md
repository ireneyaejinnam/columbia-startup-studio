# Sift — Funnel Analysis

**Period:** Apr 6 – Apr 30, 2026
**Data sources:** Supabase `auth.users` (signups), in-app `analytics` table (Amplitude + Firebase mirrored to Supabase). GA4 acquisition tracking is not yet wired (no UTMs on share links, no install attribution), so channel-level conversion is omitted this cycle.

---

## Screenshots of our dashboards

**Amplitude — Live Events**

![Amplitude Live Events dashboard](Screenshot%202026-04-30%20at%202.37.53%E2%80%AFPM.png)

**GA4 (Firebase) — Events: Event count by name (Apr 2 – Apr 29, 2026)**

![GA4 Events dashboard — 2,433 events / 14 users](Screenshot%202026-04-30%20at%202.38.00%E2%80%AFPM.png)

**GA4 (Firebase) — Analytics Overview**

![Firebase analytics overview](Screenshot%202026-04-30%20at%202.38.09%E2%80%AFPM.png)

---

## Funnel

| # | Step | Users | Step conversion |
|---|---|---|---|
| 1 | Signed up (auth) | 25 | — |
| 2 | Opened app at least once | 16 | 64% |
| 3 | Viewed recommendations | 13 | 81% |
| 4 | Tapped a card to open event detail | 8 | 62% |
| 5 | Took a terminal action (going / save / ticket / calendar) | 11 | 138%* |

*Step 5 exceeds Step 4 because some users reach a terminal action via a shared event link, which deep-links straight into a formatted event detail and bypasses the discover feed entirely.

**Supporting counts (unique users):** `event_going` 7, `event_saved` 7, `ticket_click` 9, `calendar_export` 4, `share_tap` 3.

## Where is the biggest drop-off?

Two real drops, one tracking gap.

1. **Signup → first app open: 25 → 16 (36% never returned).** Largest absolute drop in the funnel.
2. **Recommendations viewed → card tap: 13 → 8 (38% in-app drop).** Largest mid-funnel drop among users who actually engage.
3. **Share-tap is the quiet bottleneck: only 3 of 16 active users have ever shared an event.** We built universal links that route directly into a formatted in-app event detail — but the upstream share *trigger* is rarely pulled, so the link landing experience is barely being exercised.

## What do we think is causing it?

- **The 25 → 16 gap** is mostly first-launch friction. Onboarding events (`onboarding_started` = 6, `onboarding_complete` = 4) only fired for users who joined after we added that tracking, so we can't measure the onboarding step directly yet, but the 9 users who never returned almost certainly never finished setup. Several signed up via Google, which routes into a five-step preference flow before they ever see a recommendation.
- **The 13 → 8 recs→card drop** suggests the cards themselves aren't pulling enough weight. We recently raised the scoring threshold to 5+ to filter out low-quality scraper events, which helped relevance but cut volume — users may be scrolling past a thin feed without a card grabbing them.
- **The low share rate** is likely because there is no clear in-app moment that prompts sharing. The share button exists on event detail but isn't surfaced after a positive signal (e.g., right after marking "going").

## What will we do about it?

1. **Cut onboarding from 5 steps to 2** (interests + neighborhood). Defer vibe / budget / free-time selection to first contextual use. Target: lift Step 1 → Step 2 from 64% to 75%+ on the next cohort.
2. **Prompt share immediately after `event_going`.** Treat a "going" tap as the highest-intent moment and surface a one-tap share sheet. The shareable-link plumbing already exists; we just need to fire it at the right moment. Target: 3 → 10+ unique sharers next cycle.
3. **Wire GA4 acquisition properly this week** — add UTMs to all share-link URLs, verify `gtag` config, confirm install attribution. Without this we can't compare Reddit vs Instagram DM vs share-link traffic, and every cohort going forward should answer that.
4. **Revisit the scoring floor** for users who scroll past 3+ cards without tapping — temporarily widen recommendations rather than show a thin feed. Target: lift Step 3 → Step 4 from 62% to 75%+.

*Numbers are small, but the signal is clear: the leak is at activation (signup → return) and at the share moment, not at the link landing experience we just built.*
