# Workflow.md — Open Bear Page Writing System
> Load this file when starting any new page. Contains the full 7-step workflow, brand voice rules, and page file structure.

---

## Brand Voice
| Rule | Detail |
|---|---|
| Person | Second person — "your gate", "your property" |
| Tone | Confident, direct, grounded in numbers. Never salesy. |
| Claims | Always backed by a spec number from `CLIENT-DATA-MAP.md`. No unverified claims. |
| Audience | Homeowner or property owner. No trade jargon without inline explanation. |
| Lead with outcomes | "Handles gates up to 1,800 kg" not "features high load capacity" |
| Paragraph length | Max 3 sentences per paragraph |
| Numbers | Embedded naturally in sentences — never floated alone as labels |

> For full NICE copywriting method, buyer psychology, objection handling, and copy frameworks, see `expert-profile.md`.

---

## Page File Structure
Every page `.md` file must include these sections in order:
```
# [Page Title]
## Page Checklist
## SEO — Meta Title / Meta Description / Primary Keyword / Secondary Keywords
## Sections — content sections in order, each labeled with component name from Design.md
## Internal Links — destination / anchor text / location on page
## Notes for Developer — image file names, component variants, instructions
```

---

## Step 0 — Page Brief
Before outline. Before a single word. Read `CLIENT-DATA-MAP.md` + relevant `Keyword Clusters/` file. Present this brief and wait for approval:

```
PAGE BRIEF — [Page Name]
Target consumer: [homeowner / property manager / rural owner]
Primary keyword: [exact phrase from Keyword Clusters/]
Secondary keywords: [list]

Keyword slot assignment:
- H1 / First sentence / Mid-page H2 / Body paragraph / Image alt / CTA / Meta description

Draft meta title: [Primary Keyword] | Open Bear — [X]/60
Draft meta description: [benefit-led, primary keyword first] — [X]/155

Key specs to feature: [3 specs with exact numbers from CLIENT-DATA-MAP.md]

Differentiators this page must include (min 2):
- [ ] DC24V safety voltage — safe to touch, no electric shock risk
- [ ] Servo motor — adjusts to gate weight, no slamming
- [ ] Factory-direct — no reseller markup
- [ ] 50,000 units/year production capacity
- [ ] Temperature range -35°C to 70°C

Objections this page must answer:
- [ ] Electric shock risk  [ ] Gate weight handling  [ ] Climate performance
- [ ] Power cut behaviour  [ ] Noise level  [ ] Phone control
- [ ] Installation difficulty  [ ] Child and pet safety
```
**Wait for approval before Step 1.**

---

## Step 1 — Outline with Keyword Map
Produce the full page outline with keyword slots locked before writing:
```
| # | Section / Component | Purpose | Keyword slot |
```
**Wait for approval. If outline changes, update keyword map and confirm again.**

---

## Step 2 — Write Section by Section
For every section follow this sequence:

**2a** — State the component name (e.g. `[hero-full]`, `[section-features]`)

**2b** — DISPLAYS AS block:
```
Layout: [full-width / two-column / card grid]
Left/Top: [content]
Right/Bottom: [content]
User sees: [one sentence — what a visitor notices first]
```

**2c** — Write section content. Follow NICE proof formula (`expert-profile.md`): outcome headline first (5–8 words) · spec numbers in sentences · benefit-first · active voice · max 20 words per sentence · consumer language.

**2d** — Tier 1 quality checks (all five required before showing user):
1. **Banned phrase scan** — zero matches against full list in `Quality-Check-System.md`
2. **Claims verification** — every number traced to `CLIENT-DATA-MAP.md`. Level 3 specificity required.
3. **Consumer readability** — stranger test · sentences under 25 words · no passive voice · jargon explained inline
4. **Benefit-first** — FAB chain applied. Every feature sentence opens with buyer outcome.
5. **CTA check** (CTA sections only) — substitution test · value exchange test · section alignment test

**2e** — Keyword check:
```
KEYWORD CHECK — [Section name]
Primary keyword slot: [slot / confirmed present / not yet placed]
Secondary keywords present: [list]
Note: [flag if forced]
```

**2f** — Present to user. Show: component name → DISPLAYS AS → content → keyword check. **Wait for approval.**

---

## Step 3 — Consumer Journey Read
Read full compiled page as a homeowner who has never heard of Open Bear. Fix before passes run:
1. **Question order** — What is this? → Weight? → Safety? → Climate? → Control? → Get started?
2. **Flow** — Any disconnected or off-topic sections?
3. **CTA readiness** — Enough information before first CTA?
4. **Missing objections** — All 8 from the brief answered?

No output document — structural fixes only.

---

## Step 4 — Three-Pass System
Run all three passes. Present all three outputs together. Full execution method in `Quality-Check-System.md`.

**Pass A — Quality audit.** Score 6 dimensions by failure count: Clarity · Specificity · Human Voice · Consumer Fit · Benefit-First · Originality. List every failing sentence with fix instruction.

**Pass B — Surgical rewrite.** Fix only Pass A failures. 8 rewriting rules in `Quality-Check-System.md`.

**Pass C — Consumer conversion review.** 6 tests: 3-second headline · first 10 words · objection coverage · CTA journey · differentiation · read-aloud. AI-written score target: 15% or below. Max 2 fix loops.

---

## Step 5 — Differentiation Check
Minimum 2 of 5 differentiators must appear in consumer language:
| Differentiator | Consumer language |
|---|---|
| DC24V safety voltage | Safe to touch — even mid-cycle. No electric shock risk. |
| Servo motor | The motor adjusts to your gate's weight — no slamming, no strain |
| Factory-direct | You are buying from the manufacturer, not a reseller |
| 50,000 units/year | Large enough to supply distributors globally |
| -35°C to 70°C | Works in Canadian winters and Australian summers |

If fewer than 2 present: add one sentence to the most relevant section. Do not create a new section.

---

## Step 6 — Page Checklist
Present completed checklist. Page is only DONE when every box is checked.

### Brief & Planning
- [ ] Brief written and approved · Consumer confirmed · Keyword slot map approved
- [ ] Meta title approved (≤60 chars) · Meta description approved (≤155 chars)
- [ ] Outline written with keyword map · Outline approved

### Content
- [ ] Each section — written, Tier 1 checks passed, keyword checked, approved
- [ ] Consumer journey read complete
- [ ] Full page compiled into Pages/

### SEO
- [ ] Primary keyword: H1 · first sentence · mid-page H2 · body paragraph · image alt · CTA · meta description
- [ ] Meta title final ≤60 chars · Meta description final ≤155 chars
- [ ] Internal links ≥2 · Anchor text uses exact destination keyword · SILO-Structure.md updated

### Quality
- [ ] Pass A complete · Pass B complete · Pass C all 6 tests passed
- [ ] AI-written score ≤15% · Differentiation check — min 2 differentiators

### Final
- [ ] Developer notes added · Page saved to Pages/ · Memory.md updated

---

## What NOT to Do
- Never invent specs. Every number from `CLIENT-DATA-MAP.md` or spec PDFs.
- Never claim certifications unless confirmed. CE cert on Side-Mounted Swing only.
- Never write "We offer..." — second person or third person only.
- Never run three-pass system on individual sections — Tier 1 per section, three passes on full compiled page.
- Never float spec numbers as standalone labels — embed in sentences.
- Never skip Step 3 (consumer journey read) — structural fixes here are cheaper than after passes.
