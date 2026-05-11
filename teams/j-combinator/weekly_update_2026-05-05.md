# Sift — Weekly Update
**Week of May 5, 2026**

---

## What We Built Last Week and Why

- **App Store launch** — Sift is live on the Apple App Store. We have real users outside our test group for the first time. This was the priority — features are only useful if people can actually access the product.
- **Taste profile v2** — expanded taste profiles now track tag weights, borough weights, and price preferences alongside category weights, all synced to Supabase. The v1 category-only model was too coarse — two users who both like "music" but one prefers jazz in small venues and the other prefers large concerts were getting the same feed. Tag and borough weights start differentiating them.
- **Enhanced `/api/metrics` endpoint** — added `dau_last_14` (daily active users for the past 14 days), full funnel breakdown (`signed_up` → `completed_onboarding` → `saved_first_event` → `marked_going` → `ticket_clicked` → `completed_plan`), and cohort retention. We need this data to make decisions — signups alone don't tell you if people are actually using the app.
- **Undo dislike** — users can now undo a hard dislike swipe. Added because several test users accidentally dismissed events they wanted and had no way to recover them. Losing a user over an accidental swipe is an unnecessary churn driver.
- **Results filter bar** — category filter chips on the discover screen so users can narrow the feed without re-doing onboarding. Some users know exactly what they want on a given day; the swipe feed alone was too passive for them.

## What We're Building This Week and Why

- **`page_views` from Amplitude API** — the metrics endpoint has `page_views: 0` hardcoded. Switching to pull the real number from Amplitude's Dashboard REST API so the leaderboard reflects actual usage.
- **Cohort retention fix** — cohort retention is currently all zeros because it was using first analytics event instead of actual Auth signup date to assign users to cohorts. Rewriting to use Supabase Auth `created_at` as the cohort anchor.
- **User testing round 3** — running another round of usability sessions now that real users are in the app. First two rounds were on prototypes; this round is on the live product with real data.

## Current User Count

Live at [https://sift-mobile-two.vercel.app/api/user-count](https://sift-mobile-two.vercel.app/api/user-count)

## Biggest Blocker

**App Store rejection — account deletion required** — Apple reviewed the app and came back requiring a native in-app account deletion flow before approving. App Store guidelines mandate that apps offering account creation must also allow users to delete their account from within the app. Building the `/api/delete-account` endpoint (deletes all user data across every table + removes the auth record) and a deletion UI in Settings this week so we can resubmit.
