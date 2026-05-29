# Last Session — Open Bear Project
> Overwrite this file at the end of every working session.
> It always reflects the most recent session only.
> For full history, see `Memory.md`.

---

## Session Info

- **Date:** 2026-05-28
- **Project:** OpnerBear1 — Open Bear gate automation website
- **Session type:** Project setup + content architecture

---

## What We Discussed

### 1. Product Archive Page (Visual Prototype)
We built a full HTML visual prototype of the product archive page to align on layout and design direction. The prototype showed:
- Announcement bar (red) → sticky nav → dark hero section
- Left filter sidebar + 3-column product grid
- "How a Gate Motor System Works" educational section (2-column, steps + factory photo)
- "5 Mistakes When Specifying a Gate Operator" section (2-column, mistakes list + photo)
- Full product comparison table on dark background
- CTA section + footer

**Decision made:** The HTML prototype was exploratory only. Going forward all content lives in `.md` files under `Pages/`. No HTML files will be created — the developer converts content to templates.

---

### 2. Project File Structure — Built from Scratch

We established the full file and workflow system for the project:

| File | What It Does |
|---|---|
| `Claude.md` | Rules for every AI agent working on this project |
| `Memory.md` | Running log of decisions and current project state |
| `Design.md` | Design system — colors, typography, components, page templates |
| `Reusable-Sections.md` | Copy blocks that are reused across pages (nav, footer, CTAs, etc.) |
| `Pages/` directory | One `.md` file per page — content only, structured by component |
| `Last-Session.md` | This file — single-session snapshot, overwrites each time |

---

### 3. Three-Pass Copywriting System

We established a mandatory 3-pass system to prevent AI-sounding copy from going live:

- **Pass A** — Quality audit. Scores content 1–10 across 6 dimensions: Clarity, Specificity, Human Voice, B2B Fit, Benefit-First, Originality.
- **Pass B** — Full rewrite using 8 writing rules and a banned phrases list. No AI padding. Every claim backed by a number from the spec sheet.
- **Pass C** — Marketing expert review. 6 checks. Ends with an AI-written score (%). Target: 15% or below.

**Why this matters:** The client's audience is B2B — distributors, agents, installers. They will instantly dismiss content that reads like a template. Human voice is non-negotiable.

---

### 4. Design System Decisions

- **Brand Red:** `#C0392B` — all CTAs, eyebrows, active states
- **Background dark:** `#1A1A1A` — heroes, footer, comparison table
- **Font:** Inter
- **Content max-width:** 1280px
- **Page templates defined:** archive, single product, homepage, solution page, about page
- **Each template lists exact components in order** — writer and developer follow the same map

---

### 5. Reusable Sections Written and Scored

These blocks are done and can be pulled into any page without rewriting:

| Block | Pass Score | AI Score |
|---|---|---|
| Announcement bar | 8.2/10 | 8% |
| Technical — How it works | 8.8/10 | 7% |
| Buyer advice — 5 mistakes | 9.0/10 | 6% |
| Features — Core tech advantages | 9.2/10 | 6% |
| CTA — Homepage version | 9.1/10 | 5% |
| CTA — Archive version | 8.4/10 | 10% |
| Comparison table copy | Verified | N/A |

---

### 6. Products Archive Page — Written

`Pages/products-archive.md` is complete:
- All 6 product cards written with short descriptions and spec chips
- All reusable sections referenced (not repeated)
- Internal links listed
- Developer notes included
- Overall AI score: ~8%

---

## What's Done

- [x] `CLIENT-DATA-MAP.md` — all product specs, company data, brand voice
- [x] `Keyword Clusters/` — full keyword research files
- [x] `Claude.md` — agent instructions, Three-Pass system, rules
- [x] `Memory.md` — project state log
- [x] `Design.md` — design system + 5 page templates
- [x] `Reusable-Sections.md` — all shared copy blocks written and scored
- [x] `Pages/products-archive.md` — archive page content complete
- [x] `Last-Session.md` — this file

---

## What Still Needs to Be Done

### Immediate Priority

- [ ] **`Pages/product-sliding-door-operator.md`**
  Single product page for the #1 SEO priority product.
  Template: `single-product-page` from `Design.md`.
  Key angle: 1,800 kg capacity, -35°C to 70°C range, 10-parameter controller, full kit.

- [ ] **`Pages/product-heavy-duty-swing.md`**
  Single product page for the #2 SEO priority.
  Key angle: 650 Nm torque, 6m door length, orange manual release, F-class thermal.

- [ ] **`Pages/product-side-mounted-swing.md`**
  Single product page for the #3 SEO priority.
  Key angle: Bluetooth + WiFi, CE certified, fastest angular speed (69.7°/s), slim body.

---

### After Ahrefs Data is Received

- [ ] **`Pages/home.md`** — Homepage content
  Blocked on keyword data. Need search volumes and KD scores for core terms before writing.
  Template: `homepage` from `Design.md`.

---

### Remaining Product Pages

- [ ] `Pages/product-floor-swing.md` — concealed floor mount, aesthetic installs
- [ ] `Pages/product-top-mounted-swing.md` — slim aluminium, lightest unit, commercial glass doors
- [ ] `Pages/product-barrier-gate.md` — 10M+ cycles, 0.7s trip, parking/toll use cases

---

### Solutions Pages (after product pages)

- [ ] `Pages/solutions-residential.md`
- [ ] `Pages/solutions-commercial.md`
- [ ] `Pages/solutions-industrial.md`

---

### Supporting Pages

- [ ] `Pages/about.md` — Company story, factory, QC process, team, global reach
- [ ] `Pages/faq.md` — Buyer questions: spec selection, installation, ordering, warranty
- [ ] `Pages/contact.md` — Contact form + address + WhatsApp + phone

---

### Content Still Missing from Client

- [ ] **Ahrefs keyword data** — required before homepage and solutions pages
- [ ] **Product photos** for Side-Mounted Swing (currently only shipping box visible)
- [ ] **Product photos** for Floor Swing (currently no photos)
- [ ] **Business certifications** — confirm which products are CE certified beyond side-mounted swing

---

### System Improvements (do when time allows)

- [ ] Add keyword target to every page file header in `Pages/`
- [ ] Create `Pages/blog/` directory and write first 2–3 blog posts (buyer education content for SEO)
  - Suggested titles: "Swing Gate vs Sliding Gate: Which Operator Do You Need?", "How to Size a Gate Motor for Your Installation", "DC24V vs AC Gate Motors: Why the Voltage Difference Matters"
- [ ] Add internal linking map — which page links to which, tracked in one place
- [ ] Review and clean up `product-archive-page.html` — either delete (exploratory only) or document as visual reference

---

### 7. SILO Structure & Keyword Strategy

- Full silo map built in `SILO-Structure.md`
- Every page has an assigned primary keyword (exact match)
- Every page has a written SEO title and meta description (character counts verified)
- Keyword frequency rule: primary keyword 6–7 times per page across specific slots (H1, opening sentence, H2, body, alt text, CTA, meta)
- Anchor text rules defined — every internal link must use the destination page's exact keyword
- H1 on homepage = `automatic gate opener` (exact match, KD: 2, Vol: 3,800–4,770/mo)
- SILO rules added to `Claude.md` section 6

---

## Single Next Action

Write `Pages/product-sliding-door-operator.md` using the `single-product-page` template from `Design.md`.
Pull all spec data from `CLIENT-DATA-MAP.md` Product 1.
Run Three-Pass system on all new copy.
Target AI score: ≤15%.
