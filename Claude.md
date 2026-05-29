# Claude.md — Open Bear Project Instructions
> Read this file before doing any work on this project. These rules override all defaults.

---

## 1. Project Overview

**Client:** Open Bear (Shenzhen Black Bear Smart Technology Co., Ltd.)
**Website:** Gate automation products — sliding operators, swing operators, barrier gates
**Audience:** B2B — distributors, agents, installers. NOT end consumers.
**Language:** English only
**Primary Markets:** North America, Australia, Southeast Asia, Eastern Europe

**Source of truth for all product and company data:** `CLIENT-DATA-MAP.md`
**Keyword research:** `Keyword Clusters/` directory

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
├── Claude.md                    ← You are here. Agent rules.
├── Memory.md                    ← Project memory and decisions log
├── Design.md                    ← Design system, component specs, page templates
├── Reusable-Sections.md         ← Reusable copy blocks (nav, footer, CTAs, etc.)
├── CLIENT-DATA-MAP.md           ← Master product and company data
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

## 4. Page Writing Workflow

### Step 1 — Outline First
Before writing a single word of content, present the full page outline to the user:
- List every section in order with its component name, purpose, and a one-line description of what it will say
- Wait for explicit approval before writing anything
- If the user changes the outline, update it and confirm again before proceeding

### Step 2 — Write Section by Section
After the outline is approved, write one section at a time. For each section:

1. **State the component name** — e.g. `[hero-full]`, `[section-features]`
2. **Show how it displays on the page** — describe the visual layout in plain language so the user knows exactly what they will see (see format below)
3. **Write the content** for that section only
4. Wait for the user to approve or request changes before moving to the next section

**Visual display format** — use this at the top of every section you write:

```
DISPLAYS AS:
Layout: [e.g. full-width dark background / two columns / 3-column card grid]
Left side: [what appears left or top]
Right side: [what appears right or bottom]
User sees: [one sentence describing the experience — what a visitor would notice first]
```

### Step 3 — Full Page Compile
After all sections are written and approved one by one, compile the complete page content into the final `.md` file under `Pages/`.

### Step 4 — Run AI Passes (Automatic)
**Do NOT run the Three-Pass system during section writing.**
**Do NOT run the Three-Pass system on individual sections.**

After Step 3 is complete — immediately run all three passes on the complete page content without waiting for user instruction. No approval needed. Present Pass A → Pass B → Pass C output and the final AI-written score.

### Step 5 — Page Checklist
After the AI passes are complete, update the page checklist (see below). Every item must be checked before the page is considered done. Present the checklist to the user so they can see what is cleared and what is still open.

---

## Page Checklist — Template

Every page `.md` file must include this checklist at the top, below the SEO block. Update each item as work progresses. A page is only **DONE** when every box is checked.

```markdown
## Page Checklist

### Planning
- [ ] Outline written
- [ ] Outline approved by user

### Content
- [ ] Section 1 written and approved
- [ ] Section 2 written and approved
- [ ] Section 3 written and approved
- [ ] Section 4 written and approved
- [ ] Section 5 written and approved
- [ ] Section 6 written and approved
- [ ] [add/remove rows to match actual section count]
- [ ] Full page compiled into Pages/

### SEO
- [ ] Primary keyword in H1 (exact match)
- [ ] Primary keyword used 6–7 times on page
- [ ] Meta title written (under 60 chars)
- [ ] Meta description written (under 155 chars)
- [ ] All image alt texts written with keyword context
- [ ] Internal links added (minimum count met — see SILO-Structure.md)
- [ ] All anchor text uses exact destination keyword

### Quality
- [ ] Pass A complete — score logged
- [ ] Pass B rewrite complete
- [ ] Pass C review complete
- [ ] AI-written score at or below 15%

### Final
- [ ] Developer notes added
- [ ] Page saved to Pages/[filename].md
- [ ] SILO-Structure.md internal links updated
- [ ] Memory.md updated with page status

**Page status: [ ] IN PROGRESS → [ ] DONE**
```

Add the actual section names in the Content block once the outline is approved. Replace placeholder rows with the real section names.

---

## 5. Three-Pass Copywriting System

**Run automatically after Step 3 — full page compiled.**
Never run on individual sections mid-page. Never interrupt section writing with passes.

---

### Pass A — Quality Audit

Before writing or after a first draft, run this audit. Rate the content from 1–10 on each dimension:

| Dimension | What to Check |
|---|---|
| **Clarity** | Can a busy B2B buyer understand this in one read? No jargon unless it's their jargon. |
| **Specificity** | Are claims backed by numbers from the spec sheet? No vague words like "high quality", "advanced", "reliable". |
| **Human Voice** | Does it sound like a person wrote it? No AI padding phrases (see list below). |
| **B2B Fit** | Is it written for a distributor/agent/installer — not a homeowner? |
| **Benefit-First** | Does each sentence lead with what the buyer gains, not what the product has? |
| **Originality** | Are sentences structured in ways a human would naturally write them? |

