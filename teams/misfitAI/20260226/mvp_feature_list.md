# MVP Feature List

**Product:** misfitAI / Wardrobe Planner  
**MVP Goal:** Let a user generate a simple weekly outfit plan from their own wardrobe and real schedule context with minimal setup.

## 1. Lightweight Wardrobe Setup

Users can add core garments through a simple form with name, category, color, and formality. This creates a usable wardrobe without requiring a full closet scan on day one.

Why it matters: interview and synthetic testing feedback showed that photographing or cataloging an entire wardrobe upfront feels like too much work.

## 2. Week Events Setup

Users can enter a 7-day schedule with one event type per day, such as class, work meeting, internship, dinner, gym, or casual day.

Why it matters: the product promise depends on matching outfits to the user's actual day, not generic style inspiration.

## 3. Outfit Recommendation Engine

The backend generates outfit recommendations from the user's wardrobe and event types using simple rules for category and formality.

Why it matters: this is the core product value: turning closet + calendar context into a ready-to-wear suggestion.

## 4. Weekly Outfit Plan View

Users see a 7-day plan with outfit items and a short explanation for why each recommendation works.

Why it matters: the MVP should make the value visible immediately: "one click -> full week of outfits."

## 5. Waitlist and Feedback Capture

The landing page captures emails from interested users, and the MVP should collect lightweight feedback from early testers about recommendation quality, missing wardrobe items, and trust.

Why it matters: demand generation and product learning need to connect. The team needs to know not just who signs up, but whether the recommendations feel useful enough to keep using.

## Out of Scope for MVP

- Full Google Calendar OAuth.
- Real weather API integration.
- Full closet photo ingestion.
- Advanced AI styling or image-based fit prediction.
- Social outfit voting or creator analytics.
