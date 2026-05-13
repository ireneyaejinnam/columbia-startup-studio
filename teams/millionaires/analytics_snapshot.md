# Analytics Snapshot — QuestCity

**Team:** Team Millionaires (DG-ST-AB)
**Date:** April 16, 2026

---

## 1. Dashboard Screenshots

*GA4 Acquisition Overview and Amplitude Event Segmentation screenshots — see `/analytics_screenshots/` folder. Key numbers pulled below.*

**GA4 Summary (last 30 days):**
- Sessions: 287
- Users: 194
- Avg. session duration: 1m 42s
- Bounce rate: 58%
- Top sources: Direct (44%), Instagram (31%), Reddit (18%), Other (7%)

**Amplitude Summary (in-product events, last 30 days):**
- App opens: 44
- Quest board views: 38
- Quest detail views: 29
- Check-in attempts: 21
- Check-in completions: 14
- Quest completions: 9

---

## 2. Funnel with Actual Numbers

**Critical path:** Landing page → Sign up → Quest board → Quest detail → Check-in → Quest completion

| Step | Count | Conversion (step-to-step) |
|------|-------|--------------------------|
| Landing page visitors | 287 | — |
| Waitlist / sign-ups | 44 | **15%** |
| App opens (signed-up users) | 44 | 100% |
| Quest board views | 38 | **86%** |
| Quest detail views | 29 | **76%** |
| Check-in attempts | 21 | **72%** |
| Check-in completions | 14 | **67%** |
| Quest completions (all stops) | 9 | **64%** |

**Overall funnel:** 287 landing page visitors → 9 quest completions = **3.1% end-to-end conversion**

---

## 3. Written Analysis

**Where is the biggest drop-off?**

The biggest drop-off is between landing page visitors (287) and sign-ups (44) — a 15% conversion rate. 85% of people who see the product don't sign up for it.

**What do we think is causing it?**

Two factors based on user testing and landing page behavior:
1. **The product wasn't live when most visitors first hit the page.** The "Launching in NYC in March 2026" copy is stale — we're past March and people assume they missed it. This creates doubt about whether the product is real.
2. **The waitlist CTA has low urgency.** "Join the waitlist" implies waiting, not acting. People who sign up immediately came from warm channels (DMs, word of mouth). Cold traffic (Reddit, Instagram ads) converted at roughly 8% — half the overall rate.

**What will we do about it?**

We've already replaced stale launch copy with "Now live in NYC" and updated the CTA to "Start your first quest →". We expect this to improve the 15% conversion rate. We'll measure the delta over the next 2 weeks.

The second-biggest drop-off is between check-in attempts (21) and check-in completions (14) — 33% of people who try to check in don't finish. We believe this is partly photo upload friction (slow on older devices) and partly location confusion (they're not physically at the spot). We're monitoring this but not changing the mechanism before Demo Day.

**Numbers + insight + action:**
- 287 visitors → 44 sign-ups (15%). Stale copy + weak CTA is the cause. Updated both. Watching the delta.
- 21 check-in attempts → 14 completions (67%). Upload friction + location uncertainty. Monitoring post-Demo Day.
- 9 quest completions is our north star metric. Every one of those 9 people went outside and found something new. That's real.
