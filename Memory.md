# Memory.md — Open Bear Project Log
> Running log of decisions, completed work, and current state.
> Update this file every session. Most recent entries at the top.

---

## Current Status

| Item | Status |
|---|---|
| Project files setup | ✅ Complete |
| SILO-Structure.md | ✅ Complete |
| CLIENT-DATA-MAP.md | ✅ Complete |
| CLAUDE.md (agent rules) | ✅ Complete — 7-step workflow, consumer audience |
| Design.md | ✅ Complete |
| Slice-Library.md | ✅ Complete — 41 slices, 77 variations |
| Reusable-Sections.md | ✅ Complete — synced to Slice Library shortcodes |
| Quality-Check-System.md | ✅ Complete — full execution method for all checks |
| Master-Writing-System.md | ✅ Complete — reusable across projects |
| Products archive page | ✅ Complete (Pages/products-archive.md) |
| PSEO templates | ✅ Complete (4 templates in Design.md) |
| PSEO sample pages | ✅ Complete (8 pages in Pages/) |
| Keyword clusters | ✅ Complete (see Keyword Clusters/) |
| Homepage | ✅ Complete — Pages/home.md · Pass A 9.3/10 · AI 9% |
| Individual product pages | ⏳ Queued — sliding gate operator is next |
| Solutions pages | ⏳ Queued |
| About page | ⏳ Queued |

---

## Session Log

### 2026-05-30 — Session 4

**Work completed:**
- Audience changed from B2B (distributors/installers) to end consumers (homeowners, property managers)
- Spec chip format removed across all files — numbers now embedded naturally in sentences
- CLAUDE.md fully rewritten — 7-step workflow (Step 0 Brief → Step 1 Outline → Step 2 Section writing → Step 3 Consumer journey read → Step 4 Three passes → Step 5 Differentiation check → Step 6 Checklist)
- Quality-Check-System.md created — full execution method for all 5 Tier 1 checks and all 3 passes including AI-written score signal method
- Master-Writing-System.md created — standalone reusable system for other projects
- Slice-Library.md updated — [trust-supply] replaced with [trust-markets] on homepage assembly map · [trust-markets] slice added · chip fields removed from [features-proof-list] and [features-cards]
- Reusable-Sections.md updated — all component names synced to Slice Library shortcodes · buyer advice rewritten for consumer audience · footer copyright fixed (HEIXIONG → Open Bear)
- expert-profile.md updated — B2B references removed · objection handling expanded to 8 objections · product card structure updated
- Homepage written — Pages/home.md · 7 sections · Pass A 9.3/10 · Pass B 3 fixes · Pass C all 6 tests passed · AI score 9% · all 5 differentiators present · all 8 objections answered
- SILO-Structure.md updated — homepage marked written, meta tags updated to consumer version, internal link count recorded

**Decisions made:**
- Audience is end consumers — not B2B. All future pages written for homeowners and property owners.
- Numbers live inside sentences — never as standalone chip labels
- 7-step workflow is now mandatory for all pages — no shortcuts
- [trust-markets] replaces [trust-supply] on homepage — consumer regions strip, not B2B supply terms
- Homepage does not need Ahrefs data to proceed — keyword cluster file had sufficient data (KD 2, clear primary keyword)

### 2026-05-28 — Session 3

**Work completed:**
- Added `pseo-strategy.md` to project (user-created, documents full PSEO program)
- Added 4 PSEO templates to `Design.md`: `[pseo-market]`, `[pseo-application]`, `[pseo-b2b]`, `[pseo-alternative]`
- Wrote 8 sample PSEO pages under `Pages/`:
  - `sliding-gate-operator-australia.md` — market template sample
  - `swing-door-operator-uae.md` — market template sample
  - `swing-door-operator-for-hospitals.md` — application template sample
  - `sliding-gate-operator-for-warehouses.md` — application template sample
  - `sliding-gate-operator-manufacturer.md` — B2B intent template sample
  - `oem-swing-door-operator.md` — B2B intent template sample
  - `nice-gate-operator-alternative.md` — alternative template sample
  - `faac-gate-operator-alternative.md` — alternative template sample
- Added PSEO tier section to `SILO-Structure.md` with URL slugs, linking rules, and anchor text reference
- Skipped: `[pseo-standards]` (CE/UL) and `[pseo-comparison]` — user decision

