# Roam – MVP Doc

**Team:** Roam
**Date:** March 5, 2026

---

## 1. Core Flow

User opens the app → sees a **"Today's Picks"** screen with 4 activity cards in a 2×2 grid → optionally toggles **"In a rush today?"** to filter activities under 60 minutes (with at least one under 15 minutes) → taps a card → sees an overlay with the activity's location, photos, description, and total time commitment (travel + activity + 10% buffer) → taps **"Go now"** to open directions in Apple Maps or Google Maps → does the activity → receives a push notification to rate it.

That's the full demo-able loop. Core value: a time-constrained user sees exactly how long an activity will take — door to door — and can commit without anxiety.

**Card layout (2×2 grid):**
- **Top left:** Quickest option — under 30 min total including travel and a 10% buffer
- **Top right:** Highest rated / safest choice (well-reviewed restaurant, bar, or dependable spot)
- **Bottom left:** Novel but accessible (mural, park walk, small exhibit)
- **Bottom right:** Wildcard / stretch goal (longer commute or outside comfort zone)

---

## 2. Tech Stack

- **Platform:** iOS (primary target for MVP)
- **Data source:** Google Maps API — scraping restaurants, bars, cafes, and nearby locations with ratings, photos, and location data
- **Time estimates:** Manually hardcoded per activity category (e.g., bars, cafes, restaurants) with a 10% buffer added on top of travel + activity time
- **Maps integration:** Deep link to Apple Maps / Google Maps via "Go now" button
- **Notifications:** Native iOS push notifications (post-activity "How was it?" prompt)
- **Frontend:** React Native (iOS)
- **Backend / hosting:** TBD — to be finalized at next team sync

---

## 3. Team Roles

- **Tyler** — Product strategy, MVP scoping, document owner
- **Engineers (TBD)** — iOS app build, Google Maps API integration, activity card UI
- **Designer (TBD)** — Activity card layout, overlay screen, "In a rush today?" toggle UI
- **Demand gen lead (TBD)** — User outreach, social content, tracking signups and conversion

*Full role assignments to be confirmed at next team meeting. "Everyone builds" is not the plan — roles will be split and owned individually.*

---

## 4. What's Faked

- **Time estimates** are not dynamically computed. They are manually assigned per activity category (e.g., "bars ≈ 45 min") with a 10% buffer baked in. No real-time calculation happening.
- **Activity ranking** uses simple Google Maps heuristics (proximity + rating) — not a real personalization engine. The 2×2 card positions are assigned by rule, not by user data.
- **Personalization is absent.** Every user sees the same 4 cards based on location. No ML, no user history, no clustering.
- **Reel ingestion** (pulling from Instagram/TikTok) — not built, not faked. Post-MVP.
- **Social / group features** (invites, shared maps, group calendars) — not built. Post-MVP.
- **Calendar integration** — not built. Post-MVP.
- **Rating system** — post-activity notification and slider rating will be manually reviewed at first; no automated feedback loop yet.

---

## 5. Demand Gen Status

- **Current status:** Early — no formal demand gen campaigns running yet.
- **Target user:** Time-constrained college students (engineering, pre-med) who feel anxiety about committing to activities due to unclear time expectations.
- **Channels being explored:** Word of mouth within Columbia; direct outreach to target demographic for initial user testing.
- **Current numbers:** Visits — TBD; Signups — TBD; Conversion rate — TBD *(to be tracked once landing page / TestFlight is live)*

**Success metrics we're aiming for:**
- 10% of active users execute at least one activity per week within 2–4 weeks of onboarding
- 10% of users report doing more spontaneous activities after 2–4 weeks
- Statistically significant reduction in reported time-commitment anxiety (via in-app survey)
