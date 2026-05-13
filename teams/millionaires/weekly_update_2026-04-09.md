# Weekly Update — April 9, 2026

**Team:** Team Millionaires (DG-ST-AB)
**User count:** 27

---

## What we built last week

Shipped the first working version of the QuestCity onboarding flow in Lovable. Users can now sign up, set their city (NYC), and see the quest board with 5 initial quests. Check-in via photo upload is live but manually reviewed by the team.

We built this first because the onboarding gap was the single biggest finding from user testing — every tester got stuck before completing a quest. The app had no path from "sign up" to "do something."

## What we're building this week

Adding location surfacing to quest cards via Google Places API. Each quest will now show the 3 nearest matching spots. Tap opens Apple Maps / Google Maps. This directly addresses finding #2 from user testing: users expect a map pin, not a category.

Also replacing fake testimonials on the landing page with real waitlist count.

## Current user count

27 (combining waitlist signups + Lovable app sign-ups)

## Biggest blocker

Google Places API integration is taking longer than expected — billing setup on GCP was confusing. DG is on it. Should be resolved by end of week.
