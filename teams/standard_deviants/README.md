# Instaplan

A social events app for NYC. Pulls events from 20+ sources (Ticketmaster, Dice.fm, Eventbrite, and more), shows you where your friends actually went, and helps your group decide what to do in seconds.

Think Beli for events — your friends' ratings instead of strangers' star ratings, group decision-making for plans, and a "looking to go out" nudge system.

> Internally, the React Native app is still named **HAUNT** (it was our working title earlier in the semester). The public product, landing page, and pitch materials use **Instaplan**.

Built by Team Standard Deviants for Columbia's *Startup Studio: AI-Accelerated Building & Validation* (COMS4995-011), Spring 2026.

## Team

- Thomas Kennedy (trk2121)
- Saanvi Aima (sa4166)
- Anuraag Pandhi (ap4533)
- Michael Karnes (mhk2182)
- Marium Ahmed (ma4354)

## What's in this repo

This is a monorepo containing both the product and the research/marketing artifacts that fed into it.

| Path | What's there |
| --- | --- |
| `app/` | The actual product — Expo (React Native) app + Supabase backend + Python scrapers. See `app/README.md` for full setup and architecture. |
| `landing_page/` | Live landing page (`index.html`) — the Instaplan-branded waitlist page that drives signups. |
| `potential_landing_page2.0/` | In-progress redesign of the landing page. |
| `style_guide/` | `STYLE_GUIDE.md` — color palette, typography, visual tone, component patterns. |
| `idea_generation/` | Lean canvases and idea-stage docs from team formation week. |
| `interviews/` | User interview scripts, raw notes, and snapshots. |
| `synthetic-user-testing/` | LLM-as-user synthetic testing pipeline — audience configs, prompts, results, and A/B comparisons that validated copy and product direction. |
| `feedback_board/` | Standalone HTML feedback widget. |
| `mhk2182/`, `sa4166/` | Individual workstream folders (briefs, brand positioning, landing-page exploration). |
| `instaplan_pitch_script.docx` | Demo Day pitch script. |
| `instaplan_stage_cards.docx` | Stage cards / cue cards for the live pitch. |
| `HAUNT_Growth_Strategy.docx`, `HAUNT_Remediation_Plans.docx`, `REMEDIATION_PLANS.md`, `SECURITY_AUDIT.md` | Earlier growth, security audit, and remediation docs (under the prior HAUNT name). |

## Running the app

The app lives in `app/`. Quick version:

```
cd app
npm install
cp .env.example .env   # fill in Supabase URL + anon key
npx expo start
```

Then press **w** for web, **i** for iOS simulator, **a** for Android emulator, or scan the QR code with Expo Go.

Full setup instructions (including the Python scrapers in `app/scraper/`) are in [`app/README.md`](app/README.md). Database schema is documented in [`app/supabase/SCHEMA.md`](app/supabase/SCHEMA.md).

## Stack

- **Frontend:** Expo (React Native) with TypeScript — one codebase for iOS, Android, and web
- **Backend:** Supabase (Postgres + Auth + RLS + Realtime + Storage) — no custom server
- **Scrapers:** Python (Ticketmaster Discovery API, Dice.fm, Eventbrite)
- **Analytics:** PostHog
- **Landing page:** Static HTML/CSS/JS, deployed standalone
- **Deployment:** Supabase (backend) + Expo for app distribution; landing page deployed separately

## Public API

- `https://dwnxxhyrwqchzlqudhkw.supabase.co/functions/v1/user-count` — live user count
- `https://dwnxxhyrwqchzlqudhkw.supabase.co/functions/v1/metrics` — funnel + activity metrics

## Working in this repo

We use feature branches and pull requests. Never push directly to `main`. Recent active branches include `feat/*`, `feature/*`, `fix/*`, and `cleanup/*` — see the open PRs on GitHub for the current state of work.

For project context, conventions, and roles, see [`CLAUDE.md`](CLAUDE.md).
