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
| Claude.md (agent rules) | ✅ Complete |
| Design.md | ✅ Complete |
| Reusable-Sections.md | ✅ Complete |
| Products archive page | ✅ Complete (Pages/products-archive.md) |
| PSEO templates | ✅ Complete (4 templates in Design.md) |
| PSEO sample pages | ✅ Complete (8 pages in Pages/) |
| Homepage | ⏳ Awaiting Ahrefs keyword data |
| Individual product pages | ⏳ Queued |
| Keyword clusters | ✅ Complete (see Keyword Clusters/) |

---

## Session Log

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
| B2B tone — no consumer language | Buyers are agents, distributors, installers — not homeowners | 2026-05-28 |
| All specs from CLIENT-DATA-MAP.md only | Prevents invented or inaccurate specs | 2026-05-28 |
| Product archive page comes before homepage | Homepage waiting on Ahrefs data | 2026-05-28 |

---

## What's Next

**Priority order:**

1. `Pages/products-archive.md` — Write full archive page content using Three-Pass system
2. `Pages/product-sliding-door-operator.md` — Highest SEO priority product
3. `Pages/product-heavy-duty-swing.md` — Second SEO priority
4. `Pages/product-side-mounted-swing.md` — Third SEO priority
5. `Pages/home.md` — After Ahrefs data received
6. Remaining product pages
7. Solutions pages
8. About page

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
