# Claude.md — Open Bear Project Instructions
> Read this file before doing any work on this project. These rules override all defaults.

---

## 1. Project Overview

**Client:** Open Bear (Shenzhen Black Bear Smart Technology Co., Ltd.)
**Website:** Gate automation products — sliding operators, swing operators, barrier gates
**Audience:** End consumers — homeowners, property managers, and facility owners buying or researching gate automation for their own property.
**Language:** English only
**Primary Markets:** North America, Australia, Southeast Asia, Eastern Europe

**Source of truth for all product and company data:** `CLIENT-DATA-MAP.md`
**Keyword research:** `Keyword Clusters/` directory
**Quality check methods:** `Quality-Check-System.md`

---

## 2. Content-Only Rule

**We write content in Markdown (.md) files only.**

- Do NOT write HTML, CSS, JavaScript, or any visual code
- Do NOT create `.html` files
- Each page gets one `.md` file with structured content sections
- Design decisions and component templates live in `Design.md`
- Reusable copy blocks live in `Reusable-Sections.md`

The developer handles converting content to templates. We handle words.

---

## 3. File Structure

```
OpnerBear1/
├── CLAUDE.md                    ← You are here. Agent rules.
├── Memory.md                    ← Project memory and decisions log
├── Design.md                    ← Design system, component specs, page templates
├── Reusable-Sections.md         ← Reusable copy blocks (nav, footer, CTAs, etc.)
├── CLIENT-DATA-MAP.md           ← Master product and company data
├── Quality-Check-System.md      ← How every quality check is executed (read before checking)
├── Pages/
│   ├── home.md                  ← Homepage content
│   ├── products-archive.md      ← Products archive page content
│   ├── product-sliding-door-operator.md
│   ├── product-heavy-duty-swing.md
│   ├── product-side-mounted-swing.md
│   ├── product-floor-swing.md
│   ├── product-top-mounted-swing.md
│   ├── product-barrier-gate.md
│   ├── solutions-residential.md
│   ├── solutions-commercial.md
│   ├── solutions-industrial.md
│   └── about.md
├── Keyword Clusters/            ← SEO keyword research
├── Data From Client/            ← Raw client data
├── product specification/       ← Product spec PDFs/docs
├── Manual of products/          ← Product manuals (PDFs)
├── Products info/               ← Product images by category
├── product-loop.md              ← Spec card data for product archive cards (developer reference)
└── expert-profile.md            ← NICE copywriting methodology, buyer psychology, objection handling
```

When creating a new page, create a new file under `Pages/`. Never write page content directly into `CLIENT-DATA-MAP.md`.

---

## 4. Page Writing Workflow — 7 Steps

> For exact execution methods on every quality check, read `Quality-Check-System.md` before running any check.

---

### Step 0 — Page Brief

Before the outline. Before a single word of content.

Read `CLIENT-DATA-MAP.md` and the relevant file in `Keyword Clusters/`. Then produce this brief and present it to the user for approval:

```
PAGE BRIEF — [Page Name]

Target consumer: [homeowner / property manager / rural owner — pick one primary]
Primary keyword: [exact phrase from Keyword Clusters/]
Secondary keywords: [list from relevant Keyword Clusters/ file]

Keyword slot assignment:
- H1: [primary keyword]
- First sentence of opening paragraph: [primary keyword]
- Mid-page H2: [primary keyword or close secondary]
- Body paragraph: [primary keyword — different section from H2]
- Image alt text: [primary keyword in context]
- CTA section: [primary keyword]
- Meta description: [primary keyword in first 10 words]

Secondary keywords placed in:
- [section name]: [keyword]
- [section name]: [keyword]

Draft meta title: [Primary Keyword] | Open Bear — [character count]/60
Draft meta description: [benefit-led sentence, primary keyword first] — [character count]/155

Key specs to feature (from CLIENT-DATA-MAP.md):
- [spec 1 with exact number]
- [spec 2 with exact number]
- [spec 3 with exact number]

Differentiators this page must include (minimum 2):
- [ ] DC24V safety voltage — safe to touch, no electric shock risk
- [ ] Servo motor technology — adjusts to gate weight, no slamming
- [ ] Factory-direct from manufacturer — no reseller markup
- [ ] 50,000 units/year production capacity
- [ ] Temperature range -35°C to 70°C

Objections this page must answer:
- [ ] Will someone get an electric shock?
- [ ] Will it handle my gate's weight?
- [ ] Will it work in my climate?
- [ ] What happens if the power cuts out?
- [ ] Is it too loud?
- [ ] Can I control it from my phone?
- [ ] Is it hard to install?
- [ ] Is it safe around children and pets?
```

