# Check-in: Peer Review Learnings + Product Roadmap

**Team:** August Fan Club
**Product:** Evidence of Life
**Date:** March 26, 2026

---

## Part 1: Peer Review Learnings

### What worked when people used your product?

The daily timeline view clicked quickly — people understood the concept of "here's your day, here's what you planned vs. what actually happened" within the first 30 seconds of looking at it. The Plan vs. Actual toggle was the single most-praised interaction; multiple reviewers called it out unprompted as the thing that made the product feel different from a standard calendar or to-do app.

Places was the breakout. The ability to log and revisit specific locations — coffee shops, restaurants, daily spots — resonated more than any other feature. Reviewers spent the most time on the map view and asked the most follow-up questions about it. One reviewer said it was "like Google Timeline but it actually feels personal." That's the strongest signal we've gotten about where to focus.

The aesthetic also landed well. The warm color palette, the Monet background on the daily view, and the overall visual tone felt intentional and differentiated. Nobody compared it to a generic productivity app, which is what we were going for.

### What confused them or broke?

The "add places" flow was the biggest friction point. Multiple reviewers tried to add a location and couldn't figure out how — the entry point wasn't obvious, the flow wasn't intuitive, and two people gave up entirely. This is the feature people care about most and it's also the hardest one to actually use. That's a problem.

Onboarding made too many assumptions. The app didn't default to English and didn't prompt for language or timezone on first launch. One reviewer opened the app and saw Chinese text, which was disorienting. Another reviewer's "time remaining" display was wrong because the default schedule hours didn't match their actual waking hours. These are small things individually but they compound into a first impression that feels unpolished.

Competitive positioning didn't land. Two reviewers immediately asked "how is this different from Google Timeline?" and one asked "what does this do that Notion can't?" We didn't have a crisp, visible answer to either question inside the product or on the landing page. We know the answer internally — Google Timeline is passive data with no narrative layer, Notion is manual with no temporal structure — but if users have to ask, we haven't communicated it.

No product demo video existed. Three reviewers said they would have understood the product faster with a 30-second walkthrough. The landing page alone wasn't enough to convey what the experience feels like once you're inside.

### What's the biggest gap in your product right now?

The gap between what the product promises and what a new user can actually do in their first session. The value prop is "your life, automatically recorded and worth remembering" — but right now most core features are still in concierge mode. Calendar integration, photos integration, and the weekly recap aren't wired yet. A new user signs up, sees an empty dashboard, and has to manually log everything. The "automatic by default" promise is aspirational, not current reality. Until we close that gap, the product undersells itself on first use.

### One improvement we shipped based on what we heard

We added a **schedule cycle setting** in profile preferences that lets users define their waking and sleeping hours. The "daytime remaining" display on the main timeline now calculates based on this custom schedule instead of using fixed default hours. This directly addresses the feedback that the time display felt wrong for users with non-standard schedules (late risers, night owls, shift workers). It's live now at evidenceoflife.vercel.app.

This was a quick win that also forced us to think about personalization more broadly — if we're claiming to show "what your life actually looks like," the product needs to know basic things about how you live. Language, timezone, and schedule are the minimum.

---

*Part 2 (Product Roadmap) submitted separately.*
