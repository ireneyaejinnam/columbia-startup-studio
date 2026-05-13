# User Testing Synthesis

## What we observed

We ran 5 think-aloud onboarding sessions with people who had not used Recruitr before: 2 college athletes, 1 high-school club athlete, 1 assistant coach, and 1 parent of a recruit. Each tester was asked to open the product, explain what they thought it was for, create or choose the right account type, and find one athlete or coach action that felt useful.

The strongest pattern was that people understood Recruitr once they reached the highlight feed, but several were unsure what to do before that moment. The first clear "aha" moment happened when testers saw athlete clips with recruiting actions next to them: likes, comments, share, profile, shortlist, and search. Before reaching the dashboard, testers asked whether Recruitr was a social app, a recruiting database, or a video portfolio tool.

Common friction:
- 4 of 5 testers hesitated on the landing page because the product value was not concrete enough until they saw the feed.
- 3 of 5 testers looked for a quick way to try the app before creating a full profile.
- 3 of 5 testers expected coach and athlete onboarding to feel different immediately.
- 2 of 5 testers did not understand what "activation" meant until they posted, saved, or messaged someone.
- 2 of 5 testers wanted clearer trust signals around coach verification and athlete visibility.

## What we're changing

We are changing onboarding around one primary action: get the user into the recruiting workflow as fast as possible.

Product changes:
- Make the landing page promise more specific: "Scroll athlete highlights, shortlist prospects, and message recruits."
- Split onboarding by role earlier: "I am a coach" vs. "I am an athlete."
- Route coaches toward search/shortlists and athletes toward profile completion/post creation.
- Add a stronger first-session checklist:
  - Athlete: complete profile, upload first highlight, choose school/team.
  - Coach: select school/team, search athletes, save first shortlist.
- Hide demo login in production, but keep a controlled reviewer/demo path for private testing.
- Add password reset and email verification so reviewers can recover accounts without our help.
- Add metrics around page views, signups, activation, and waitlist leads so we can see where onboarding drops.

## Why

The sessions showed that Recruitr becomes easy to understand when users see the app behaving like a recruiting feed, not when they read abstract copy. The product should not make new users infer the workflow. It should guide each role to one meaningful first action.

For coaches, that action is saving or messaging a prospect. For athletes, that action is posting a highlight or completing a profile. We are treating those actions as activation because they show the user has moved from browsing to recruiting behavior.

## Session notes

| Tester | Profile | First moment they understood | Most confusing moment | Would use again? |
|---|---|---|---|---|
| T1 | Club soccer athlete | Seeing the vertical highlight feed | Did not know whether to sign up as athlete or "player" | Yes, if coaches were verified |
| T2 | Assistant basketball coach | Search + shortlist flow | Unsure if all athletes were real or sample data | Yes, for prospect tracking |
| T3 | High-school athlete | Profile page with stats and clips | Landing page felt too broad | Maybe, if profile setup was fast |
| T4 | Parent of recruit | Athlete profile and school/team info | Did not know who could see posts | Yes, as a monitoring tool |
| T5 | College athlete | Create post and profile edit | Wanted clearer next step after signup | Yes, if coaches were active |

## Product recommendation

For the next reviewer build, the onboarding goal should be:

> Within 90 seconds, a new user should complete one recruiting action: athlete posts a highlight, or coach saves/messages a prospect.

That gives us a measurable activation event and a clearer product promise.
