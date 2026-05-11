# Growth Strategy Doc — Sift
**Team:** J Combinator
**Week:** Mar 31 – Apr 7, 2026
**Part 2 due:** Apr 9, 2026

---

## Part 1 — Your Plan

### Channels You're Targeting

**1. EdStem — Columbia TA/course channels**
Post in relevant Columbia course channels on EdStem where students might be planning things to do around the city. Frame it as a student-built tool looking for honest feedback from peers.

**2. Friends & Classmates — Direct outreach**
Personal messages to friends and Columbia classmates asking them to try Sift and share it with their own networks. Warmest possible audience — highest conversion rate of any channel.

**3. Instagram DMs — NYC & Columbia influencers**
Direct outreach to 5–10 NYC lifestyle, food, and events-focused Instagram accounts and Columbia student creators. Offer early access / skip the waitlist in exchange for trying the app and sharing if they find it useful.

---

### Approach for Each

**EdStem**
- Target: 1–2 posts in high-traffic Columbia channels (e.g., student life, off-campus, general)
- What to say: Position as a Columbia student asking for feedback on a side project — not a product launch. Lead with the problem ("finding things to do in NYC is a mess"), share the link, and ask for honest thoughts.
- Offer: Early access, no waitlist
- Volume: 1–2 posts this week

**Friends & Classmates**
- Target: Direct message friends, roommates, classmates — anyone in NYC aged 22–30
- What to say: Personal text or DM, not a copy-paste blast. Something like: "hey I built this thing for finding stuff to do in NYC, would mean a lot if you tried it and told me what's broken — siftapp.site." Ask them to forward it to one person they think would find it useful.
- Offer: Just a personal ask — no incentive needed, the relationship is the incentive
- Volume: Each team member reaches out to 10–15 people personally this week

**Instagram DMs**
- Target: 5–10 accounts — mix of NYC events pages (10k–100k followers) and Columbia student creators
- What to say: Short, personal DM. Not a template blast. Reference something specific about their account, explain what Sift does in one sentence, offer early access to skip the waitlist.
- Example DM:
  > "Hey [name] — love how you cover [specific thing]. I'm a Columbia student who built a NYC event discovery tool called Sift — you answer 3 questions and get a short list of things actually worth doing this weekend. Would love to give you early access if you want to try it. No ask beyond honest feedback."
- Volume: 5–10 DMs this week

---

### What Success Looks Like

| Channel | Leading Indicator | Goal |
|---------|------------------|-------|
| EdStem | Replies / clicks on post | 2+ meaningful responses, 5+ signups |
| Friends & Classmates | People who actually try it (not just click) | 15–20 people try the flow end-to-end |
| Instagram DMs | Response rate, link clicks | 30%+ reply rate, 3–5 influencers try it |
| Overall | New signups this week | 10–15 signups |
| Retention | Return visits the following weekend | At least 30% of signups come back |

A channel is working if it drives signups **and** those users return. A signup who never comes back is a vanity number. Friends are especially valuable here — they'll give you honest feedback, not just a silent bounce.

---

## Part 2 — What Happened

### Results Per Channel

| Channel | Reach | Clicks | Signups | Activations |
|---------|-------|--------|---------|-------------|
| EdStem | ~80 views | 12 | 4 | 2 |
| Friends & Classmates | ~60 DMs sent | 38 | 18 | 13 |
| Instagram DMs | 8 accounts | 3 replies | 2 | 1 |
| **Total** | **~148** | **53** | **24** | **16** |

*Signups = completed sign-up flow. Activations = saved or marked going for at least one event.*

### What Worked / What Didn't

- **What worked:** Friends & classmates was by far the most effective channel. Direct personal outreach — not a template blast — converted at roughly 30% from DM to signup. The ask was low-friction ("try it and tell me what's broken") and the relationship did the work. People who came in through friends also activated at a much higher rate than EdStem signups, likely because they had context from the person who sent them.

- **What didn't:** Instagram DMs underperformed. 8 DMs sent, 3 replies, only 1 person actually used the app. The accounts we reached had large enough followings that a cold DM from an unknown student didn't land. EdStem drove some signups but low activation — people clicked out of curiosity, not intent. The "feedback request" framing didn't filter for people who actually wanted to find things to do.

### What We're Changing Next

- **Doubling down on personal outreach** — each team member committing to 10 more personal DMs per week, specifically targeting people who complain about not knowing what to do on weekends (easy to find on Twitter/X and group chats).
- **Dropping EdStem** — too passive, low intent. The people who respond to course channel posts aren't the same people who want a weekend plans app.
- **Shifting Instagram strategy** — instead of cold DMs to large accounts, targeting micro-creators (1k–10k followers) who specifically post about NYC going-out content. Smaller audience but higher reply rate and more authentic fit. Volume: 3 targeted DMs per day for 2 weeks.

---

## Cold Start Strategy

### 1. Cold Start Type

**AI/Algorithm** — Sift's core value is that it learns your taste and gets better the more you use it. There's no network effect between users (you don't see what friends are doing), no marketplace (we're not connecting buyers and sellers), and no user-generated content supply problem. The cold start challenge is that the algorithm is weak until a user has interacted enough for the taste profile to be meaningful. Every new user starts cold.

### 2. Who Is Your Hard Side

The hard side is **the first 20–30 users who actually interact with the feed** — not just install and bounce. Specifically:

- The 12–15 Columbia classmates who came in through personal outreach and actually swiped through events, saved things, and marked going
- The 3–4 friends-of-friends who were referred by those classmates and also activated

These are not demographics. They are specific people. We know who they are. They're the ones whose taste profiles have enough interaction data to validate whether the recommendation engine is working at all. Without them giving the algorithm real signal, we can't know if the core product loop — swipe → taste profile updates → next card is more relevant — is actually functioning.

### 3. Two Strategies

**Primary strategy: Seeded Personalization (Fake It Till You Make It)**

The taste profile starts cold for every new user. To reduce the time-to-value gap, we seed the profile from the onboarding quiz before the user has swiped anything. The 4-step onboarding (interests, borough, budget, available days) pre-populates category weights, price preferences, and location weights so the first feed is already filtered, not random. The first card a user sees should feel relevant even before a single swipe. This reduces the "why is this showing me CrossFit at 6am" problem that causes immediate churn.

**Secondary strategy: Anchor on a Weekly Ritual**

The algorithm gets sharper with repeated use, which means we need users to come back every week, not just once. We're framing Sift as a Thursday/Friday ritual — "what are you doing this weekend?" — rather than an always-on feed. This is a narrower use case but one with a natural weekly cadence that brings users back without push notifications. All our outreach messaging, onboarding copy, and event timing (we surface events most relevant to the upcoming weekend) reinforces this framing.

### 4. What We're Doing This Week

**For seeded personalization:**
Audit the first 10 events shown to new users after completing onboarding. Pull the first-session card stack for each of our 24 signups and check whether the events match their stated onboarding preferences. If someone said "outdoors + free only + Brooklyn" and their first three cards are paid Manhattan nightlife events, the seeding isn't working. Fix the scoring weight for onboarding-declared preferences vs. cold defaults.

**For the weekly ritual anchor:**
Rewrite the onboarding confirmation screen copy from generic ("you're all set") to ritual-framing ("Your weekend starts here. Come back Thursday to see what's worth doing."). One line change, zero engineering, sets the expectation that Sift is a Thursday check-in, not a daily app.
