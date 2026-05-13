# Evidence of Life — Style Guide

**Team:** August Fan Club  
**Date:** February 2026  
**Landing page:** https://evidenceoflife.vercel.app/

---

## 1. Visual Tone

**Overall feel:** Minimal, warm, reflective, and calm — a productivity product that feels supportive rather than stressful.

**What it is:**
- Quietly intelligent
- Grounded and emotionally clear
- Soft, personal, and evidence-driven

**What it is not:**
- Not a cold enterprise productivity dashboard
- Not a gamified hustle app
- Not a generic journaling template

Evidence of Life should feel like a gentle daily operating system: structured enough to help users see their time, but warm enough that imperfect days still feel valid.

---

## 2. Color Palette

| Name | Hex | Role |
|------|-----|------|
| **Deep Navy** | `#27496D` | Primary brand color — headings, primary CTA, key actions |
| **Warm Terracotta** | `#D9825B` | Accent color — highlights, section labels, emotional emphasis |
| **Sage Evidence Green** | `#7FA68A` | Evidence / success color — completed states, recap, calm validation |
| **Soft Slate Blue** | `#6B7A99` | Secondary text, supporting labels, subtle UI structure |
| **Warm Off-White** | `#FAF7F2` | Page background and landing page canvas |
| **Light Mist** | `#F3F5F7` | Card backgrounds, timeline panels, soft UI surfaces |
| **Charcoal** | `#1F2933` | Primary body text and strong readable copy |
| **Muted Gray Blue** | `#6B7280` | Secondary body text, helper text, captions |
| **Soft Error Red** | `#C7524A` | Form errors, warning states, destructive actions |

### Color Rules

- Use Deep Navy for the strongest product identity moments: hero headline, primary buttons, and major headings.
- Use Warm Terracotta sparingly for emphasis, not as the main UI color.
- Use Sage Evidence Green for moments of completion, proof, recap, or “this counted.”
- Keep backgrounds warm and soft. The product should not feel sterile or overly clinical.
- Avoid pure black text. Use Charcoal for readability with a softer tone.

---

## 3. Typography

**Heading font:** Playfair Display, Georgia, or a similar editorial serif  
**Body font:** Inter, system sans-serif, or a clean modern sans-serif

The brand uses a contrast between emotional/editorial headings and clean functional body text. Headlines should feel memorable and human; body copy should feel clear and lightweight.

### Type Scale

| Style | Size | Weight | Usage |
|-------|------|--------|-------|
| H1 | 3.5rem–4.5rem | 700 | Hero headline, product identity |
| H2 | 2.25rem–2.75rem | 650 | Major landing page sections |
| H3 | 1.5rem–1.75rem | 600 | Feature groups, card titles |
| Body | 1rem–1.125rem | 400 | Paragraph copy, product explanation |
| Small | 0.875rem | 400–500 | Captions, labels, helper text |
| CTA | 1rem | 600 | Buttons and main conversion actions |

### Typography Rules

- Keep headlines short and declarative.
- Use emotionally clear lines such as “Your day did not disappear.”
- Avoid dense technical language on the landing page.
- Body copy should explain the product through the user transformation: plan → action → evidence → recap.

---

## 4. Component Patterns

### Buttons

| Type | Style | Usage |
|------|-------|-------|
| **Primary CTA** | Deep Navy background, white text, rounded pill shape, medium shadow | Main actions: “Join the Waitlist,” “Get Early Access” |
| **Secondary CTA** | Transparent or Warm Off-White background, Deep Navy border/text | Secondary actions: “See How It Works,” “View Demo” |
| **Evidence CTA** | Sage Green background, white text, rounded pill shape | Completion/recap actions in product UI |

Button copy should be short and direct. Preferred CTA language:
- Join the Waitlist
- Start Seeing Your Day
- Turn Plans Into Evidence
- Get Early Access

### Cards

- Background: Light Mist or white
- Border: subtle 1px border or soft shadow
- Border radius: 16px–24px
- Padding: generous, usually 20px–32px
- Optional top border in Warm Terracotta, Deep Navy, or Sage Green to show the three product layers

Cards should feel like calm evidence containers, not crowded dashboards.

### Form Inputs

- Border radius: 12px–16px
- Background: white or Warm Off-White
- Border: 1px solid muted gray
- Focus state: Deep Navy border or soft glow
- Placeholder: Muted Gray Blue

### Timeline Blocks

Timeline blocks should communicate time gently and visually.

- Planned time: Deep Navy or Soft Slate Blue
- Actual/focus time: Sage Evidence Green
- Gap/deviation: Warm Terracotta or subtle dashed line
- Completed evidence: slightly stronger fill or check marker

---

## 5. Imagery & Icons

**Icon style:** Simple rounded line icons, preferably Lucide-style.

**Imagery style:** Warm, natural, low-friction screenshots of daily life: desk, calendar, laptop, notes, coffee shop, campus, walking, library. Product screenshots should be the main visual asset.

**What to avoid:**
- Overly polished corporate productivity imagery
- Cold dashboards filled with fake metrics
- Stock photos that feel staged
- Visuals that make the product feel like hustle culture

---

## 6. Copy and Voice

**Voice:** calm, specific, and emotionally honest.

Evidence of Life should sound like a product that understands imperfect days. It should not shame users for not finishing everything.

Preferred phrases:
- “Your day did not disappear.”
- “Turn scattered plans into visible proof.”
- “Unfinished work still counts.”
- “See what actually happened.”
- “A plan becomes action. Action becomes evidence. Evidence becomes recap.”

Avoid:
- “Maximize your productivity”
- “Crush your goals”
- “Become your best self”
- “AI-powered everything”

---

## Implementation Notes

- **CSS framework:** Tailwind CSS
- **Frontend:** React / TypeScript / Vite
- **Deployment:** Vercel
- **Responsive:** mobile-first design; test at 375px width minimum
- **Primary landing page URL:** https://evidenceoflife.vercel.app/