**Wait for user approval before proceeding to Step 1.**

---

### Step 1 — Outline with Keyword Map

After the brief is approved, produce the full page outline. List every section in order with three columns:

```
| # | Section / Component | Purpose | Keyword slot |
|---|---|---|---|
| 1 | [hero-full] | [what it says in one line] | Primary keyword — H1 + first sentence |
| 2 | [section-trust-bar] | [what it says in one line] | None |
| 3 | [section-features] | [what it says in one line] | Secondary keyword: [keyword] |
| 4 | [section-specs] | [what it says in one line] | Primary keyword — body paragraph |
```

The keyword slot column locks where every keyword lands before writing begins. No surprises during writing.

**Wait for user approval. If the outline changes, update the keyword map and confirm again before proceeding.**

---

### Step 2 — Write Section by Section

After the outline is approved, write one section at a time. Follow this exact sequence for every section:

**2a — State the component name**
e.g. `[hero-full]`, `[section-features]`, `[section-specs-table]`

**2b — Show how it displays on the page**

```
DISPLAYS AS:
Layout: [e.g. full-width dark background / two columns / 3-column card grid]
Left side: [what appears left or top]
Right side: [what appears right or bottom]
User sees: [one sentence — what a visitor notices first]
```

**2c — Write the section content**

Follow the NICE proof formula (see `expert-profile.md`):
- Outcome headline first — 5–8 words, states what the buyer gains
- Spec numbers embedded naturally inside sentences — not floated as separate labels
- Benefit-first — buyer outcome before product feature in every sentence
- Active voice — max 20 words per sentence
- Consumer language — no unexplained technical terms

**2d — Run Tier 1 quality checks** (before showing the user — all five required)

**Check 1 — Banned phrase scan**
Search the section word by word against the full banned list in `Quality-Check-System.md`. Zero matches required. Any match = rewrite before proceeding. Never adjust a banned phrase — remove or rewrite the sentence entirely.

**Check 2 — Claims verification**
Trace every number and performance claim to `CLIENT-DATA-MAP.md` or spec PDFs. Every claim must reach Level 3 on the specificity ladder (number present). Remove any claim that cannot be sourced. Do not estimate or approximate numbers.

**Check 3 — Consumer readability**
Four sub-tests — all must pass:
- Stranger test: no unexplained technical terms
- Sentence length: nothing over 25 words
- Passive voice: zero passive constructions
- Jargon ratio: every technical term explained inline in the same sentence

**Check 4 — Benefit-first**
Apply FAB chain (Feature → Advantage → Benefit) to every sentence describing a product feature. Use the "So what?" method. Every sentence must open with what the buyer gains, not what the product has. See `Quality-Check-System.md` for full method.

**Check 5 — CTA check** (only for sections that contain a CTA)
Three-part test:
- Substitution test: cannot be replaced by "click here"
- Value exchange test: states exactly what the reader gets when they click
- Section alignment test: CTA matches the section topic

**2e — Run keyword check**

Confirm which keyword slot this section fills from the outline map. Verify the keyword appears naturally in the assigned slot. Note any secondary keywords present.

```
KEYWORD CHECK — [Section name]
Primary keyword slot: [which slot / confirmed present / not yet placed]
Secondary keywords present: [list any that appear]
Note: [flag if any keyword feels forced — rewrite or flag to user]
```

**2f — Present to user for approval**
Show: component name → DISPLAYS AS block → written content → keyword check result.
**Wait for approval before moving to the next section.**

---

### Step 3 — Consumer Journey Read

After all sections are written and approved. Before any AI pass.

Read the full compiled page end-to-end as a homeowner who has never heard of Open Bear. Check four things:

**1. Question order** — Does the page answer buyer questions in the natural sequence?
The natural sequence for a gate opener buyer:
- What is this? → Does it handle my gate? → Is it safe? → Will it work in my climate? → Can I control it easily? → How do I get started?

If the page answers these out of order, restructure the sections before running passes.

**2. Flow** — Is there any section that feels disconnected, too long, or off-topic? Fix the transition or trim the section before proceeding.

**3. CTA readiness** — By the time the reader reaches the first CTA, have they received enough information to act on it? If not, move the CTA to after the key objection answer.

