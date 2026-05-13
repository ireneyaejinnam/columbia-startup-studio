# Style Guide — QuestCity

**Team:** Team Millionaires (DG-ST-AB)
**Date:** February 26, 2026

---

## Color Palette

| Role | Name | Hex |
|------|------|-----|
| Primary | Quest Orange | `#F4622A` |
| Secondary | Deep Slate | `#1E2A38` |
| Accent | Electric Lime | `#C8F135` |
| Background (light) | Off-White | `#F9F6F0` |
| Background (dark) | Ink | `#111820` |
| Text (primary) | Charcoal | `#1E2A38` |
| Text (secondary) | Stone | `#6B7280` |
| Success | Grass | `#22C55E` |
| Destructive / Warning | Ember | `#EF4444` |

**Rationale:** Orange is energetic and action-oriented without being alarming. The dark slate grounds it. Electric lime provides a game-feel accent (progress bars, XP indicators). The off-white background feels like paper/a map — intentional.

---

## Typography

### Heading Font
**Space Grotesk** (Google Fonts — free)
- H1: 48px / 700 weight / -0.02em letter spacing
- H2: 36px / 600 weight / -0.01em
- H3: 24px / 600 weight
- H4: 18px / 600 weight

### Body Font
**Inter** (Google Fonts — free)
- Body: 16px / 400 weight / 1.6 line height
- Small / caption: 14px / 400 weight
- Button label: 15px / 600 weight / 0.01em letter spacing

### Code / Quest Names
**JetBrains Mono** — used sparingly for quest titles and challenge IDs only

---

## Visual Tone

**Adventure-meets-craft:** Feels like a well-designed field guide — structured, purposeful, with a hint of playfulness. Not loud or gamey. Not sterile or corporate. Confident without being aggressive.

---

## Component Patterns

### Buttons

**Primary CTA button:**
- Background: `#F4622A` (Quest Orange)
- Text: `#F9F6F0` (Off-White), 15px / 600 weight
- Border radius: 8px
- Padding: 14px 28px
- Hover: darken 8% (`#DC541F`)

**Secondary button:**
- Background: transparent
- Border: 2px solid `#1E2A38`
- Text: `#1E2A38`
- Same radius and padding as primary

**Disabled state:** 40% opacity on both

### Quest Cards

- Background: white
- Border: 1px solid `#E5E7EB`
- Border radius: 12px
- Padding: 20px
- Drop shadow: `0 2px 8px rgba(0,0,0,0.06)`
- Quest category badge: small pill, `#C8F135` background, `#1E2A38` text

### CTA Strip

- Background: `#1E2A38` (Deep Slate)
- Text: `#F9F6F0`
- Accent bar: 4px top border in `#F4622A`

### Progress / XP Bar

- Track background: `#E5E7EB`
- Fill: `#C8F135` (Electric Lime)
- Border radius: full (pill shape)
- Height: 8px

### Navigation

- Background: white with 1px bottom border `#E5E7EB`
- Active link: `#F4622A` with bottom underline
- Logo: Space Grotesk 700, "Quest**City**" (City in orange)

---

## Iconography

Use **Lucide Icons** (open source, MIT license). Stroke weight: 1.5px. Size: 20px for UI, 24px for feature sections.

---

## Spacing System

Based on 4px grid. Common values:
- `4px` — tight (within components)
- `8px` — small (between related elements)
- `16px` — base unit
- `24px` — section internal padding
- `48px` — section separation
- `80px` — hero/major section padding
