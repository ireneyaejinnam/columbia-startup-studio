# Roam – Check-in: Peer Review Learnings + Product Roadmap

## Part 1: Peer Review Learnings

**What worked**

People got the concept immediately. When we walked them through the map and showed how pins get pulled from reels, the reaction was pretty consistently "oh that's actually useful." The visual side of it landed — seeing your saved spots on a map felt satisfying in a way that just having a list doesn't. A few people said they could see themselves using it before a trip or when trying to figure out where to go on a weekend.

**What confused them or broke**

Onboarding was the main friction point. People weren't sure what to do first — like, do you start by adding a reel? Do you already need saved places? The entry point wasn't obvious. A couple people also got confused about what a "map" is in the app vs. just a collection of pins. The distinction between personal maps and group maps wasn't clear either.

**Biggest gap right now**

We don't have a clear reason for someone to come back. The first session feels novel but there's no pull to return unless you're actively trip-planning. We haven't closed the loop between saving a place and actually doing something with it — revisiting, organizing, sharing. That's the gap.

**One improvement we shipped**

Based on feedback that people wanted to use this with friends, we shipped the social layer: users can now add friends and create shared group maps together. So instead of your saved spots living in a silo, you can build a map collaboratively — like a group trip or a shared "places we want to try" list. This was the most-requested thing we heard and we got it live. You can see it in the app under the Groups tab.

---

## Part 2: Product Roadmap

**What we need to learn about our product**

- Who is actually coming back, and why? We have usage data but it's messy and we haven't defined what "retained" even means for us yet.
- Is the aha moment the map itself, or the process of building it? We think it's the map, but we haven't confirmed that.
- Does the social layer change retention, or just acquisition? Now that groups are live, we want to see if shared maps create more return visits than solo maps.
- Who is our real user — aesthetic curators, travel planners, urban explorers? We're building for all three right now which means we're probably not nailing any of them.

**Week-by-week breakdown**

| Week | Dates | What we're building | Goal |
|------|-------|---------------------|------|
| 1 | Mar 31 – Apr 6 | Clean analytics + define key events (pin created, return session, map shared) | Know what's actually happening in the app |
| 2 | Apr 7 – Apr 13 | Set up simple retention dashboard; identify Day 1 and Day 7 drop-off points | Find where we're losing people |
| 3 | Apr 14 – Apr 20 | Tighten core loop: faster pinning, basic folder/tag organization | Reduce friction in the save → revisit loop |
| 4 | Apr 21 – Apr 27 | Recruit 10–15 users per segment (curators, travelers, explorers); begin observing usage patterns | Start narrowing ICP |
| 5 | Apr 28 – May 4 | Run small distribution test (shareable public maps, short-form content); track inbound interest | Test for organic pull |
| 6 | May 5 – May 11 | Polish for Demo Day: tighten onboarding, prep data story, finalize demo flow | Ship what we're showing |

**What we're not building right now**

- AI chatbot / itinerary generator (see open question below)
- Social graph / following system
- Advanced search or discovery
- Google Maps integration
- Paid features or monetization
- Major UI redesigns

Rule: if it doesn't improve retention or help us identify our user, we don't touch it.

**Demo Day vision**

By May 12, we want to show a live app with real users who came back on their own — not just people we manually recruited. The story we want to tell is: *here's a specific type of person, here's the problem they had, here's how Roam fits into their life, and here's the data that shows they're actually using it.*

Data we need to support it:
- Day 1 and Day 7 retention numbers by segment
- At least one cohort showing 30%+ Day 1 retention
- Evidence that group maps drive more return visits than solo maps
- A few users who shared the app or a map without being asked

**Biggest open question**

Should we build an AI chatbot that generates itineraries or plans from your saved pins? It's a natural extension — you've saved 20 spots in Tokyo, the app could just build a day-by-day plan for you. But we're not sure if that's the product or a distraction. It could be a strong aha moment, or it could pull us away from the core retention problem before we've solved it. We're genuinely split on this one.
