# Weekly Update — 2026-04-28

**Team:** Standard Deviants
**Product:** HAUNT — social events app for NYC

## What we built last week and why

Going-Out Status shipped before the April 23 feature freeze: users can toggle available / maybe / offline with an optional time and note, and friends see it on a "Who's Out" screen and in the feed. We hit freeze with the core loop intact (browse → log → share → coordinate) plus the going-out nudge layer. Past freeze, we shifted into iteration mode: tightened the onboarding flow (cut a screen, moved the friend-add prompt earlier), patched an RLS bug that was leaking some friends-only logs, and ran user testing sessions on the new flow with strangers recruited via Reddit and Columbia channels — synthesis is in `20260402/user_testing.md`.

We also drafted the pitch deck (live + leave-behind versions, in `pitch_draft1_live.pdf` and `pitch_draft1_leavebehind.pdf`) for class today.

## What we're building this week and why

No new features, per freeze. Focus is on (1) onboarding polish based on the user-testing findings — the first-minute-to-aha gap is too long for cold visitors; (2) running a second Reddit Ads creative cycle now that we have funnel data from the first one to point at what's working; (3) tightening the pitch based on whatever feedback we get in class today. Demo Day is two weeks out and the slope of the user count between now and then is the most important slide in the deck.

## Current user count

15 signups, 9 active users, 2 friend clusters of 2+ people.

## Biggest blocker

Activation, not acquisition. We're getting people to sign up but the drop between signup and first meaningful action is bigger than we'd like. The user testing identified it (people don't immediately see what to *do* after the empty feed) and we have changes queued, but every fix has to clear "is this a feature change in disguise" given freeze.
