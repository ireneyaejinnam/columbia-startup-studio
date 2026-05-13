# Demand Test Plan — QuestCity

**Team:** Team Millionaires (DG-ST-AB)
**Date:** February 26, 2026
**Budget:** ~$200 (~$40/day × 5 days)
**Platform:** Meta (Instagram + Facebook) Ads

---

## Audience

**Target:** NYC-based adults aged 24–34 who follow accounts in the categories:
- Local NYC food/coffee/lifestyle (e.g., @infatuation, @timeoutnewyork)
- Outdoor/fitness (e.g., running clubs, hiking NYC)
- Dating/relationships (e.g., date night content creators)

**Location targeting:** New York City — specifically Manhattan, Brooklyn, Queens (3 boroughs for launch)

**Exclusions:** tourists, travel content followers, people outside NYC

---

## A/B Message Angles

### Angle A — The Game Frame
**Hook:** "What if your weekend had a quest?"
**Visual:** Mock quest card UI — "Coffee Connoisseur: Visit 5 indie coffee shops in Brooklyn"
**CTA:** "Join the waitlist → questcity-millionaires.netlify.app"

### Angle B — The Guilt Frame
**Hook:** "You've lived in NYC for 3 years. How much of it have you actually seen?"
**Visual:** Split — Google Maps saved places (long list, none checked off) vs. QuestCity quest completion badge
**CTA:** "Start exploring → questcity-millionaires.netlify.app"

---

## Budget Allocation

| Day | Spend | Focus |
|-----|-------|-------|
| Day 1–2 | $40/day | Run both angles equally — A/B split |
| Day 3 | $40 | Pause weaker angle; double down on winner |
| Day 4–5 | $40/day | Run winner only; test 1 variation of creative |

**Total:** ~$200

---

## Success Threshold (Committed in Advance)

We will interpret results as **meaningful demand** if we hit:
- **Waitlist sign-up rate ≥ 8%** of clicks (i.e., 8 in 100 people who click sign up)
- **Total sign-ups ≥ 40** from paid traffic over 5 days
- **Cost per sign-up ≤ $5**

If we hit these thresholds, we proceed to building. If we don't, we revisit the message before spending more.

---

## Pre-Flight Checklist

- [x] Conversion works end-to-end (thank-you shown after waitlist signup)
- [x] UTMs on every ad link (`?utm_source=meta&utm_medium=paid&utm_campaign=Team_QuestCity_AngleA_Feb26`)
- [x] Static creative ready (1 image per angle — designed in Canva)
- [x] Clean naming convention: `Millionaires_QuestCity_AngleA_Feb26` / `...AngleB_Feb26`
- [ ] Pixel installed on landing page (in progress — adding Meta Pixel this week)

---

## Tracking

- **Primary metric:** Waitlist sign-ups (Netlify form + UTM params)
- **Secondary metric:** Click-through rate on each ad (Meta Ads Manager)
- **Traffic source breakdown:** GA4 → Acquisition → Source/Medium

We will report results at the next class session.
