# Check-In: Peer Review Learnings and Product Roadmap

## Team

Standard Deviants

## Product

Instaplan is a mobile social event discovery and group coordination app for NYC. The core user is someone who wants to go out but does not want to browse ten different event sites, text five group chats, or pick something their friends will not actually enjoy.

The product combines real event discovery, friend-based social signal, going-out status, group event voting, calendar-aware coordination, and event logging.

## Look Back: Peer Review

### What worked when people used your product?

- The overall concept was easy to understand: a better way to discover things to do in NYC and coordinate plans with friends.
- The strongest value proposition was social signal. Seeing friends' activity, ratings, logs, or going-out status feels more useful than anonymous star ratings or generic event listings.
- Testers could move through a real product flow across Explore, Map, Feed, Chat, Profile, Friends, Who's Out, event detail pages, event creation, and group voting.
- The real event supply is a major strength. Pulling events from Ticketmaster, Eventbrite, Dice, SeatGeek, Meetup, and NYC-specific sources makes the product feel grounded in actual things people could attend.
- The group coordination idea resonated because choosing plans is usually a social problem, not just a search problem.

### What confused them or broke?

- The product has many powerful pieces, so the first-time user experience can feel broad before the user understands the main loop.
- The app needs to make the "first friend" moment clearer. A social product is much harder to evaluate if the tester does not quickly see friend activity, friend logs, or a live group decision.
- The difference between saving an event for later, marking interest, hiding something with the heartbreak/not-interested action, creating an event, and starting a group vote needed clearer hierarchy.
- Some parts of the experience depend on seeded or existing social data. Without that, the app can look more like an event browser than a social coordination tool.
- Push notifications are not wired up yet, which means the coordination loop is less alive than it needs to be for real usage.

### What's the biggest gap?

The biggest gap is activation into the social loop. Instaplan becomes most valuable when a user has friends in the app, can see who is free or interested, and can turn event discovery into a plan. The product needs to get new users to that moment quickly.

### Improvement shipped based on feedback

- Added saved events so users can bookmark something interesting without committing to it immediately. Saved events now persist through `saved_events`, show up on the user's Profile, and can be pulled into event proposals when planning with a group.
- Added a clearer negative-preference action for events users are not interested in: the heartbreak / "Not for me" interaction. This records a dismiss signal so the app can hide that event and suppress similar recommendations instead of repeatedly showing events the user has already rejected.
- Improved the event detail action model by separating "Save" from "Not for me." This gives users two lightweight ways to train the product: one for future intent and one for disinterest.
- Connected dismissal feedback back into Explore filtering, so discovery is not a one-size-fits-all feed. Events the user dismisses, repeated events with the same title, and semantically similar events can be filtered out.
- Made saved events useful beyond the individual user by adding them as a source in the proposal event picker, so saved discoveries can become group plans later.

## Look Forward: Product Roadmap

### What do we still need to learn?

- Who is the sharpest initial audience: Columbia students, NYC friend groups, nightlife/event-heavy users, or people who already organize group plans often?
- Which feature creates the strongest aha moment: friend activity, Who's Out, group swipe voting, map-based discovery, or event logs?
- How much event quality matters versus social context. Do users care more about the best events, or about knowing which events their friends would actually go to?
- What minimum social graph is needed before the product feels useful?
- Whether users will invite friends into a new app for planning, or whether we need stronger sharing/link-based flows before signup.

### What do we need to build between now and Demo Day?

- A polished demo path that shows the complete loop: discover an event, see social signal, share it with friends, vote as a group, and log it afterward.
- Better onboarding that gets users from signup to interests, friends, and a useful Explore feed quickly.
- A stronger friend-invite and group-join flow so the app does not depend on users already having friends inside Instaplan.
- Push notifications or a convincing substitute for live coordination moments like messages, group votes, friend requests, and going-out status changes.
- A polished Instaplan landing page and initial demand-gen plan for beta testers.
- Cleaner demo data with realistic NYC events, users, friend activity, event logs, chats, and group proposals.
- More product polish on the screens most likely to be shown on Demo Day: Explore, event detail, Who's Out, Chat, Swipe Vote, and Profile.

### Biggest open question

Can Instaplan become useful before a user's whole friend group joins, or does the product need to focus first on viral group links and lightweight coordination flows?

## Demo Day Success: May 12

Success on Demo Day means we can show that Instaplan is more than another event listing app:

1. A user opens the app and sees real NYC events.
2. The user sees friend-based context that helps them decide what is worth doing.
3. The user marks themselves as looking to go out or sees which friends are available.
4. A group uses swipe voting or proposals to agree on an event.
5. The app turns discovery into an actual plan.
6. Afterward, the event log creates better social signal for the next decision.

The story should be simple: Instaplan helps people stop endlessly searching and texting, and actually get out with friends.
