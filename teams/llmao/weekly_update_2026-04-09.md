# Weekly Update — Apr 9, 2026

**Team:** LLmao
**Product:** [rekindled.social](https://rekindled.social)

> First update — one-time Thursday cadence per the assignment. Tuesdays from here on.

## What we built last week

- **Growth Strategy Doc — Part 1.** Picked our three acquisition channels (short-form content, campus / community seeding, referral loop), wrote the approach and success metrics for each, and submitted on Apr 2. See `20260402/growth_strategy.md`. Why: we needed a real plan before turning on spend or seeding, not a "let's try TikTok" reflex.
- **Analytics installed end-to-end.** GA4 (acquisition) and Amplitude (in-product events) are live with funnel events firing across sign-up, swipe, match-attempt, and confirm. Why: without granular events we'd only know that people drop off, not where.
- **`/api/metrics` and `/api/user-count` endpoints shipped.** Public, no-auth, pulling live from the database. Registered the URL in `20260402_api-metrics.md`. Why: powers the class leaderboard and forces us to keep the live numbers honest.

## What we're building this week

- **Hit 20+ real users through the funnel by Thursday.** Mix of channels — campus outreach + the first short-form posts + warm-network. Why: the assignment floor, and more importantly the first time we'll have real funnel data instead of synthetic.
- **Track A user testing (3–5 sessions on strangers, $10/session).** Recruit through Reddit / Columbia students we don't know. Why: friends are polite; strangers click the wrong things and that's the data we need before pitch week.
- **Cold-start strategy.** Pick our cold-start type, name our hard side, and commit to a primary + secondary play. Why: density is the biggest open risk for this product and we haven't named the plan in writing yet.

## Current user count

Per `/api/metrics` at `rekindledapp.netlify.app/api/metrics`. Single digits going into this week — most existing accounts are seeded from internal testing. The whole point of the next 5 days is to make this number real.

## Biggest blocker

**Density, not traffic.** We can drive visits; what we can't yet do is concentrate enough users on the *same* event in the *same* week to make a group form. Until that's solved, every other metric is leading or lagging this one.
