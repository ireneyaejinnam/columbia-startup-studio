# CLAUDE.md

Project context for Claude (and any new collaborator) working in this repo.

## What this is

**Instaplan** — a social events app for NYC. Internal code name is **HAUNT** (you'll see this in `app/`); the public-facing brand is **Instaplan**. Treat them as the same product.

Tagline: *Your friends know where to go.* We aggregate events from 20+ sources, layer a social graph on top (friends' ratings, "going" / "considering" status, group swipe sessions), and help groups decide where to go without a 14-message group chat.

This is a Columbia Startup Studio (COMS4995-011) project, Spring 2026. Demo Day is May 12, 2026.

## Repo layout

This is a monorepo. The product is in `app/`. Everything else is research, marketing, and coursework artifacts.

```
/
├── app/                          # THE PRODUCT — Expo RN app + Supabase + scrapers
│   ├── src/                      # App source (screens, components, navigation, lib)
│   ├── supabase/migrations/      # DB schema migrations (numbered, never edit a shipped one)
│   ├── supabase/SCHEMA.md        # Plain-English schema reference — read this first
│   ├── scraper/                  # Python scrapers (Ticketmaster, Dice, Eventbrite)
│   ├── __tests__/                # Jest tests
│   └── README.md                 # Full setup + architecture
├── landing_page/                 # Live Instaplan waitlist page (HTML/CSS/JS)
├── potential_landing_page2.0/    # In-progress landing page redesign
├── style_guide/                  # STYLE_GUIDE.md — colors, typography, components
├── synthetic-user-testing/       # LLM-as-user testing pipeline + results
├── interviews/                   # User interview scripts + notes + snapshots
├── idea_generation/              # Lean canvases from team formation
├── feedback_board/               # Standalone HTML feedback widget
├── mhk2182/, sa4166/             # Individual workstreams (briefs, brand work)
├── instaplan_pitch_*.docx        # Demo Day pitch materials
└── HAUNT_*, REMEDIATION_*, SECURITY_AUDIT.md  # Earlier growth + security docs
```

When working on the product, you almost always want to be inside `app/`.

## Tech stack

**Frontend** (`app/`)
- **Expo** (React Native) — single codebase for iOS, Android, web
- **TypeScript** — strict-ish; types live in `app/src/types/`
- **React Navigation** — stack + bottom tabs (Explore, Map, Feed, Chat, Profile)
- **Leaflet** (web) + `react-native-maps` (native) — map screen
- **PostHog** — analytics

**Backend**
- **Supabase** — Postgres + Auth + Row-Level Security + Realtime + Storage. No custom server.
- The Expo client talks directly to Supabase via `@supabase/supabase-js`. RLS policies enforce who-sees-what.
- Edge functions expose public endpoints (`/user-count`, `/metrics`) for the course leaderboard.

**Scrapers** (`app/scraper/`)
- Python 3, run manually or on cron. Uses the Supabase service key (bypasses RLS) and deduplicates on `source_id`.

**Landing page**
- Static HTML/CSS/JS. Deployed separately. Tracks signups + UTM params with PostHog.

## Database

16 tables. Full reference in `app/supabase/SCHEMA.md`. The main groupings:

- **Identity & social:** `profiles`, `friendships`, `friend_groups`, `friend_group_members`
- **Events & activity:** `events`, `event_logs`, `event_log_companions`, `event_invites`, `feed_items`
- **Group decision-making:** `swipe_sessions`, `swipe_session_members`, `swipe_votes`
- **Chat:** `conversations`, `conversation_members`, `messages`

Migrations are numbered (`001_schema.sql`, `002_…`, etc.) and additive. Never edit a shipped migration — write a new one.

## Conventions

**Git workflow**
- Branch off `main`. Name branches `feat/<thing>`, `fix/<thing>`, `cleanup/<thing>`, `feature/<thing>` (we're inconsistent on the prefix, but pick one of those).
- One feature per branch. Open a PR. Don't push to `main` directly.
- Squash on merge is fine. Keep PR titles descriptive — they end up in the changelog by virtue of the git log.

**Code style**
- TypeScript everywhere in `app/`. Prefer `import type` for type-only imports.
- Components in `app/src/components/`, screens in `app/src/screens/`, shared logic in `app/src/lib/`.
- Theme tokens (colors, spacing, category colors) live in `app/src/constants/theme.ts` — use them, don't hardcode hex values.
- Supabase queries: import the client from `app/src/lib/supabase.ts`. Don't instantiate new clients ad-hoc.

**Secrets & env**
- Never commit `.env`. Use `.env.example` as the template.
- `EXPO_PUBLIC_*` vars are public (bundled into the client) — only put the Supabase URL and anon key here.
- The Supabase service key belongs in `scraper/.env` only — never in the app bundle.

**Testing**
- Jest config in `app/jest.config.js`, setup in `app/jest.setup.js`. Tests live in `app/__tests__/`.
- Playwright e2e setup exists on the `feat/playwright-e2e` branch.

**Analytics**
- PostHog is wired into both the app and the landing page. Funnel events fire on signup, first login, first event log, and first chat message.
- The course leaderboard pulls from `/metrics` and `/user-count` edge functions — don't break their schemas.

## Team & rough roles

| Member | UNI | Primary focus |
| --- | --- | --- |
| Thomas Kennedy | trk2121 | Engineering — app + backend |
| Saanvi Aima | sa4166 | Product, design, brand, landing page |
| Anuraag Pandhi | ap4533 | Engineering + growth experiments |
| Michael Karnes | mhk2182 | Engineering — app + infra |
| Marium Ahmed | ma4354 | Research, synthetic testing, demand gen |

Roles overlap — everyone codes when needed, everyone writes copy when needed.

## Where to look first

- **What is this product?** → Top of this file, plus `instaplan_pitch_script.docx`
- **How do I run it?** → `app/README.md`
- **What's in the database?** → `app/supabase/SCHEMA.md`
- **What does it look like?** → `style_guide/STYLE_GUIDE.md`, `landing_page/index.html`
- **What have we learned from users?** → `interviews/`, `synthetic-user-testing/`
- **What's broken / planned?** → Roadmap at the bottom of `app/README.md` and open PRs/issues on GitHub

## Things to know that aren't obvious

- The brand changed mid-semester from **HAUNT** to **Instaplan**. The React Native app code, supabase project name, and earlier docs still say HAUNT. Don't rename — it's working and the demo is tomorrow.
- RLS is on but the "friends-only visibility" rules aren't fully wired everywhere yet. If you add a query that returns user content, double-check whether it's leaking across the friendship boundary.
- The scrapers can produce duplicate events across sources. The dedup logic in `app/scraper/utils.py` handles this via `source_id` + fuzzy match on title + venue + start_time.
- The map screen uses two different libraries (Leaflet on web, `react-native-maps` on native) because there's no single library that works well in both Expo web and native. They're abstracted behind the same screen-level interface.

## When in doubt

Read `app/README.md` first — it's the most up-to-date description of the actual product surface. This file is meant to be the index; the app README is the source of truth for setup and architecture.
