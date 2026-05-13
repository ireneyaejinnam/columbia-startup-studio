# Weekly update — Circles — 2026-05-12

## What we built last week (and why)

**Product**

- **Outer Circles (recommendation navigator):** Replaced the old Trending Circles horizontal row with a large, photo-forward circular browsing component on the Home feed. It supports drag/swipe, arrow-key navigation, and dot indicators—so discovery feels like browsing a gallery, not scrolling a list. Uses smart recommendations first and falls back to active feed circles.
- **Chords naming refactor:** Renamed the internal "stories" schema to "chords" across the entire stack—client components, Supabase tables (`chords`, `chord_views`), storage bucket, type map, and seed data. Fixed the chord photo upload bug that was silently failing because the client was writing to a bucket that no longer existed.
- **Canonical chords schema migration:** Added `016_chords_canonical_schema.sql` with RLS-enabled `chords` and `chord_views` tables, forward-copying legacy rows for zero-downtime migration.

**Product vocabulary overhaul**

- **Entity naming alignment:** Renamed surface-level product terminology across 40+ files to match the circle metaphor:
  - **My Circles → Inner Circles** — your joined circles are your inner circle.
  - **Friends → Dots** — connections on the platform are "dots" you connect.
  - **Profile → My Dot** — your profile is your dot in the network.
  - **Create → Draw a Circle** — creating a circle is "drawing" one.
  - **Recommendations → Outer Circles** — circles outside your network are your outer circles.
- Updated the **README** with a formal Circles Vocabulary table mapping product terms to frontend usage and backend code names.

**Bug fixes and stability**

- **Navigation fixes:** Fixed the previous-page navigation bug in CreateCircle, prevented routing to the dead `/messages` route, and removed stray localhost references from the deployed build.
- **Navigation alignment:** Unified icon rail and bottom nav options across desktop and mobile, ensured the smart search bar renders consistently, and fixed minor UI bugs in the Circles browse page.

**Why (summary):** The naming inconsistencies were creating real confusion—both for users who saw mixed terminology and for developers who had to mentally translate between "stories" and "chords." The Outer Circles navigator is our main discovery surface now that the feed has real content. And the bug fixes unblock core flows (photo sharing, navigation) that were breaking for live users hitting the deployed app.

---

## What we're building this week (and why)

1. **Onboarding flow** — a lightweight first-run experience that explains the circle metaphor and gets new users to their first circle faster, since analytics show drop-off before first action.
2. **Chat and messaging** — bringing back real-time chat inside circle detail pages so members can coordinate without leaving the app.
3. **Analytics review** — first pass at interpreting GA4 and Amplitude data to identify the biggest activation bottlenecks.
4. **Polish pass** — continuing to tighten mobile layout, touch targets, and load performance based on what we're seeing from real usage.

**Why:** With the vocabulary, discovery, and schema finally consistent, the next lever is reducing friction in the activation funnel—onboarding, in-circle communication, and data-driven iteration.

---

## Current user count

Analytics pipeline is live; first full week of data collection in progress.

## Biggest blocker

No real-time chat yet—users who join a circle have no way to coordinate within the app, which creates a dead-end after the join action.