**Pass A output format:**
```
PASS A AUDIT
Clarity: [score]/10 — [one line note]
Specificity: [score]/10 — [one line note]
Human Voice: [score]/10 — [one line note]
B2B Fit: [score]/10 — [one line note]
Benefit-First: [score]/10 — [one line note]
Originality: [score]/10 — [one line note]
Overall: [average]/10
Issues to fix in Pass B: [bulleted list of specific problems]
```

---

### Pass B — Rewrite

Rewrite the content fixing every issue identified in Pass A.

**Rules for Pass B:**

1. **Start sentences differently.** No two sentences in a row should start with the same word.
2. **Cut every filler phrase.** See the banned list below.
3. **Ground every claim in a number.** "Powerful" → "650 Nm — the highest torque in the range." "Durable" → "Rated for 10,000,000+ cycles."
4. **Write at a 9th grade reading level.** Short sentences. Active voice. No passive constructions.
5. **One idea per sentence.** Never combine two ideas with "and" when two separate sentences are stronger.
6. **Use the buyer's language.** They say "gate operator", "torque rating", "load capacity" — use those words exactly.
7. **No manufactured urgency.** Don't write "don't miss out" or "act now". B2B buyers are not impulsive.
8. **Vary sentence length.** Mix short punchy sentences (5–8 words) with medium ones (15–20 words). Never write three long sentences in a row.

**Banned phrases — never use these:**
- "cutting-edge", "state-of-the-art", "world-class", "next-generation"
- "seamlessly", "robust", "leverage", "elevate", "empower"
- "innovative", "revolutionize", "game-changing", "industry-leading"
- "tailor-made", "bespoke", "holistic", "end-to-end solution"
- "In today's world", "In the modern era", "In an ever-changing landscape"
- "Whether you're looking for...", "Look no further"
- "Our team of experts", "Dedicated team", "Passionate professionals"
- "Don't hesitate to contact us"
- "At [Company], we believe..."
- Any sentence that starts with "We are proud to..."

---

### Pass C — Marketing Expert Review

After Pass B, apply this final check as a senior B2B marketing strategist would:

1. **Does the headline earn attention?** A distributor skimming a trade page — would they stop here?
2. **Is the value proposition clear in the first 10 words of every section?** If not, restructure.
3. **Does the copy speak to pain points?** Buyers have real problems: unreliable suppliers, warranty failures, wrong specs. Address these directly.
4. **Is there a clear next action?** Every section should point toward quote request, spec download, or contact.
5. **Does it differentiate from competitors?** NICE, Blutezeit, Joytech are the competition. What makes Open Bear different must be explicit — DC24V safety voltage, servo motor technology, 50,000 unit/year capacity.
6. **Would this pass a native English speaker's eye?** Read every sentence aloud. If it sounds robotic, rewrite it.

**Pass C output format:**
```
PASS C REVIEW
Headline strength: [pass/fail] — [note]
Value prop clarity: [pass/fail] — [note]
Pain point coverage: [pass/fail] — [note]
CTA presence: [pass/fail] — [note]
Differentiation: [pass/fail] — [note]
Native English check: [pass/fail] — [note]
Final changes made: [list]
AI-Written Score: [X]% — [brief justification]
```

**AI-Written Score target: 15% or below.** If above 15%, return to Pass B and rewrite further.

---

## 5. Brand Voice Rules

| Rule | Detail |
|---|---|
| **Person** | Second person — "your gate", "your facility", "your installation" |
| **Tone** | Confident, technical, direct. Never salesy. |
| **Claims** | Always backed by a spec number. No unverified claims. |
| **Avoid** | Consumer language. This is B2B. No "perfect for your home." |
| **Lead with outcomes** | Not features. "Handles 1,800 kg" not "features high load capacity." |
| **Length** | Short paragraphs. Max 3 sentences per paragraph. |

> For the full NICE copywriting method, buyer psychology breakdown, objection handling copy, and copy frameworks (PAS, FAB, AIDA, StoryBrand), see `expert-profile.md`.

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

## SEO
- **Meta Title:** [under 60 chars]
- **Meta Description:** [under 155 chars]
- **Primary Keyword:** [exact phrase]
- **Secondary Keywords:** [list]

## Sections
[Content sections in order, each labeled with a component name from Design.md]

## Internal Links
[list of pages this page links to]

## Notes for Developer
[any specific instructions — image file names, component variants, etc.]
```

---

## 8. Agent Workflow

When an agent starts a new page:

1. Read `CLIENT-DATA-MAP.md` for all product and company data
2. Read `Keyword Clusters/` for the relevant keyword file
3. Read `Design.md` for the page template to follow
4. Read `Reusable-Sections.md` to pull in existing copy blocks (do not rewrite what's already written)
5. Write the page content following the file structure above
6. Run the Three-Pass Copywriting System on all new copy
7. Save to `Pages/[page-name].md`
8. Update `Memory.md` with what was written and any decisions made

---

## 9. What NOT to Do

- Do not invent product specs. Every number must come from `CLIENT-DATA-MAP.md` or the spec PDFs.
- Do not make claims about certifications unless they are confirmed in the client data (Side-Mounted Swing is CE certified — others are not confirmed).
- Do not write in first person plural ("We offer..."). Write in second person or third person.
- Do not create new files outside the `Pages/` directory without a clear reason.
- Do not rewrite content that has already passed all three passes — improve by adding, not replacing.