**4. Missing objections** — Cross-check the full page against the 8 objections listed in the brief. Every objection must be answered somewhere. If any is missing, add the answer to the most relevant existing section before proceeding.

This step produces no document output — only structural fixes to the compiled page. Fix everything here before the passes run.

---

### Step 4 — Three-Pass System

Run immediately after Step 3. No user approval needed between passes. Present all three pass outputs together after all three complete.

> Full execution method for every pass — including scoring method, rewriting rules, and AI score signals — lives in `Quality-Check-System.md`. Read it before running any pass.

**Pass A — Full-page quality audit**

Read the full page once. Mark every sentence that fails any of the five Tier 1 checks. Score six dimensions using the failure count method — not impression.

Six dimensions: Clarity · Specificity · Human Voice · Consumer Fit · Benefit-First · Originality

Failure count to score: 0 = 10/10 · 1 = 9/10 · 2–3 = 7–8/10 · 4–6 = 5–6/10 · 7–10 = 3–4/10 · 11+ = 1–2/10

Output:
```
PASS A AUDIT — [Page Name]
Clarity: [X]/10 — [main failure type]
Specificity: [X]/10 — [main failure type]
Human Voice: [X]/10 — [main failure type]
Consumer Fit: [X]/10 — [main failure type]
Benefit-First: [X]/10 — [main failure type]
Originality: [X]/10 — [main failure type]
Overall: [average]/10

Failure list:
- [Section]: [exact sentence] — [which check failed] — [fix instruction]
```

Every failure list item must include the exact sentence, the check it failed, and what direction the fix should take.

**Pass B — Surgical rewrite**

Fix every item on the Pass A failure list. Only those items. Do not rewrite sentences that passed.

Eight rewriting rules (full detail in `Quality-Check-System.md`):
1. No two consecutive sentences start with the same word
2. Every vague claim gets a verified number from `CLIENT-DATA-MAP.md`
3. No sentence over 25 words — split into two
4. Every passive construction rewritten active
5. One idea per sentence — split "and" constructions when two sentences are stronger
6. Vary sentence rhythm — short punch (5–10 words) mixed with medium explanation (11–20 words)
7. Use the buyer's exact words — "gate opener" not "access automation system"
8. No urgency language — buyers research over days, not minutes

Output:
```
PASS B COMPLETE — [Page Name]
Items fixed: [count]
Sections touched: [list]
Items needing client data to resolve: [list, if any]
```

If any failure could not be fixed because required spec data does not exist in `CLIENT-DATA-MAP.md` — flag it. Remove the claim. Note what data is needed from the client.

**Pass C — Consumer conversion review**

Six tests run on the rewritten page:

1. **3-second headline test** — Read only each section headline for 3 seconds. Does it make a promise or state an outcome a homeowner wants? Failing headlines must be rewritten as outcome statements of 5–8 words.

2. **First 10 words test** — Do the first 10 words of each section's body copy state what the buyer gains? If the first 10 words introduce the product, the company, or a feature — they fail.

3. **Objection coverage test** — Cross-check all 8 buyer objections from the brief against the page. Every one must be answered with a specific, number-backed response.

4. **CTA journey test** — Map every CTA. Each must advance the reader one step closer to contact. No two CTAs should send to the same destination.

5. **Differentiation test** — At least 2 of the 5 Open Bear differentiators must be explicitly stated in consumer language (see brief). If fewer than 2 are present, add to the most relevant section.

6. **Read-aloud test** — Read the full page aloud. Mark every sentence that hesitates, requires a second read, or sounds assembled rather than spoken. Rewrite every marked sentence.

**AI-Written Score — target 15% or below.**

Assess using the signal method in `Quality-Check-System.md`. If above 15%: identify the top 3 AI-signal sentences, rewrite them, reassess. Maximum 2 loops. If still above 15% after 2 loops, flag to user with the specific remaining sentences.

Output:
```
PASS C REVIEW — [Page Name]
3-second headline test: [pass/fail] — [note]
First 10 words test: [pass/fail] — [note]
Objection coverage test: [pass/fail] — [uncovered objections if any]
CTA journey test: [pass/fail] — [note]
Differentiation test: [pass/fail] — [differentiators present / missing]
Read-aloud test: [pass/fail] — [flagged sentences if any]

Final changes made:
- [exact change and location]

AI-Written Score: [X]% — [sentences driving score if above 15%]

Page status: READY FOR CHECKLIST / NEEDS FURTHER WORK
```

---

### Step 5 — Differentiation Check

