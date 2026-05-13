# MVP Feature List — QuestCity

**Team:** Team Millionaires (DG-ST-AB)
**Date:** February 26, 2026

These are the 5 features required for a functional v1. Not a wishlist. Each will go through feature-forge in the Build phase.

---

## Feature 1: Quest Board

**What it is:** A browsable list of available quests in the user's city. Each quest has a name, category (Food / Art / Outdoor), estimated time, difficulty, and point value.

**Why it's core:** Without a quest board, there's no product. This is the entry point — where users decide what adventure to take.

**MVP scope:** 10 hand-curated quests for NYC only. No filtering, no personalization. Just a list.

---

## Feature 2: Quest Detail + Location Surfacing

**What it is:** Tapping a quest opens the detail view: description, rules, and a list of the 3 closest matching locations sourced via Google Places API.

**Why it's core:** User testing showed that "find 5 coffee shops" is meaningless without a starting location. Users need a map pin, not a category. This feature is the bridge between intent and action.

**MVP scope:** Google Places API integration. First 3 locations surfaced. Tap to open in native Maps app. No custom map view.

---

## Feature 3: Photo Check-In

**What it is:** At each quest location, users take a photo to verify their visit. Photo uploads to the backend. Quest progress updates.

**Why it's core:** This is the moment of completion — the core game loop. Without check-in, there's no way to validate progress or award points.

**MVP scope:** Simple photo upload. Manual review by team for MVP (Wizard of Oz). No AI verification yet.

---

## Feature 4: Points + Badge System

**What it is:** Users earn points for each check-in. Completing a full quest awards a badge. Points accumulate on a profile.

**Why it's core:** This is the reward layer that makes the game loop compelling. Completing a quest needs to feel like an achievement, not just ticking a box.

**MVP scope:** Points counter. Static badge image on quest completion. No animated rewards, no leaderboard (phase 2).

---

## Feature 5: User Profile

**What it is:** A simple profile page showing the user's name, total points, completed quests, and earned badges.

**Why it's core:** Progress needs to be visible. Without a profile, there's no sense of accumulation — users have no reason to return.

**MVP scope:** Name, avatar (optional), points total, quest history list, badge gallery. No social sharing from profile yet.

---

## Google Analytics Certification

Started. In progress this week via [Google Skillshop](https://skillshop.google.com). Estimated completion: Week 7.
