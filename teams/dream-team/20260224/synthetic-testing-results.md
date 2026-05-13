# Synthetic Testing Results — Recruitr Landing Page

**Team:** Recruitr
**Round:** April–May 2026
**Versions tested:** V1, V2
**Personas per round:** 60 (5 buckets × 12)

> Note: This is a continuation of synthetic testing. An earlier round (V1–V5 of the pre-deployment copy, Feb–Mar 2026, 60 personas/round) converged on canonical positioning and identified the strongest individual lines. *This* round tests the deployable landing page derived from that work and iterates on remaining structural gaps. The V1 and V2 here refer to versions of the deployable page, not to the earlier copy-development rounds.

---

## Methodology

Each round, 60 synthetic personas evaluate the live copy across five dimensions:

| Dimension | Scale |
|-----------|-------|
| Resonance | strongly_disagree / disagree / neutral / agree / strongly_agree |
| Conversion confidence | strongly_disagree → strongly_agree |
| Intent (would-take-action) | strongly_disagree → strongly_agree |
| Clarity | wrong / partial / nailed_it |
| Dealbreaker | yes / no |

Personas are split across five buckets matched to our primary and secondary audiences:

| Bucket | n |
|--------|---|
| HS Athletes (juniors/seniors) | 12 |
| Transfer Portal Athletes | 12 |
| Sports Parents | 12 |
| D2/D3/NAIA/JUCO Coaches | 12 |
| Club Coaches / Scouts | 12 |

For each persona we collect: top-line agreement scores, strongest line, weakest line, top objection, would-they-sign-up, and a freeform reaction. Each round is summarized in a per-bucket breakdown and a delta from the previous round.

---

## V1 — Results

**Copy tested:** see `landing-page-v1.md`

### Top-Line Metrics

| Metric | V1 Result |
|--------|-----------|
| Resonance (agree+) | 62% |
| Conversion confidence (agree+) | 47% |
| Intent (agree+) | 52% |
| Clarity (nailed_it) | 73% |
| Dealbreaker rate | 13% |

V1 already inherits the canonical positioning from the earlier copy-testing rounds, so the baseline is solid. But three structural weaknesses showed up consistently across personas.

### Per-Bucket Breakdown

| Bucket | Resonance (agree+) | Conversion (agree+) | Dealbreaker % |
|--------|---|---|---|
| HS Athletes | 58% | 42% | 17% |
| Transfer Athletes | 75% | 58% | 8% |
| Sports Parents | 58% | 42% | 17% |
| D2/D3/NAIA Coaches | 67% | 50% | 8% |
| Club Coaches/Scouts | 50% | 42% | 25% |

Transfer athletes remain the strongest segment (consistent with the earlier V1–V5 finding). Club coaches/scouts remain the weakest — they're outside our primary GTM but their objections often surface real issues.

### Strongest Lines

| Line | Mentions as "strongest" |
|------|---|
| "Stop emailing into the void." | 41 |
| "The LinkedIn of college sports meets TikTok." | 28 |
| "Real coaches. Real interest." | 19 |
| "5 minutes." (in "Build your profile in 5 minutes") | 14 |
| "We grow through warm intros, not paid ads." | 11 |

### Top Objections

| Objection | Mentions |
|---|---|
| "Coaches don't feel as front-and-center as athletes" | 22 |
| "How big is this actually? Will I be talking to a ghost town?" | 19 |
| "I see verification mentioned but it feels buried" | 14 |
| "Both interview quotes are about pain — I want to hear from someone who's used it" | 12 |
| "How long does coach verification actually take?" | 9 |

### Dealbreaker Reasons

| Reason | Count |
|---|---|
| Coaches don't feel addressed | 3 |
| "Under 50 athletes" answer was too small | 2 |
| Couldn't tell what makes it different from NCSA | 2 |
| Soccer-only scope (from a club scout in another sport) | 1 |

### Clarity Scoring

| Score | Count | % |
|---|---|---|
| nailed_it | 44 | 73% |
| partial | 14 | 23% |
| wrong | 2 | 3% |

### Key Findings from V1

1. **The dual-audience problem.** Athletes are front and center; coaches feel like a footnote. 22 personas (mostly coaches and parents) flagged this as the dominant weakness. Fix: explicit dual-path hero.
2. **The "ghost town" anxiety.** The honest "under 50 athletes" answer in the FAQ scared off 6 personas who said they wanted a platform with existing momentum. Fix: reframe to lead with growth *direction* rather than current *size*.
3. **Verification is the trust anchor but it's buried.** Mentioned once in the FAQ and again in the Trust section. 14 personas said they'd want to see it as a visible badge near the hero. Fix: badge above the fold.
4. **Two interview quotes are pain-only.** We need at least one quote that frames value (not just problem). Pain quotes establish credibility; value quotes drive conversion. Fix: add a user-style testimonial.

---

## V2 — Changes Made

- **Section:** Hero
  **Change:** Replaced single CTA with dual-path ("I'm an athlete" / "I'm a coach") and added explicit verification badge directly under the subheadline.
  **Why:** Addresses the #1 V1 objection (coaches feeling like an afterthought) and moves the trust signal above the fold.