**Decisions made:**
- PSEO pages are leaf pages — no incoming links from core silo pages
- Alternative pages include mandatory disclaimer noting specs sourced from public data
- 2 sample pages per template = proof of concept before full PSEO build-out

### 2026-05-28 — Session 1

**Work completed:**
- Created `CLIENT-DATA-MAP.md` — full product data, specs, company info, brand voice, SEO priorities
- Created keyword cluster files in `Keyword Clusters/`
- Wrote initial product archive page as HTML (file: `product-archive-page.html`) — this was exploratory. Going forward, all content goes in `.md` files under `Pages/`
- Set up project file structure: `Claude.md`, `Memory.md`, `Design.md`, `Reusable-Sections.md`

**Decisions made:**
- Content-only workflow: all page content in `.md` files, no HTML
- Three-pass copywriting system established in `Claude.md`
- Each page gets its own file in `Pages/`
- Design templates live in `Design.md`, reusable copy blocks in `Reusable-Sections.md`

**Note on the HTML file:**
`product-archive-page.html` was created during an exploratory session. It contains the right structure and copy but was written before the content-only rule was established. The content from this file should be extracted and properly written in `Pages/products-archive.md` using the Three-Pass system.

---

## Key Decisions

| Decision | Reason | Date |
|---|---|---|
| Content in `.md` only, no HTML | Developer handles templates; we handle words | 2026-05-28 |
| Three-pass copywriting system | AI-written content scores poorly — human voice required | 2026-05-28 |
| Audience changed to end consumers | User decision — homeowners and property owners, not B2B | 2026-05-30 |
| All specs from CLIENT-DATA-MAP.md only | Prevents invented or inaccurate specs | 2026-05-28 |
| Numbers embedded in sentences, not chips | Chips feel mechanical — sentences read naturally | 2026-05-30 |
| 7-step workflow mandatory for all pages | Brief + outline before writing prevents wasted copy | 2026-05-30 |
| [trust-markets] on homepage, not [trust-supply] | Supply terms are B2B — homepage audience is consumer | 2026-05-30 |

---

## What's Next

**Priority order:**

1. `Pages/product-sliding-door-operator.md` — Highest SEO priority product (vol 5,000+/mo)
2. `Pages/product-heavy-duty-swing.md` — Second SEO priority
3. `Pages/product-side-mounted-swing.md` — Third SEO priority
4. `Pages/solutions-residential.md` — Residential gate opener
5. `Pages/solutions-commercial.md` — Commercial gate operator
6. `Pages/solutions-industrial.md` — Industrial gate operator
7. Remaining product pages (floor swing, top-mounted, barrier gate)
8. `Pages/about.md`

**Outstanding from client:**
- Product photos for Side-Mounted Swing (shipping box only currently)
- Product photos for Floor Swing
- Hero background image for homepage (gate in motion, property setting)

---

## Confirmed Product Details (quick reference)

| Product | Key Differentiator | Max Load | SEO Priority |
|---|---|---|---|
| Sliding Door Operator | 1,800 kg capacity, -35°C to 70°C | 1,800 kg | 🔴 #1 |
| Heavy-Duty Swing | 650 Nm torque, 6m door length | 1,200 kg | 🔴 #2 |
| Side-Mounted Swing | Bluetooth + WiFi, CE certified, 69.7°/s | 200 kg | 🔴 #3 |
| Floor Swing | Concealed install, 250 kg | 250 kg | 🟠 |
| Top-Mounted Swing | Lightest (5.3 kg), slim aluminium | 200 kg | 🟠 |
| High-Speed Barrier Gate | 10M+ cycles, 0.7s trip speed | — | 🟠 |

---

## Pending Inputs from Client

- [ ] Ahrefs keyword data (needed before homepage)
- [ ] Product photos for Side-Mounted Swing (currently only shipping box visible)
- [ ] Product photos for Floor Swing
- [ ] Company registration / business license (if needed for credibility section)

---

## Competitor Reference

| Competitor | Notes |
|---|---|
| niceforyou.com | Design reference + direct competitor |
| blutezeit.com | Direct competitor |
| thejoytech.com | Direct competitor |

Open Bear differentiators vs competitors:
- DC24V safety voltage (most competitors use AC)
- Servo permanent magnet synchronous motor (smoother, more precise)
- Factory-direct pricing (no distributor markup)
- 50,000 units/year capacity (scale credibility)