After Pass C. Before the checklist.

One explicit question: **Does this page make it clear — in plain language a homeowner understands — why Open Bear is the better choice over a competitor they may also be looking at?**

Check the page for these five differentiators. Minimum two must appear, stated explicitly in consumer language:

| Differentiator | Consumer language version |
|---|---|
| DC24V safety voltage | Safe to touch — even mid-cycle. No electric shock risk. |
| Servo motor technology | The motor adjusts to your gate's weight — no slamming, no strain |
| Factory-direct | You are buying from the manufacturer, not a reseller |
| 50,000 units/year capacity | Large enough to supply distributors globally — not a small operation |
| -35°C to 70°C range | Works in Canadian winters and Australian summers without modification |

If fewer than two are present: identify which section best absorbs the missing differentiator and add one sentence. Do not create a new section for this.

---

### Step 6 — Page Checklist

After Step 5. Present the completed checklist to the user with every item marked. A page is only **DONE** when every box is checked.

```markdown
## Page Checklist — [Page Name]

### Brief & Planning
- [ ] Page brief written and approved
- [ ] Target consumer persona confirmed
- [ ] Keyword slot map approved
- [ ] Draft meta title approved (under 60 chars)
- [ ] Draft meta description approved (under 155 chars)
- [ ] Outline written with keyword map
- [ ] Outline approved by user

### Content
- [ ] [Section 1 name] — written, Tier 1 checks passed, keyword checked, approved
- [ ] [Section 2 name] — written, Tier 1 checks passed, keyword checked, approved
- [ ] [Section 3 name] — written, Tier 1 checks passed, keyword checked, approved
- [ ] [Section 4 name] — written, Tier 1 checks passed, keyword checked, approved
- [ ] [Section 5 name] — written, Tier 1 checks passed, keyword checked, approved
- [ ] [Section 6 name] — written, Tier 1 checks passed, keyword checked, approved
- [ ] [add/remove rows to match actual section count]
- [ ] Consumer journey read complete — question order, flow, CTA readiness, objections confirmed
- [ ] Full page compiled into Pages/

### SEO
- [ ] Primary keyword in H1 (exact match)
- [ ] Primary keyword in first sentence of opening paragraph
- [ ] Primary keyword in one mid-page H2
- [ ] Primary keyword in one body paragraph (different section from H2)
- [ ] Primary keyword in at least one image alt text
- [ ] Primary keyword in CTA section body copy
- [ ] Primary keyword in meta description (first 10 words)
- [ ] Secondary keywords placed naturally — confirmed in section keyword checks
- [ ] Meta title final — under 60 chars — format: [Primary Keyword] | Open Bear
- [ ] Meta description final — under 155 chars
- [ ] Internal links added — minimum 2
- [ ] All anchor text uses exact destination keyword — no "click here" or "learn more"
- [ ] SILO-Structure.md updated with this page's links

### Quality
- [ ] Pass A complete — overall score logged
- [ ] Pass B complete — all failures fixed — client data gaps flagged if any
- [ ] Pass C complete — all 6 tests passed
- [ ] AI-written score at or below 15%
- [ ] Differentiation check complete — minimum 2 differentiators present

### Final
- [ ] Developer notes added
- [ ] Page saved to Pages/[filename].md
- [ ] Memory.md updated with page status and any decisions made

**Page status: IN PROGRESS → DONE**
```

Replace placeholder section names with the real section names from the approved outline.

---

## 5. Brand Voice Rules

| Rule | Detail |
|---|---|
| **Person** | Second person — "your gate", "your property", "your installation" |
| **Tone** | Confident, direct, grounded in numbers. Never salesy. |
| **Claims** | Always backed by a spec number from `CLIENT-DATA-MAP.md`. No unverified claims. |
| **Audience** | Speak to a homeowner or property owner. No trade jargon without inline explanation. |
| **Lead with outcomes** | "Handles gates up to 1,800 kg" not "features high load capacity" |
| **Paragraph length** | Max 3 sentences per paragraph |
| **Numbers** | Embedded naturally in sentences — never floated alone as labels |

> For the full NICE copywriting method, buyer psychology, objection handling, and copy frameworks (PAS, FAB, AIDA, StoryBrand), see `expert-profile.md`.

---

## 6. SEO Rules

