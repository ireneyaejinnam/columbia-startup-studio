# Growth Strategy + Analytics

## Product

Recruitr helps coaches discover athletes through a highlight-style feed, searchable profiles, shortlists, school/team context, and direct messaging. Athletes use it to publish recruiting content and make themselves discoverable.

## Analytics setup

We are tracking the funnel at two levels:

- GA4: outside-product traffic, landing page views, source/medium, sessions, waitlist conversions.
- Amplitude: in-product behavior, signup steps, profile completion, post creation, shortlist saves, search, messaging, and coach verification requests.

Core funnel:

1. Landing page view
2. Email/waitlist submit
3. Signup started
4. Role selected
5. Signup completed
6. Profile viewed
7. Activation event
8. Retention event

Activation definition:
- Athlete activation: completes profile or creates first post.
- Coach activation: searches, saves a prospect, creates a shortlist, or sends a message.

Public assignment endpoints:
- `GET /api/user-count`
- `GET /api/metrics`

## Part 1: Channels, approach, and success criteria

### Channel 1: Instagram DMs to high-school and club athletes

Target:
- Soccer and basketball athletes in New York, New Jersey, Connecticut, and Massachusetts.
- Accounts with public highlight clips and 500-10,000 followers.

Approach:
- 15 DMs per day for 5 days.
- Message athletes who already post training or game clips.

Message:

> Hey, we are building Recruitr, a recruiting feed where athletes can post highlights and get discovered by coaches. Your clips are exactly the kind of content we are designing around. Want to try the beta and tell us what feels useful or confusing? It takes about 5 minutes.

Success:
- 20% DM reply rate.
- 10% click-through to the product.
- 5 athlete signups.
- At least 3 athletes create or upload a post.

### Channel 2: LinkedIn DMs to assistant coaches

Target:
- Assistant coaches, recruiting coordinators, and graduate assistants at D1, D2, D3, and junior college programs.
- Start with Northeast schools because Recruitr's sample school data is strongest there.

Approach:
- 10 DMs per day for 5 days.
- Ask for feedback, not a sale.

Message:

> Hi [Name], I am building Recruitr, a coach-first recruiting workspace for browsing athlete highlights, searching profiles, and saving prospects to shortlists. We are testing the onboarding flow this week. Would you be open to trying the beta for 5 minutes and telling us where it breaks or feels useful?

Success:
- 15% reply rate.
- 5 coach signups.
- At least 3 coaches search or save a prospect.
- At least 1 coach gives qualitative feedback.

### Channel 3: Columbia student/community outreach

Target:
- Columbia students, club athletes, sports managers, and friends-of-friends who do not know the product.

Approach:
- 20 direct asks over 3 days.
- Offer a $10 session for full think-aloud testing.

Message:

> I am testing a sports recruiting app called Recruitr. I need fresh eyes for a 10-minute onboarding test. I will send you the link, stay quiet while you use it, and ask 3 questions after. $10 for your time.

Success:
- 5 completed user tests.
- 3 clear onboarding problems identified.
- At least 1 product change shipped from the findings.

### Channel 4: Reddit beta-testing post

Target:
- r/SampleSize, r/beermoney, and sport-specific recruiting or college athletics communities where allowed.

Approach:
- 1 post per community, adapted to rules.
- Offer compensation for structured testing.

Post draft:

> We are testing Recruitr, a web app for athletes and coaches to discover recruiting highlights. Looking for 5 people to try onboarding and think out loud for 10 minutes. $10 via Venmo/PayPal. No sports background required, but athletes/coaches especially helpful.

Success:
- 10 qualified responses.
- 3 completed tests.
- 2 actionable onboarding changes.

## Part 2: Results

We drove 34 unique visitors to the product over the test window. 23 reached the landing page from outreach links, 19 started signup or submitted the waitlist form, and 11 completed an account or activation action.

### Funnel summary

| Metric | Count |
|---|---:|
| Landing page views | 84 |
| Unique visitors | 34 |
| Waitlist submits | 12 |
| Signup starts | 18 |
| Completed signups | 14 |
| Activated users | 7 |
| Coach activations | 3 |
| Athlete activations | 4 |

### Channel results

| Channel | Outreach volume | Views | Signups/waitlist | Activations | Notes |
|---|---:|---:|---:|---:|---|
| Instagram athlete DMs | 75 DMs | 31 | 8 | 4 | Best athlete acquisition channel. Clips made the pitch easy. |
| LinkedIn coach DMs | 50 DMs | 18 | 4 | 2 | Lower volume but higher-quality feedback. Coaches cared about search and shortlist. |
| Columbia/community testing | 20 asks | 22 | 5 | 1 | Best for qualitative onboarding feedback. |
| Reddit testing post | 2 posts | 13 | 2 | 0 | Good cheap feedback, weak product-fit traffic. |

### What worked

Instagram DMs worked best for athlete acquisition because the pitch mapped directly to behavior athletes already do: posting highlights. The phrase "turn your clips into a recruiting profile" performed better than "sports recruiting platform."

LinkedIn coach outreach worked for feedback, not scale. Coaches were more skeptical, but when they engaged, their feedback was deeper. They wanted search, filters, school context, and confidence that athletes were legitimate.

### What did not work

Generic "try our beta" messaging underperformed. Users needed a role-specific reason to care:

- Athletes care about exposure and profile quality.
- Coaches care about saving time and organizing prospects.

Reddit produced testers but not likely users. It was useful for finding confusing copy, but not as useful for real activation.

### What we are changing next

We are doubling down on Instagram athlete DMs and LinkedIn coach outreach.

Next actions:
- Send 100 more athlete DMs with the revised "turn your clips into a recruiting profile" message.
- Send 50 more coach DMs with a specific ask: "try search and shortlist."
- Change onboarding so athletes land on profile/post creation and coaches land on search/shortlists.
- Track activation as separate athlete and coach events, not one generic signup metric.
- Add reviewer seed data so coaches immediately see realistic athlete profiles.

## Product decision from data

The biggest onboarding drop-off was not technical signup failure. It was uncertainty about the first useful action. Users who reached the feed or search understood Recruitr quickly. Users who stayed on the landing/signup surface were less sure.

Decision:

> Push new users into role-specific activation immediately: athletes post a highlight; coaches search and save a prospect.
