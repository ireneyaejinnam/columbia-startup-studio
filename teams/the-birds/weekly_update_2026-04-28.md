# Weekly update — Circles — 2026-04-28

## What we built last week (and why)

**Product**

- **Columbia Events integration:** Imported all upcoming Columbia events via the Bedework feed (with pagination) and added a dedicated Columbia Events section directly to the Home feed—solving the "empty room" problem and providing immediate value to new users who open the app for the first time.
- **Smart search bar:** Added a typo-tolerant search bar with Columbia-specific filters, refined search result layouts (removed thumbnail images to emphasize text), and hid the search bar contextually on profile and circle detail pages.
- **Social system and discovery:** Built a complete social layer—named, deep-linked notifications, a friends graph with circles-in-common pills, a new Friends tab on mobile bottom navigation, friend profile navigation, and a community discovery / activity page revamp.
- **Guest browsing:** Enabled guest browsing with sign-in prompts for protected actions—lowering the barrier to entry so new visitors can explore before committing to an account.

**Polish and Quality Bar**

- **Visual rebranding and typography:** Transitioned branding to "Chords" (media vocabulary), improved overall typography, and standardized avatar backgrounds (deterministic placeholder colors plus app-wide profile photos instead of initials).
- **Circle Details upgrades:** Collage Cards where member-contributed photos replace the creator's face as the cover image, a circle photo gallery, relocated share button for stronger contrast, and inline Sign In for guests.
- **Mobile and layout fixes:** Rebuilt the right sidebar, prevented horizontal scrolling on mobile, centered the bottom navigation FAB, standardized LIVE badge placement, and fixed the Create button to bottom-left on desktop.
- **Feed management:** Revamped the activity feed with limits, overlap detection, and "view more/less" toggles for a cleaner reading experience.

**Growth and Feedback**

- **Columbia Subreddit launch:** We posted our application on the Columbia subreddit to start driving organic campus traffic.
- **Early feedback:** Strong validation from students on Reddit regarding our value proposition: *"This looks super cool! It's great to see all campus events in a single place instead of sifting through emails or reading posters on campus."*

---

## What we're building this week (and why)

1. **Analytics instrumentation (GA4 + Amplitude)** — we need real data on activation funnels and feature usage to make evidence-based product decisions, especially with users coming in from Reddit.
2. **Sign-in page polish** — minimalist animated circles background to make the first impression feel premium and reinforce the product metaphor.
3. **Sidebar cleanup** — removing redundant guest CTAs from the desktop sidebar to reduce visual noise.

**Why:** With real campus users arriving from our subreddit launch, we need to (a) measure what they do and (b) make the first touchpoints (sign-in, feed) feel polished and trustworthy.

---

## Current user count

Early organic traffic from the Columbia subreddit launch; instrumentation going in this week to get exact numbers.

## Biggest blocker

No analytics pipeline yet—we're making product decisions without quantitative data. GA4 and Amplitude integration is the top priority this week.
