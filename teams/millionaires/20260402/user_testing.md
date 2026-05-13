# Track A: User Testing — Onboarding Flow

**Team:** Team Millionaires (DG-ST-AB)
**Date:** April 7, 2026
**Sessions:** 4

---

## What we observed

Three patterns appeared across all four sessions:

**1. Nobody knew what to do on their first quest.** Every user arrived at the quest screen confused about at least one of: time window, check-in method, or how to find the first location. We have no onboarding. The gap between "I signed up" and "I completed my first quest" doesn't exist in the product.

**2. Users expected a map pin, not a category.** "Find 5 indie coffee shops" is meaningless without a starting point. Every tester assumed the app would surface a specific location with directions. We're building a quest app without the navigation layer.

**3. Couple mode is our strongest differentiator but completely undefined.** Our most excited users (James & Priya, our exact target demographic) hit a wall immediately: "Do we share one account?" We had no answer. Core feature, zero mechanic.

Secondary findings:
- Fake testimonials visibly destroyed trust with one skeptical user — she called them out unprompted
- Competitive/solo users (Maya, Derek) converted faster and had clearer activation paths than couples
- Photo privacy was an unprompted concern: "Where does my photo go?"

---

## What we're changing

**Change 1: Add a 3-screen onboarding before the first quest**
- Problem: Users hit the quest screen with zero context
- Fix: Insert swipeable onboarding (under 30 seconds): (1) Here's how quests work, (2) Here's how to check in, (3) Here's your first quest

**Change 2: Add location surfacing to quest cards**
- Problem: "Find 5 coffee shops" means nothing without a starting point
- Fix: Each quest card surfaces the 3 closest matching spots via Google Places API; navigation opens in native Maps

**Change 3: Define couple mode mechanics**
- Problem: Strongest demographic hits a wall at "how do we share this?"
- Fix: Two separate accounts linked to a shared quest; both check in independently; shared progress on leaderboard

---

## Why

Sessions showed that users want the product but can't use it. All four testers expressed genuine excitement about the concept — and all four got stuck before completing their first quest. The product isn't broken; the onboarding doesn't exist. These three changes directly address the moments where every tester stopped.
