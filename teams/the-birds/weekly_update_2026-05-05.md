# Weekly update — Circles — 2026-05-05

## What we built last week (and why)

**Product**

- **Analytics pipeline (GA4 + Amplitude):** Integrated Google Analytics 4 and Amplitude with a unified `analytics.ts` module that initializes both providers, tracks page views on route changes, and exposes a `trackEvent` helper for custom events—so we finally have quantitative data on activation, retention, and feature usage.
- **Sign-in page redesign:** Replaced the static sign-in background with a minimalist animated-circles treatment (CSS keyframe orbits and floating shapes) to reinforce the product metaphor and create a premium first impression.
- **Desktop sidebar cleanup:** Removed the redundant guest CTA from the desktop sidebar—one less piece of visual noise for signed-out visitors who already see the sign-in prompt.

**Why (summary):** With real users arriving from our Reddit launch, the priority shifted to *measuring* what those users do (analytics) and *polishing* the first touchpoint they hit (sign-in). We deliberately kept the scope tight this week to avoid shipping broken features while the instrumentation was landing.

---

## What we're building this week (and why)

1. **Chords naming refactor** — renaming the internal "stories" schema to "chords" across client, Supabase schema, storage bucket, and seed data so the product vocabulary is consistent and developers stop translating between old and new names.
2. **Circular recommendations (Outer Circles)** — replacing the old Trending Circles horizontal row with a photo-forward, drag/swipeable circular navigator on the Home feed to make discovery feel more engaging.
3. **Bug fixes** — chord photo upload failures, navigation regressions, dead `/messages` route, and stray localhost references that break the deployed build.
4. **Entity naming alignment** — renaming surface-level product terminology (My Circles → Inner Circles, Friends → Dots, Profile → My Dot, Create → Draw a Circle) to match the thematic vocabulary of the product.

**Why:** The naming inconsistencies created confusion for both users and developers; the recommendation navigator is our main discovery lever now that the feed has real content; and the bug fixes unblock core flows (photo sharing, navigation) that are breaking for live users.

---

## Current user count

Analytics just went live; collecting baseline data this week.

## Biggest blocker

Schema naming debt—the "stories" vs "chords" mismatch is causing upload failures and confusion across the codebase. Refactor is underway.
