# Sift — Demand Test Plan

**Date:** February 25, 2026
**Goal:** Validate demand for Sift before building the product. Measure whether the target audience will give us their email (waitlist signup) when presented with the value proposition.

---

## Audience

**One audience, defined tightly:**

- **Location:** New York City (Manhattan + Brooklyn, expand to all 5 boroughs if budget allows)
- **Age:** 22–30
- **Interests:** Events, nightlife, arts & culture, fitness classes, food & dining, things to do in NYC
- **Behaviors:** Instagram-active, engaged with NYC lifestyle content, likely to click on local discovery content
- **Exclusions:** Tourists (exclude "traveling to NYC" behaviors), event organizers/promoters, people outside the 5 boroughs

**Platform:** Meta Ads (Instagram feed + stories). This is where the target audience already discovers events passively — meeting them in the exact channel where the problem lives.

---

## Two Angles

Run two ad variants pointing to the **same landing page** (or two variants of the landing page). The goal is to learn which emotional framing drives higher intent.

### Angle A: "Decision Fatigue" (Overwhelmed Planner frame)

**Ad copy:**
> You just spent 20 minutes scrolling six apps and you still don't know what to do this weekend.
>
> Sift gives you 3–5 things actually worth doing — matched to what you're into, when you're free, and how far you'll go.
>
> Join the waitlist →

**Visual:** Clean, minimal — the Sift logo on off-white with one recommendation card example (the Kehinde Wiley card or foraging walk). No lifestyle imagery. Let the copy do the work.

**Why this angle:** This is the #1 validated pain point across all 10 interviews. It targets overwhelmed planners (strongest converting bucket at 75%) and resonates across most segments.

**Landing page variant:** Hero headline = *"Stop scrolling six apps just to figure out what to do this weekend."*

---

### Angle B: "You're Missing It" (Culture Seeker / Discovery frame)

**Ad copy:**
> The best things happening in NYC this week are the ones you'll never hear about — until they're over.
>
> Sift tracks pop-ups, exhibitions, limited-run shows, and things that don't last forever. We'll tell you before they're gone.
>
> Join the waitlist →

**Visual:** One of the example cards showing "Ends in 5 days" urgency badge. Warm Stone accent color. Moody NYC photography in background (gallery interior or pop-up storefront).

**Why this angle:** Culture seekers hit 100% resonance and 75% conversion in V2 testing. The "information asymmetry" framing is emotionally distinct from Angle A and targets a different motivation (curiosity vs. fatigue).

**Landing page variant:** Hero headline = *"The best things in NYC are the ones you almost missed."*

---

## Budget

| Item | Cost | Notes |
|------|------|-------|
| Meta Ads — Angle A | $150 | 3–5 day run, optimize for link clicks |
| Meta Ads — Angle B | $150 | Same duration, same audience, A/B split |
| Domain + hosting | $12/yr | Vercel free tier + custom domain |
| Email capture tool | $0 | Formspree free tier, or Mailchimp free |
| **Total** | **~$312** | |

**Duration:** 5 days minimum. Aim for 500+ landing page visits per angle (1,000+ total) to get statistically meaningful conversion data.

**Expected CPM:** $8–15 for NYC-targeted Instagram (young professional interests). At $12 CPM average, $150 buys ~12,500 impressions per angle. At 2–4% CTR, that's 250–500 clicks per angle.

---

## Success Thresholds

### Primary metric: Waitlist conversion rate
(email signups ÷ landing page visits)

| Result | Interpretation | Next step |
|--------|---------------|-----------|
| **< 3%** | Weak signal. Copy or targeting needs work. | Rethink positioning or audience. Don't build yet. |
| **3–5%** | Moderate signal. Interest exists but not urgent. | Iterate copy, test new angles, consider narrower vertical. |
| **5–8%** | Strong signal. Real demand. | Start building MVP. Use winning angle for launch messaging. |
| **> 8%** | Very strong. Pent-up demand. | Accelerate. Consider raising pre-seed off this signal. |

### Secondary metrics (track but don't gate decisions on):

| Metric | What it tells you |
|--------|-------------------|
| CTR (ad → landing page) | Which angle hooks attention in-feed |
| Scroll depth | Whether people read past the hero |
| Category selection (quick-qualify question) | Which vertical has highest demand |
| Cost per email signup | Unit economics of future acquisition |
| Angle A vs. Angle B conversion gap | Which emotional frame to lead with |

### Tracking setup:
- **UTM parameters:** `?utm_source=meta&utm_medium=paid&utm_campaign=demand_test&utm_content=angle_a` (and `angle_b`)
- **Events to track:** page_view, scroll_25/50/75/100, cta_click, email_submit, category_select
- **Tools:** Google Analytics 4 (free) + Formspree or Mailchimp for email capture. If using Vercel, Vercel Analytics is also free.

---

## What we learn regardless of result

Even if conversion is low, we get:
1. **Which angle performs better** — decision fatigue vs. discovery. This shapes all future messaging.
2. **Category demand distribution** — the quick-qualify question tells us which vertical to build first.
3. **Cost per interested user** — baseline for future CAC modeling.
4. **Scroll depth** — if people bounce at the hero, it's a hook problem. If they read everything but don't convert, it's a trust problem.

---

## Timeline

| Day | Action |
|-----|--------|
| Day 0 | Finalize landing page, set up domain, email capture, analytics |
| Day 1 | Launch both ad variants |
| Day 3 | Check interim results — kill any ad set with <0.5% CTR |
| Day 5 | End test. Pull data. |
| Day 6 | Analyze: conversion rates, angle comparison, category breakdown |
| Day 7 | Decision: build, iterate, or pivot |
