# STYLE_GUIDE.md — Sift

**Purpose:** Define the visual identity for Sift so that every page, screen, and asset feels cohesive. This document is also an AI onboarding doc: when you hand it to a code agent alongside your BRAND_POSITION.md, the agent generates consistent, on-brand output.

---

## 1. Visual Tone

**Overall feel:** Quiet confidence. Clean enough to get out of the way, grounded enough to feel trustworthy. The design should feel like a deep breath before a good weekend.

**What it is:** Minimal, calm, decisive

**What it is not:** Not playful, not flashy, not corporate, not trendy

---

## 2. Color Palette

| Name | Hex | Role |
|------|-----|------|
| **Steel Blue** | #547AA5 | Primary accent — buttons, links, CTAs, focus states |
| **Warm Stone** | #A68B6B | Warm accent — "ending soon" tags, category badges, urgency indicators, highlights |
| **Slate** | #4F5165 | Secondary UI — dividers, muted labels, helper text, hover states |
| **Off-White** | #EFEFF0 | Page canvas and card backgrounds |
| **Dark Teal** | #293132 | Body text and headings |
| **Error Red** | #C0392B | Error states, alerts, destructive actions |

### Color Rules

- Use `#293132` (Dark Teal) for all body text and headings — never pure black (`#000000`)
- `#547AA5` (Steel Blue) is the primary action color; use it for CTAs, links, and interactive elements
- `#A68B6B` (Warm Stone) provides temperature contrast — use it sparingly for urgency, category tags, and moments of delight (e.g., "Matched because…" indicators). It should feel like a reward, not decoration
- `#4F5165` (Slate) works for secondary UI: dividers, subtle labels, metadata text, disabled states
- `#EFEFF0` keeps the canvas light without being stark white
- Ensure sufficient contrast between text and background (WCAG AA: 4.5:1 ratio minimum for body text)
- Steel Blue on Off-White passes AA for large text; pair with white text on filled buttons

---

## 3. Typography

**Heading font:** Merriweather (serif — editorial, grounded, deliberate)
**Body font:** Inter (sans-serif — clean, highly readable, pairs with everything)

### Type Scale

| Style | Size | Weight | Usage |
|-------|------|--------|-------|
| Display | 2.75rem | Medium 500 | Hero headline only — one per page |
| H1 | 2.25rem | Medium 500 | Page titles, primary headings |
| H2 | 1.75rem | Bold | Section titles |
| H3 | 1.375rem | Semibold | Subsection headers |
| Body | 1rem | Regular | Paragraph text |
| Small | 0.875rem | Regular | Captions, labels, helper text, metadata |

### Typography Rules

- Merriweather headings should feel deliberate — short, declarative, unhurried
- Body copy in Inter at 1rem with generous line-height (1.6–1.75) for readability
- Avoid bold in body text except for structural emphasis (e.g., a key term in a paragraph, not entire sentences)
- Letter-spacing on Merriweather headings: subtle negative tracking (-0.01em to -0.02em) for polish
- Use Merriweather italic for pull quotes, the tagline, and editorial emphasis — not for headings at scale
- At mobile sizes (≤ 480px), Display drops to 2rem and H1 drops to 1.75rem

---

## 4. Component Patterns

### Buttons

| Type | Style | Usage |
|------|-------|-------|
| **Primary CTA** | Filled `#547AA5`, white text, 8px border radius, hover: `#466A91` + subtle lift (translateY -1px, light shadow) | Main action: "Get Started", "Join Waitlist", "Show me what's happening" |
| **Secondary** | Outlined `#547AA5` (1.5px border), transparent background, 8px border radius, hover: `#547AA5` fill at 8% opacity | Alternative or lower-priority actions |
| **Ghost** | No border, `#4F5165` text, hover: underline | Navigation links, inline actions, tertiary options |

### Recommendation Cards

These are the core product moment — where users decide "this app gets me." Design them with care.

- Background: white (`#FFFFFF`) on the Off-White canvas for subtle elevation
- Border: 1px solid `#E0E0E2`
- Border radius: 10px
- Padding: 20–24px
- Left accent border: 4px solid `#547AA5` (default) or `#A68B6B` (for "ending soon" cards)
- Shadow: `0 1px 3px rgba(0,0,0,0.06)` — barely there, just enough separation

