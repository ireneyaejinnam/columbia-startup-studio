# Weekly Update — August Fan Club (Evidence of Life)
**Week of April 7, 2026**

## What we built last week and why

We ran our first round of user testing on the sign-up flow — five simulated think-aloud interviews across a mix of students and young professionals, mobile and desktop, varying technical ability. We chose to test sign-up specifically because our concierge onboarding starts this week and we can't onboard anyone if they can't get through the front door.

The results were clear: three breakpoints in the first 30 seconds. The sign-up/sign-in toggle is essentially invisible (5/5 users thought the page froze), the email confirmation link was returning a 404 (now partially fixed — it lands on a "no active session" dead-end instead), and Google OAuth is blocked in every in-app browser. We also shipped a schedule cycle setting that lets users define waking/sleeping hours so the "time remaining" display is personalized.

## What we're building this week and why

Three sign-up fixes: (1) separating sign-in and sign-up into visually distinct states, (2) auto-redirecting after email confirmation instead of the blank "no session" screen, and (3) detecting in-app browsers to prevent the Google OAuth 403 error. These are low-to-medium effort and they're blocking everything downstream — we can't run concierge onboarding, collect retention data, or grow the user base until the first 30 seconds work.

In parallel, Shan is starting concierge onboarding with waitlist users. The goal is to understand the gap between "signed up" and "gets it."

## Current user count

Registered users: ~10. We front-loaded outreach to friends, classmates, and early waitlist signups this week. Sign-up friction has been the primary bottleneck converting interest into active accounts.

## Biggest blocker

Single-threaded engineering. Willow is the critical path for all product work. The sign-up fixes, the "add places" UX redesign, and analytics setup are all competing for her time. We're prioritizing sign-up fixes this week because nothing else matters if users can't create an account.
