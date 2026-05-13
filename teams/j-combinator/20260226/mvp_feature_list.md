# Sift — MVP Feature List

Sift is a NYC event discovery app that learns your taste and surfaces events worth going to. The following 5 features represent the minimum viable product: everything a user needs to find an event, commit to it, and come back.

---

## Feature 1: Personalized Onboarding Quiz

**What it is:** A short setup flow (interests, neighborhood/borough, available days/times, budget, and vibe preference) that seeds the user's initial taste profile before they've swiped on anything.

**Why it's core:** Without this, every new user gets a cold, untailored feed. The quiz provides the baseline signals that make first-session recommendations feel personal rather than generic. It is the entry point to the entire personalization system.

**Key screens/files:** `app/(onboarding)/flow.tsx`, `src/types/user.ts`, `src/lib/tasteProfile.ts`

---

## Feature 2: Swipeable Event Discovery Feed

**What it is:** A card-stack interface on the Discover tab where users swipe or tap to like, skip, or save events. Each card shows the event image, name, date/time, neighborhood, price, and a short hook line.

**Why it's core:** This is the primary user loop. It is how users consume events and how the app collects the interaction signals (like, dislike, save, going) that power the recommendation engine. Without a working feed there is no product.

**Key screens/files:** `app/(tabs)/discover.tsx`, `src/components/events/EventCard.tsx`, `src/lib/eventRecommendations.ts`, `src/lib/getEvents.ts`

---

## Feature 3: Adaptive Taste Profile & Recommendations

**What it is:** A lightweight ML-style weighting system that updates in real time as the user interacts with the feed. Category weights, tag weights, borough weights, and price preference are adjusted on every like, dislike, save, and "going" interaction. The feed re-ranks accordingly.

**Why it's core:** This is what makes Sift more than a list app. The taste profile is what differentiates Sift — it turns passive swiping into a personalization engine that gets better with use. Without it, every user sees the same feed.

**Key screens/files:** `src/lib/tasteProfile.ts`, `src/lib/getEvents.ts` (`computeEventScore`), `src/lib/interactions.ts`, Supabase migration `015_taste_profile_v2.sql`

---

## Feature 4: Plan Tab (Saved & Going Events)

**What it is:** A dedicated tab where users see the events they've saved to lists or marked as "going." Events can be viewed in calendar or list mode, reordered via drag-and-drop, and exported to Google Calendar or shared as an ICS file.

**Why it's core:** Discovery without follow-through has no retention loop. The Plan tab converts passive interest into committed attendance and gives users a reason to return to the app. It is also the primary surface for sharing, which drives organic growth.

**Key screens/files:** `app/(tabs)/plan.tsx`, `src/components/events/EventPlanCard.tsx`, `src/components/profile/CalendarSection.tsx`, `src/lib/calendar.ts`, `src/lib/userDataService.ts`

---

## Feature 5: Automated Event Ingestion Pipeline

**What it is:** A dual-pipeline backend system that keeps the event database fresh. A daily cron scrapes curated sources (Dice, Resident Advisor, Luma, Fever, Eventbrite, museums). Every three days, an AI discovery pipeline uses Claude to find additional events via web search, then enriches and scores them before upserting to Supabase.

**Why it's core:** The app is only as good as its event inventory. A stale or thin database kills every other feature. This pipeline is infrastructure, not a UI feature, but it is a required part of the MVP — without it the product cannot function in production.

**Key files:** `lib/ingest/run-daily.ts`, `lib/ai-collect-data/run-all.ts`, `.github/workflows/daily-ingest.yml`, `.github/workflows/ai-discovery.yml`, `supabase/migrations/006_ai_events.sql`