### Keyword Placement
- H1 must contain the **exact-match primary keyword** — no variations, no creative rewording
- Primary keyword appears **6–7 times per page** across these specific slots:
  1. H1 (exact match)
  2. First sentence of the opening paragraph
  3. One H2 or subheading (mid-page)
  4. One body paragraph (not the same section as #3)
  5. At least one image alt text
  6. CTA section body copy
  7. Meta description (does not count as on-page but still required)
- Never use the primary keyword twice in the same paragraph
- Never force it into a sentence where it reads unnaturally — rewrite the sentence instead
- Use exact-match keyword phrases from `Keyword Clusters/` — do not paraphrase keywords
- Secondary keywords fill the remaining body naturally — no target count, just relevance

### Meta Tags
- Every page needs a unique meta title (under 60 characters) and meta description (under 155 characters)
- Meta titles follow format: `[Primary Keyword] | Open Bear`
- Meta description must include the primary keyword in the first 10 words

### Internal Links
- Every page links to at least 2 other pages
- Anchor text on internal links must use the **exact target keyword** of the destination page — never "click here" or "learn more"
- Follow the SILO structure in `SILO-Structure.md` — only link within the correct tier paths

### SILO Structure
The full site is built as a keyword silo. See `SILO-Structure.md` for the complete map.

**Core rule:** Pages only link to their parent tier or their direct children. No cross-silo links.
- Tier 3 (product pages) → links UP to Tier 2 (/products) and Tier 1 (Homepage)
- Tier 2 (category pages) → links UP to Tier 1 and DOWN to its Tier 3 children
- Tier 1 (Homepage) → links DOWN to all Tier 2 pages
- Blog posts → link UP to Tier 1 or Tier 2 only

**URL structure: flat keyword slugs at root level — no nested directories (except /blog/)**

| Page | URL | Keyword |
|---|---|---|
| Homepage | `/` | automatic gate opener |
| Products Archive | `/gate-operators` | gate operators |
| Commercial | `/commercial-gate-operator` | commercial gate operator |
| Residential | `/residential-gate-opener` | residential gate opener |
| Industrial | `/industrial-gate-operator` | industrial gate operator |
| Sliding | `/sliding-gate-operator` | sliding gate operator |
| Heavy-Duty Swing | `/heavy-duty-swing-gate-operator` | heavy duty swing gate operator |
| Side-Mounted | `/side-mounted-swing-door-operator` | side mounted swing door operator |
| Floor Swing | `/floor-swing-door-operator` | floor swing door operator |
| Top-Mounted | `/top-mounted-swing-door-operator` | top mounted swing door operator |
| Barrier Gate | `/barrier-gate-operator` | barrier gate operator |

---

## 7. Page Content Structure

Every page `.md` file must include these sections in order:

```markdown
# [Page Title]

## Page Checklist
[Insert completed checklist from Step 6]

## SEO
- **Meta Title:** [under 60 chars]
- **Meta Description:** [under 155 chars]
- **Primary Keyword:** [exact phrase]
- **Secondary Keywords:** [list]

## Sections
[Content sections in order, each labeled with component name from Design.md]

## Internal Links
[list of pages this page links to, with anchor text]

## Notes for Developer
[image file names, component variants, any specific instructions]
```

---

## 8. Agent Workflow

When an agent starts a new page, follow these steps in order:

1. Read `CLIENT-DATA-MAP.md` — all product and company data
2. Read the relevant file in `Keyword Clusters/` — primary and secondary keywords
3. Read `Design.md` — page template and component names
4. Read `Reusable-Sections.md` — pull existing copy blocks, do not rewrite them
5. Read `Quality-Check-System.md` — understand how every quality check is executed before writing
6. Follow the 7-step Page Writing Workflow (Section 4 above)
7. Save completed page to `Pages/[page-name].md`
8. Update `Memory.md` with page status and any decisions made

---

## 9. What NOT to Do

- Do not invent product specs. Every number must come from `CLIENT-DATA-MAP.md` or the spec PDFs.
- Do not claim certifications unless confirmed in client data. Only the Side-Mounted Swing has confirmed CE certification.
- Do not write in first person plural ("We offer..."). Write in second person or third person.
- Do not create new files outside the `Pages/` directory without a clear reason.
- Do not rewrite content that has already passed all three passes — improve by adding, not replacing.
- Do not run quality passes on individual sections mid-writing — Tier 1 checks run per section, the three-pass system runs on the full compiled page only.
- Do not float spec numbers as standalone labels — embed them naturally inside sentences.
- Do not skip the consumer journey read (Step 3) — structural problems found here are cheaper to fix than after the passes run.
