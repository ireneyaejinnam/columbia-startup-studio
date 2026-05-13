# Growth Strategy

Goal: drive 20+ real users through the funnel with enough granularity to learn which channel actually converts, not just which channel makes noise — and then keep the network alive past the first week by addressing the cold start problem head-on.

This doc is structured in three parts:

- **Part 1** (due April 2): channel selection, draft messaging, success criteria.
- **Part 2** (due April 9): results per channel, what worked, what we're changing.
- **Cold Start Strategy** (due April 9): how we get the network off the ground.

---

# Part 1 — Channels, Approach, Success Criteria

## TL;DR

We're a social events app for NYC. The differentiator is the social layer (who's going, friends logging events), not the event catalog. That tells us where to fish: places where NYC-anchored people who already make plans together hang out. For Part 1, we're running two channels in parallel — our personal social graph (free, warm) and paid Reddit Ads targeted at NYC-focused subreddits (cold, $75 spend) — because the failure modes are different enough that we'll learn from running them simultaneously rather than sequentially.

---

## Channel 1: Personal social graph (ours + our friends')

### Who, specifically

- Direct first-degree contacts in NYC: classmates at Columbia, friends and friends-of-friends in the 20–30 age range living in Manhattan or Brooklyn, anyone we've gone to an event with in the last six months.
- Second-degree: we ask each first-degree contact who signs up to share with one specific friend group (their roommates, their grad cohort, their workout group, etc.). The ask is targeted — "share with the three people you'd actually go to a concert with" — not a generic "tell your friends."

### Volume commitment

- **30 personal DMs over 5 days** (6/day average), split across the founding team. Sent on iMessage, Instagram DM, and WhatsApp depending on where the relationship lives.
- **10 follow-ups** on day 4 to people who opened but didn't sign up.
- For every contact who signs up, **1 nudge** to bring in one friend group.

### Draft message