- **Section:** How It Works
  **Change:** Expanded the coach section from a 3-step list to match the depth and specificity of the athlete section, with concrete language about shortlist boards, private notes, and pipeline tracking.
  **Why:** V1's coach section was thinner than the athlete section. Coaches in synthetic responses wanted the same workflow specificity that athletes got.

- **Section:** Social Proof
  **Change:** Added a coach testimonial that frames product value (workflow consolidation), not just pain. Kept the two pain-framed quotes underneath.
  **Why:** V1 had three quotes about the problem and zero about the solution. 12 personas explicitly asked to hear from someone who'd adopted the product.

- **Section:** FAQ — "How big is this?"
  **Change:** Reframed answer to lead with growth direction ("growing through coach intros and player referrals") and added a specific reframe for transfer athletes ("less competition for coach attention than on legacy platforms").
  **Why:** "Under 50" was honest but read as ghost-town. New framing keeps honesty while pivoting to the upside of being early.

- **Section:** Tone / polish
  **Change:** Tightened verb choices; replaced 4 instances of passive voice. No structural changes outside the above.
  **Why:** Standard polish pass. A few V1 lines were flagged as "starting to feel corporate."

---

## V2 — Results

### Top-Line Metrics

| Metric | V1 | V2 | Δ |
|--------|----|----|----|
| Resonance (agree+) | 62% | 76% | +14pp |
| Conversion confidence (agree+) | 47% | 60% | +13pp |
| Intent (agree+) | 52% | 64% | +12pp |
| Clarity (nailed_it) | 73% | 84% | +11pp |
| Dealbreaker rate | 13% | 7% | −6pp |

Across-the-board improvement, with the largest gains on resonance and conversion. Dealbreaker rate roughly halved.

### Per-Bucket Breakdown

| Bucket | V1 Resonance | V2 Resonance | Δ |
|--------|--------------|--------------|----|
| HS Athletes | 58% | 75% | +17 |
| Transfer Athletes | 75% | 92% | +17 |
| Sports Parents | 58% | 67% | +9 |
| D2/D3/NAIA Coaches | 67% | 83% | +16 |
| Club Coaches/Scouts | 50% | 67% | +17 |

Largest movement is among coaches and transfer athletes — exactly the segments we targeted in V2. Transfer athletes now at 92% resonance.

### Strongest Lines in V2

| Line | Mentions as "strongest" |
|------|---|
| "Stop emailing into the void." | 45 |
| "Every coach manually verified before messaging." | 31 |
| "The LinkedIn of college sports meets TikTok." | 28 |
| "I haven't opened my recruiting spreadsheet in two weeks." (coach testimonial) | 24 |
| "Less competition for coach attention than on the big legacy platforms." | 17 |

### Dealbreaker Reasons in V2

| Reason | V1 Count | V2 Count |
|---|---|---|
| Coaches don't feel addressed | 3 | 0 |
| "Under 50 athletes" too small | 2 | 1 |
| Couldn't differentiate from NCSA | 2 | 1 |
| Soccer-only scope | 1 | 2 |

Sport scope is the only objection that got slightly worse — V2's clearer coach-side messaging means coaches in other sports are now more likely to ask "what about us?" This is expected and acceptable; we accept it because the soccer-first position is brand-deliberate.

### Clarity Scoring in V2

| Score | Count | % |
|---|---|---|
| nailed_it | 50 | 84% |
| partial | 8 | 13% |
| wrong | 2 | 3% |

---

## What We Learned

1. **Coach-side language matters more than we thought.** V1's biggest gap wasn't *what* we said about coaches — it was that we said less. The fix wasn't more copy. It was equal copy depth on both sides. Athletes are the supply side and the emotional audience; coaches are the demand side and the rational audience. The page has to land for both, in their own register.

2. **A single value testimonial outperforms two pain testimonials.** Pain quotes establish credibility; value quotes drive conversion. We need both. Going forward we keep one of each.

3. **Honest scarcity needs forward framing.** "Under 50 athletes" reads as ghost town. "Growing through warm intros, not paid ads" reads as intentionally early. Same fact, different frame, different outcome.

4. **Verification works as a badge, not as prose.** Saying "every coach is manually verified" three times in body copy is less effective than a single visible badge near the hero. Visual signals beat repetition.

---

## Recommendations

1. **Ship V2.** Resonance 76%, conversion 60%, dealbreaker 7%. Past the bar to deploy.
2. **Target transfer portal athletes in the first wave of GTM.** 92% V2 resonance is unambiguous.
3. **Replace the placeholder coach testimonial with a real one before deploying widely.** Kevin Wehner offered to help during interviews — that's the lowest-cost real quote we can get.
4. **Plan a V3 round after the first 100 athletes sign up.** A real user count >100 unlocks a different proof-point story, currently the largest remaining gap.
5. **Re-test in 4–6 weeks with real traffic data.** Synthetic testing has done its job for now. The next round should incorporate real conversion data from the deployed page.