**Card anatomy:**

| Element | Style |
|---------|-------|
| Event title | H3 (Merriweather, 1.375rem, Semibold) |
| Details line (location · price · date) | Small (Inter, 0.875rem), `#4F5165` |
| "Matched because…" line | Small (Inter, 0.875rem), `#547AA5`, italic |
| "Ends in X days" badge | Small (Inter, 0.875rem), `#A68B6B`, semibold — only shown when ≤14 days remain |
| Category tag | Pill shape (16px height, 6px horizontal padding, 4px border radius), `#A68B6B` text on `#A68B6B` at 12% opacity background |

### General Cards (non-recommendation)

- Background: `#EFEFF0` or white
- Border: 1px solid `#E0E0E2`
- Border radius: 10px
- Padding: 20–24px
- No heavy shadows; prefer subtle border definition

### Form Inputs

- Border radius: 8px
- Border: 1px solid `#D0D0D2`
- Focus state: border shifts to `#547AA5`, plus 2px offset ring in `#547AA5` at 30% opacity
- Placeholder text: `#9A9AA0`
- Error state: border shifts to `#C0392B`, helper text in `#C0392B` below the field

### Tags & Badges

- Category tags: pill shape, `#A68B6B` text on light Warm Stone background (`rgba(166,139,107,0.12)`)
- Status badges ("Free", "Ending soon"): same pill shape, color varies by status:
  - Free → `#547AA5` text on light Steel Blue background
  - Ending soon → `#A68B6B` text on light Warm Stone background
  - New → `#4F5165` text on light Slate background

---

## 5. Imagery & Icons

**Icon style:** Lucide icons — thin stroke (1.5px), rounded caps, consistent weight. Use at 20px or 24px for UI elements.

**Photography style:** Real NYC locations, natural lighting, no people in frame. Capture the space, not the crowd. Moody is better than bright — golden hour, quiet gallery interiors, a pop-up storefront at dusk. Photography should make the user feel like they're discovering something, not being sold something.

**What to avoid:**
- Stock photography of any kind
- Staged lifestyle shots or influencer-style imagery
- Heavy gradients, decorative flourishes, or anything that clutters the canvas
- Illustrations that feel cute or whimsical — Sift is calm, not playful

---

## 6. Spacing & Layout

**Base unit:** 8px

| Token | Value | Usage |
|-------|-------|-------|
| xs | 4px | Tight gaps (icon-to-label, badge padding) |
| sm | 8px | Compact spacing (within components) |
| md | 16px | Default spacing (between related elements) |
| lg | 24px | Section padding, card internal spacing |
| xl | 32px | Between content sections |
| 2xl | 48px | Major section breaks |
| 3xl | 64px | Page-level vertical rhythm (hero to first section, etc.) |

**Max content width:** 720px for text-heavy pages (landing page body, blog posts). 1080px for card grids and dashboards.

**Grid:** 12-column on desktop, collapse to single column on mobile. Gutters: 24px.

---

## 7. Motion & Interaction

Keep it minimal. Motion should feel like a response, not a performance.

- **Button hover:** 150ms ease — darken fill + translateY(-1px) + shadow fade-in
- **Card hover:** 150ms ease — shadow deepens slightly (`0 2px 8px rgba(0,0,0,0.1)`)
- **Page transitions:** None. Sift loads fast and gets out of the way.
- **Loading states:** Subtle pulse animation on skeleton placeholders, not spinners
- **No parallax, no scroll-triggered animations, no bouncing elements.** The brand is calm.

---

## Implementation Notes

- **CSS framework:** TBD — style tokens above are framework-agnostic (Tailwind-ready if needed)
- **Deployment:** TBD
- **Responsive breakpoints:**
  - Mobile: 375px (minimum test width)
  - Tablet: 768px
  - Desktop: 1080px
- **Font loading:** Load Merriweather (400, 400i, 500, 700) and Inter (400, 500, 600) from Google Fonts. Use `font-display: swap` to avoid layout shift.
- **Dark mode:** Not planned for V1. If added later, swap Off-White → `#1A1A1A`, Dark Teal → `#E0E0E0`, and adjust card/component backgrounds accordingly.
