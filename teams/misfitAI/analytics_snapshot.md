# Analytics Snapshot

**Product:** misfitAI / Wardrobe Planner  
**Date:** April 16, 2026  
**Metrics endpoint:** https://misfitai-2026.web.app/api/metrics

---

## 1. Dashboard Screenshots

Dashboard screenshots still need to be added/exported for full compliance.

- **GA4 Acquisition Overview:** _Screenshot needed_
- **Amplitude Event Segmentation:** _Screenshot needed_

Suggested filenames once exported:

- `analytics/ga4_acquisition_overview.png`
- `analytics/amplitude_event_segmentation.png`

---

## 2. Funnel With Current Numbers

Current public metrics endpoint response:

```json
{
  "signups": 35,
  "active_users": 65,
  "waitlist": 0,
  "page_views": 207
}
```

## Critical Path

| Funnel Step | Count | Conversion |
|-------------|-------|------------|
| Landing page views | 207 | 100% |
| Account signups | 35 | 16.9% of page views |
| Active users | 65 | 185.7% of signups |

**Note:** Active users are higher than signups, which likely means the analytics definition includes anonymous/session activity, pre-auth activity, or repeated meaningful events rather than only registered accounts. We should tighten this definition before using active users as a clean activation metric.

---

## 3. Written Analysis

The clearest current funnel signal is that 207 page views produced 35 signups, a signup conversion rate of about 17%. For an early-stage product with mostly organic traffic, that suggests the landing page and core pitch are working well enough to create interest.

The biggest measurement issue is after signup. The endpoint reports 65 active users, which is higher than the 35 registered signups. That means our active-user metric is probably not aligned with the assignment definition of "users who did something meaningful." It may be counting anonymous visitors, sessions, or events rather than unique signed-in users. Because of that, we cannot yet cleanly answer how many signed-up users reached activation.

The biggest product risk is still the onboarding-to-first-recommendation step. From peer review and user testing, users understood the wardrobe planning idea but got confused when wardrobe creation felt manual or fragmented. If users sign up but do not complete wardrobe setup or generate an outfit, the product loses the chance to show its value.

## What We Think Is Causing Drop-Off

The likely cause is onboarding friction. Users need enough wardrobe and preference data for recommendations to feel personal, but too much setup makes the product feel like a chore. Manual wardrobe entry and overlapping Manual/Search/Vision paths can make the first session feel confusing before users reach the "aha" moment.

## What We Will Do About It

This week, we will focus analytics and product work on the activation funnel:

1. Tighten event definitions so `active_users` means a signed-in user who completes a meaningful action.
2. Track these specific events: signup completed, onboarding started, wardrobe item added, outfit generation started, recommendation viewed.
3. Make vision-based wardrobe creation the primary onboarding path.
4. Reduce manual/free-text setup and use structured dropdowns where possible.
5. Treat "recommendation viewed" as the key activation event, because that is the first moment users can judge whether misfitAI is useful.

The next analytics snapshot should be able to answer: of 35 signups, how many completed onboarding, added wardrobe items, and viewed at least one outfit recommendation?