Cold-ish (someone we haven't talked to in a few months):

> hey — quick one. been building a social events app for nyc with my team for class — it's basically eventbrite + the social layer (you can see what your friends are going to, plan things together, log stuff after). looking for ~20 people to actually try it this week and tell us what's broken. would take you 5 min and you'd genuinely be helping. cool if i send the link?

Warm (a close friend):

> ok need a favor. we're testing the app this week and i need real users on it. can you sign up + try to find one event you'd actually go to? if it sucks tell me exactly where, that's the whole point. [link]

Follow-up at day 4 if they opened but didn't sign up:

> no pressure if you're slammed — but if you've got 5 min today, the funnel data on whether you bounce or not is genuinely useful to me. [link]

The "share with one friend group" ask, after they sign up:

> ok one more — could you send it to the [roommates / lab / whoever] group chat? that's the test we actually need, whether it's useful when a few friends are all on it.

### Why this channel

The product's value is unlocked when you have friends on it. A friend group joining together is worth more to us than ten isolated signups, both for our metrics (active usage, not just signups) and for the user experience (an empty feed makes the whole thing feel dead). Personal DMs are the only realistic way to get a clustered signup pattern in week one.

---

## Channel 2: Paid Reddit Ads targeting NYC subreddits

### Which subreddits, specifically

- r/nyc
- r/AskNYC
- r/WhatsHappeningNYC
- r/nycevents
- r/Columbia
- r/FoodNYC
- r/NYStateofMind

### Approach: paid Reddit Ads, community-targeted

Rather than posting organically (which risks mod removal and patterns as spam at our size), we're running paid promoted posts via Reddit Ads Manager with **community targeting** — Reddit's most distinctive feature, which serves ads directly to users actively browsing the subreddits we care about. We layer NYC geo-targeting on top so we're not spending impressions on the half of r/nyc that doesn't actually live in NYC.

### Budget and volume commitment

- **Total budget: $75 over 5 days ($15/day).** Naming the tradeoff up front: this is well below the ~$50/day that Reddit Ads guides recommend for the optimization algorithm to do its job. At $15/day with typical Reddit CPCs of $0.75–$2.00, we're looking at roughly 7–20 clicks per day and 35–100 clicks total over the run. That's a small enough sample that a single high-performing or low-performing day can swing our conclusions, and Reddit's "Maximize Conversions" bidding will probably underperform because it won't see enough conversion events to learn from. We're going in with eyes open: this is a budget-constrained test, not a definitive read on the channel. We'll treat the directional signal seriously but won't kill or scale the channel based on $75 of data alone.
- **One ad group**, targeting all seven subreddits as a cluster, with NYC geo-targeting layered on. At this budget, splitting per-subreddit is impossible — we'd starve every cell. Single ad group is the only viable structure.
- **Two ad creatives** running simultaneously so we get _some_ A/B signal, even if the per-creative data is noisy. Refresh if either tanks below 0.3% CTR after 48 hours.
- **Bid strategy:** **manual CPC capped at $1.25.** Skipping automated bidding here — at $15/day the algorithm won't accumulate enough conversions to optimize, and manual gives us tighter cost control on a small budget.
- **Tracking:** Reddit Pixel installed on the landing page before launch, firing on page view + signup. Even if the volume is too low for the algorithm to optimize on, the pixel data still gives us clean attribution for our own analysis.

### Draft ad creative #1 (problem-led, native Reddit voice)

> **Headline:** Escape the group chat
> 
> **Body:** Image of 3 screens on branded background (think standard image based ad)
> 
> **CTA button:** Sign up

### Draft ad creative #2 (social-layer-led, more direct)

> **Headline:** Escape the 
> 
> **Body:** Image of Poll screen with brief problem focused text.
> 
> **CTA button:** Sign up

### Why this channel

Reddit's community-targeting puts us in front of people _while they're actively reading NYC subs_ — i.e., already in the mindset of "what's going on in this city." That's the exact decision moment our product is for. Compared to organic posting, paid ads sidestep the mod-removal risk and give us guaranteed delivery and clean attribution data through the Reddit Pixel. The honest tradeoff: at $75 of total spend, we won't get enough volume to make a definitive call on the channel — we'll get a directional read at best. But it's still the cleanest available source of cold-traffic signup data for the week, and combined with our personal-graph results, it's enough to inform Part 2's bigger decision about whether to invest more in paid acquisition.

---

## What does success look like

We're tracking per channel, not in aggregate, because the whole point of running two channels is to learn which one to double down on next week.

### Per-channel targets for the 5-day window

|Metric|Personal graph|Reddit Ads|
|---|---|---|
|Spend|$0|$75|
|Reach (DMs sent / impressions)|30 DMs sent|6,000–10,000 impressions|
|CTR / response rate|60%+ open-and-click|0.5%+ CTR (35–60 clicks)|
|Cost per click|n/a|under $2.00|
|Signups|50%+ of clicks (~10)|10%+ of clicks (~5)|
|Cost per signup|n/a|under $20|
|Active users (did one meaningful action)|70%+ of signups (~7)|40%+ of signups (~2)|
|Friend-cluster signups (≥2 people from same group)|2 clusters|0 expected|

The numbers are different on purpose. Personal DMs should convert at much higher rates because the trust is pre-existing — if we're sending 30 DMs and only getting 3 signups, the message is wrong, not the channel. Reddit ad traffic is much colder, so a 10% click-to-signup rate is the healthy benchmark. The Reddit signup target (~5) is small because the budget is small; that's a real limitation of this test, not a design choice. If Reddit drives more raw signups but personal DMs drive more _active_ users and friend clusters, that's a real signal about which channel matters for retention vs. vanity metrics.

### Total floor

20+ signups across both channels combined, with at least 8 active users (per our `/api/metrics` definition of active) and at least 2 friend clusters of 2+ people each. If we hit the signup number but not the activity number, that's a product problem, not a channel problem, and the user testing findings should already be addressing it.

### How we'll know a channel is working

- **Personal graph is working if:** we see friend clusters forming (multiple people from the same DM thread signing up within a day of each other), and post-signup activity rate is above 70%. If we get signups but no clusters, the "share with one friend group" ask is failing and we need to rework it.
- **Reddit Ads is working if:** CTR clears 0.5%, cost-per-signup stays under $20, and we can see _any_ meaningful difference between the two creatives (gives us a creative direction for Part 2). At $75 of total spend we won't get statistical certainty on any of these, but a directional read is the realistic goal. We let the campaign run the full 5 days regardless — pulling it early would shrink an already-small dataset for a savings of ~$30. The decision about whether to keep investing in Reddit Ads in Part 2 will weigh this directional read alongside the personal-graph results.

---

# Part 2 — Results, Analysis, What's Next

## Reddit Campaign Update — 4/30

Campaign ran 4/23–4/29. Creative #2 was added on 4/26, so it had ~4 days of exposure vs. ~7 for Creative #1 — relevant context, but as the data below shows, the per-creative gap is too wide to be explained by exposure window alone.

### Results

**Reddit Ads (Ads Manager, 4/23–4/29)**

|Metric|Result|Part 1 target|Outcome|
|---|---|---|---|
|Spend|$84.60|$75|Over by $9.60|
|Impressions|6,742|6,000–10,000|In range|
|Clicks|54|35–60|At top of range|
|CTR|0.801%|0.5%+|✅ Cleared|
|CPC|$1.57|under $2.00|✅ Cleared|

**Landing page traffic (instaplan.org analytics, last 7 days)**

|Metric|Result|
|---|---|
|Visitors|47|
|Page views|59|
|Sessions|53|
|Avg session duration|1m 34s|
|Bounce rate|74%|
|Mobile / Desktop split|42 / 5 (89% mobile)|

**Per-creative breakdown (UTM content)**

|Creative|Visitors|Views|
|---|---|---|
|triplescreens (Creative #1, problem-led)|44|46|
|tripleswipe (Creative #2, social-layer-led)|2|3|
|untagged|2|10|

**Click-to-visitor reconciliation:** Reddit reports 54 clicks; site analytics shows 47 visitors. The ~13% gap is consistent with normal cold-traffic loss (bot clicks, abandoned page loads, tracking-blocked browsers), so attribution is clean.

**Signups:**  3

### What worked

CTR of 0.801% beat the 0.5% target by 60%. For a $15/day spend on a single ad group with no bid optimization, that's a genuine signal that Reddit's community-targeting is putting us in front of the right people — NYC subreddit readers responded to the ad at a healthy rate. CPC of $1.57 also came in under our $2.00 ceiling.

Creative #1 ("Escape the group chat" / triplescreens) carried the entire campaign. 44 of 47 site visitors came through it. The problem-led, native-Reddit voice landed better than the more explanatory one — worth taking as a creative direction signal even though we didn't get a clean A/B test (see below).

### What didn't

**The A/B test didn't actually run.** triplescreens drove 44 visitors; tripleswipe drove 2. A 22:1 split can't be explained by Creative #2's shorter exposure window — at minimum it should have produced 15–20 visitors over 4 days at parity. Either Reddit's algorithm starved Creative #2 of impressions (likely, given that at $15/day with manual CPC the system tends to concentrate budget on whichever creative wins early), or the social-layer pitch genuinely didn't click with cold Reddit traffic. We can't distinguish those two explanations from this data, which is itself a finding: at this budget, you don't get to A/B test, you get one creative that runs.

**Bounce rate is the real story.** 74% bounce with a 1m 34s average session means the ad is working but the landing page isn't. People are clicking through and leaving without converting — exactly the "landing page not tuned for cold Reddit traffic" failure mode we flagged as a risk in Part 1. The Reddit pixel and CTR numbers tell us we found the right audience; the bounce rate tells us the landing page didn't close them.

**Budget overrun.** Spent $84.60 against a $75 cap — small ($9.60), but Reddit's daily-budget pacing isn't strict and we should set a hard campaign-level cap next time rather than relying on the daily.

**Volume is too small to make scaling decisions on.** Even with the wins, 47 visitors and an unknown-but-small signup count is a directional read, not a statistical one — exactly what we said going in.

### What we're changing next

The directional bar from Part 1 was: CTR ≥ 0.5%, CPS ≤ $20, clear creative winner. Two of three cleared cleanly (CTR, creative winner); CPS depends on the signup number we'll plug in, but bounce rate suggests it's the weak link. Decisions:

1. **Fix the landing page before spending another dollar on Reddit.** A 74% bounce rate is a product/page problem, not a channel problem. Specifically: 89% of our traffic is mobile, so the mobile landing experience is what matters — not desktop. Audit the mobile page for load speed, above-the-fold value prop clarity, and whether the signup CTA is actually visible without scrolling. Ship fixes before re-running ads.
2. **Run Creative #1 again at higher budget once the page is fixed.** triplescreens earned the right to a real test. Step daily budget up to ~$50/day (the threshold Reddit's optimizer needs to learn) and split the ad group by individual subreddit to find which NYC subs actually convert.
3. **Replace Creative #2 with a different second creative.** tripleswipe didn't get a fair test, but the campaign also doesn't owe it one — write a new variant with a clearer NYC-specific hook and run it head-to-head with triplescreens at the higher budget.
4. **Set a hard campaign-level budget cap** to avoid the small overrun pattern repeating at scale.

---

# Cold Start Strategy

**Added:** Following the April 9 class on the Cold Start Problem.

This section addresses how we get the network off the ground when "social events app" is dead-on-arrival without enough friends already on it. It builds on the Part 2 results above — specifically, the finding that friend clusters drive activity in a way isolated signups don't.

---

## 1. Cold start type

**Network.**

The product's value to any individual user is a direct function of how many of their friends are also on it. The whole differentiator we keep coming back to in user testing — "see who's going," "coordinate with friends," "plan together" — only works once a user's social graph has at least 2–3 people on the app. Without that, we look like a worse Eventbrite, which is exactly what testers told us in week 10. This isn't a marketplace (no two-sided supply/demand), not content/supply (events come from external feeds, not UGC), not invite-only/status, and AI isn't the moat. It's a network problem, and the cold start dynamic is the dominant constraint on growth right now.

## 2. Who is our hard side?

The hard side is **the planners** — the people in any friend group who actually start the "what are we doing this weekend" conversation. They're the ones who screenshot Eventbrite into the group chat. They're the ones who text "this looks fun" first. If they don't adopt the app, no one downstream of them does either, because the rest of the group is reactive. They're the supply side of social plans inside any given friend group.

The assignment's bar is naming specific people, not a role. We haven't done that yet because it requires team buy-in — each founder needs to commit to which specific 2–3 planners in their own network they're personally responsible for converting, and we want that to be a real commitment made together rather than a list one person assembles unilaterally. We're aligning on this at our next team sync and will update this doc with the named list (target: 8–10 specific planners) once everyone's committed. Until that list exists, our cold-start strategy is fiction — naming names is the gating exercise.

## 3. Two strategies

From the seven-strategy menu in the class deck ("Pick Two, Not Seven"), our two are **Constrained Launch** (primary) and **Single-Player Mode** (secondary). Reasoning for why these two and not the others is at the end of this subsection.

### Primary: Constrained Launch — pick one tight cluster and saturate it

> _"100% of a small network beats 1% of a large one."_

Pick **one** friend group, dorm floor, grad cohort, or club, and saturate it. The goal is to get to a point where, inside that one group, opening the app actually shows you who's going to what. Not 5% of your friends — most of them. That's the smallest viable network for our product, and until we have one of those working, expanding broader is a waste.

### Secondary: Single-Player Mode — useful alone first, social layer activates as friends join

> _"Come for the tool, stay for the network."_

Make the app useful to a single user with zero friends on it — so they don't churn while waiting for the network to fill in. The "tool" is the event-discovery and map functionality (the parts testers consistently said they liked). The "network" is the social layer that activates as friends join.

In practice: invest in making Explore + Map genuinely good at "what's happening in NYC tonight" even for a solo user. That's our retention floor for any user we acquire faster than their friends do. This buys us time on the cold-start problem — instead of a single-player experience that feels broken, the user gets a real utility, and the social layer gradually lights up as their friends join. The deck calls out **Eventbrite** as a class example here, which is on the nose — the brutal version of this strategy is "if our solo experience isn't at least as good as Eventbrite's, no one stays long enough to find out we have a social layer." That's the bar.

Why we picked these two (and not the other five): **Seed the Supply** is partly already done — events come from external feeds, not us populating them. **Invite Mechanics** doesn't fit our stage; no one's clamoring for invites yet, so artificial scarcity would feel fake. **Wizard of Oz** doesn't apply because we're not faking supply. **Piggyback** is interesting (Eventbrite/Ticketmaster deep links via the Get-Tickets CTA already piggyback on their distribution), but it's a tactic inside our funnel, not a primary cold-start lever. **Event-Driven Launch** — tying the launch to a specific NYC density moment like Columbia's Bacchanal or a major festival weekend — is the strongest alternative we considered, and we'd reach for it next if Constrained Launch stalls. Two-strategy focus was the call; we're not running seven plays at once.

These two strategies pair well: Constrained Launch attacks the cold-start problem at the cluster level, while Single-Player Mode keeps individual users alive while we work on getting their cluster onboard.

## 4. What we can do THIS WEEK

### For Constrained Launch

**Pick the cohort and run a 30-minute in-person onboarding session.** Concretely: team members reach out to their network group chats this week and schedule a 30-minute session where everyone signs up together, follows each other in-app, and saves at least one event each. The goal is to get 15+ people from the same group on the app, mutually connected, in a single session — a saturated small network bootstrapped in 30 minutes, vs. weeks of isolated DMs.

Done = at least 15 people from one cohort signed up, following each other, with at least one event saved each. Measurable, time-boxed, this week.

### For Single-Player Mode

**Audit Explore + Map for solo-user utility and ship the top 3 fixes.** The user testing already gave us the list: address taps don't open Maps, filter changes don't apply without refresh, scroll doesn't initialize on first load, recommendations don't reflect onboarding selections. These are exactly the fixes that determine whether a solo user (someone whose friends aren't on the app yet) finds the tool useful enough to stick around. We pick the three highest-impact items from the user_testing.md priority list and ship them before the in-person onboarding session, so when the cohort does sign up, they don't bounce off the same broken-first-minute issues testers flagged.

Done = three specific bugs from the user_testing.md priority list shipped to production this week. Not "in progress." Shipped.