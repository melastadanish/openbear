# SILO-Structure.md — Open Bear Site Architecture
> This file defines the keyword silo for the entire site.
> Every page, every internal link, and every piece of content must follow this structure.
> Do not add internal links that break the silo — see rules at the bottom.

---

## URL Structure Decision

**Flat keyword slugs at root level.** No nested directories.

| ❌ Old (nested) | ✅ New (flat keyword slug) |
|---|---|
| `/solutions/commercial` | `/commercial-gate-operator` |
| `/solutions/residential` | `/residential-gate-opener` |
| `/solutions/industrial` | `/industrial-gate-operator` |
| `/products/sliding-door-operator` | `/sliding-gate-operator` |
| `/products/heavy-duty-swing-door-operator` | `/heavy-duty-swing-gate-operator` |
| `/products/side-mounted-swing-door-operator` | `/side-mounted-swing-door-operator` |
| `/products/floor-swing-door-operator` | `/floor-swing-door-operator` |
| `/products/top-mounted-swing-door-operator` | `/top-mounted-swing-door-operator` |
| `/products/high-speed-barrier-gate` | `/barrier-gate-operator` |
| `/products` | `/gate-operators` |
| `/blog/how-a-gate-operator-system-works` | `/blog/how-a-gate-operator-system-works` *(blog stays nested)* |

**Why this matters for SEO:**
- Keyword sits at root level — stronger URL signal to Google
- Shorter URL = cleaner link equity
- The slug itself reinforces the page's primary keyword
- No wasted directory depth in the URL path

---

## Product Archive Filter — Category URLs

The filter strip on `/gate-operators` uses real crawlable URLs — not JavaScript filters.
Each category tab navigates to its own indexable page with unique H1 and intro copy.

| Filter Tab Label | URL | Primary Keyword | Products Shown |
|---|---|---|---|
| All Gate Operators | `/gate-operators` | gate operators | All 6 products |
| Sliding Gate | `/gate-operators/sliding` | sliding gate operator | Sliding (200W + 400W) |
| Swing Gate | `/gate-operators/swing` | swing gate operator | Heavy-duty + Side-mounted + Floor + Top-mounted |
| Barrier Gate | `/gate-operators/barrier` | barrier gate operator | High-speed barrier gate |

### Category Page Requirements
Each category URL (`/gate-operators/sliding`, `/gate-operators/swing`, `/gate-operators/barrier`) must have:
- Unique H1 containing the category keyword
- Short intro paragraph (2–3 sentences) — unique copy, not duplicated from `/gate-operators`
- Only the relevant product cards shown
- Breadcrumb: `Home > Gate Operators > [Category]`
- Links UP to `/gate-operators` and `/`
- Canonical tag pointing to itself (not to `/gate-operators`)

### SILO Position of Category Pages
Category filter pages sit between Tier 2 and Tier 3 — they are sub-pages of `/gate-operators` and parent pages of individual product pages within their family.

```
/gate-operators (Tier 2)
  ├── /gate-operators/sliding  → links to /sliding-gate-operator
  ├── /gate-operators/swing    → links to all 4 swing product pages
  └── /gate-operators/barrier  → links to /barrier-gate-operator
```

### Linking Rules for Category Filter Pages
- Link UP to `/gate-operators` and `/`
- Link DOWN to their product children only
- Do NOT cross-link between `/gate-operators/sliding` and `/gate-operators/barrier`
- Anchor text for `/gate-operators/sliding` = "sliding gate operator"
- Anchor text for `/gate-operators/swing` = "swing gate operator"
- Anchor text for `/gate-operators/barrier` = "barrier gate operator"

---

## Full Silo Map

```
TIER 1 — HOMEPAGE ✅ WRITTEN
openbear.com/
Keyword: automatic gate opener
Vol: 3,800–4,770/mo | KD: 2
Links DOWN to: all Tier 2 pages
Receives links FROM: all Tier 2 and Tier 3 pages
Internal links out: /gate-operators + all 6 product pages + /contact (8 total)
─────────────────────────────────────────────────────
         │
TIER 2 — CATEGORY & SOLUTION PAGES (flat slugs)
         │
         ├── /gate-operators
         │   Keyword: gate operators
         │   Vol: 860–870/mo
         │   Links: UP to / · DOWN to 3 category filter pages + all 6 product pages
         │   Filter tabs: /gate-operators/sliding · /gate-operators/swing · /gate-operators/barrier
         │
         │   ├── /gate-operators/sliding
         │   │   Keyword: sliding gate operator
         │   │   Links: UP to /gate-operators · / · DOWN to /sliding-gate-operator
         │   │
         │   ├── /gate-operators/swing
         │   │   Keyword: swing gate operator
         │   │   Links: UP to /gate-operators · / · DOWN to 4 swing product pages
         │   │
         │   └── /gate-operators/barrier
         │       Keyword: barrier gate operator
         │       Links: UP to /gate-operators · / · DOWN to /barrier-gate-operator
         │
         ├── /commercial-gate-operator
         │   Keyword: commercial gate operator
         │   Vol: ~800/mo
         │   Links: UP to / · DOWN to heavy-duty + sliding + barrier + top-mounted
         │
         ├── /residential-gate-opener
         │   Keyword: residential gate opener
         │   Links: UP to / · DOWN to side-mounted + floor + top-mounted
         │
         └── /industrial-gate-operator
             Keyword: industrial gate operator
             Links: UP to / · DOWN to sliding + heavy-duty + barrier
─────────────────────────────────────────────────────
         │
TIER 3 — PRODUCT PAGES (flat keyword slugs)
         │
         ├── /sliding-gate-operator
         │   Keyword: sliding gate operator
         │   Vol: 5,000+/mo | KD: medium
         │   Links UP to: /gate-operators · /
         │   Receives from: /gate-operators · / · /industrial-gate-operator · blog posts
         │
         ├── /heavy-duty-swing-gate-operator
         │   Keyword: heavy duty swing gate operator
         │   Vol: 1,500+/mo | KD: medium
         │   Links UP to: /gate-operators · /
         │   Receives from: /gate-operators · / · /commercial-gate-operator · /industrial-gate-operator
         │
         ├── /side-mounted-swing-door-operator
         │   Keyword: side mounted swing door operator
         │   Vol: growing | KD: low
         │   Links UP to: /gate-operators · /
         │   Receives from: /gate-operators · / · /residential-gate-opener
         │
         ├── /floor-swing-door-operator
         │   Keyword: floor swing door operator
         │   Vol: moderate | KD: low
         │   Links UP to: /gate-operators · /
         │   Receives from: /gate-operators · / · /residential-gate-opener
         │
         ├── /top-mounted-swing-door-operator
         │   Keyword: top mounted swing door operator
         │   Vol: moderate | KD: low
         │   Links UP to: /gate-operators · /
         │   Receives from: /gate-operators · / · /commercial-gate-operator · /residential-gate-opener
         │
         └── /barrier-gate-operator
             Keyword: barrier gate operator
             Vol: 1,200+/mo | KD: medium
             Links UP to: /gate-operators · /
             Receives from: /gate-operators · / · /commercial-gate-operator · /industrial-gate-operator
─────────────────────────────────────────────────────
TIER 3 — BLOG (supports Tier 1 and Tier 2)

/blog/how-a-gate-operator-system-works
  Keyword: how does a gate operator work
  Links UP to: / · /gate-operators
  Supports: Homepage authority

/blog/swing-gate-vs-sliding-gate
  Keyword: swing gate vs sliding gate operator
  Links UP to: /gate-operators · /sliding-gate-operator · /heavy-duty-swing-gate-operator
  Supports: Both product pages

/blog/dc24v-vs-ac-gate-motors
  Keyword: DC24V gate motor
  Links UP to: / · /gate-operators
  Supports: Homepage + brand differentiation

/blog/how-to-size-a-gate-motor
  Keyword: how to size a gate motor
  Links UP to: / · /gate-operators
  Supports: Buyer education → product range
```

---

## Page Keyword & URL Map (Quick Reference)

| Page | URL | Primary Keyword | Tier |
|---|---|---|---|
| Homepage | `/` | automatic gate opener | 1 | ✅ Written |
| Products Archive | `/gate-operators` | gate operators | 2 |
| Sliding Category Filter | `/gate-operators/sliding` | sliding gate operator | 2.5 |
| Swing Category Filter | `/gate-operators/swing` | swing gate operator | 2.5 |
| Barrier Category Filter | `/gate-operators/barrier` | barrier gate operator | 2.5 |
| Commercial Solutions | `/commercial-gate-operator` | commercial gate operator | 2 |
| Residential Solutions | `/residential-gate-opener` | residential gate opener | 2 |
| Industrial Solutions | `/industrial-gate-operator` | industrial gate operator | 2 |
| Sliding Gate Opener | `/sliding-gate-operator` | sliding gate opener | 3 | ✅ Written |
| Heavy Duty Swing Gate Opener | `/heavy-duty-swing-gate-operator` | heavy duty swing gate opener | 3 | ✅ Written |
| Side-Mounted Swing | `/side-mounted-swing-door-operator` | side mounted swing door operator | 3 |
| Floor Swing | `/floor-swing-door-operator` | floor swing door operator | 3 |
| Top-Mounted Swing | `/top-mounted-swing-door-operator` | top mounted swing door operator | 3 |
| Barrier Gate | `/barrier-gate-operator` | barrier gate operator | 3 |
| Blog: How it works | `/blog/how-a-gate-operator-system-works` | how does a gate operator work | 3 |
| Blog: Swing vs Sliding | `/blog/swing-gate-vs-sliding-gate` | swing gate vs sliding gate operator | 3 |
| Blog: DC24V vs AC | `/blog/dc24v-vs-ac-gate-motors` | DC24V gate motor | 3 |
| Blog: How to size | `/blog/how-to-size-a-gate-motor` | how to size a gate motor | 3 |

---

## SEO Title & Meta Description — All Pages

### Tier 1

**Homepage (`/`)**
- Title: `Automatic Gate Opener | Open Bear` *(33 chars)*
- Description: `Find the right automatic gate opener for your property. DC24V safety voltage, 60 dB quiet motors, and remote control built in. Ships globally.` *(144 chars)*
- Status: ✅ Written — Pages/home.md · Pass A: 9.3/10 · AI score: 9%

---

### Tier 2

**Products Archive (`/gate-operators`)**
- Title: `Gate Operators & Door Automation Products | Open Bear` *(53 chars)*
- Description: `Browse 6 categories of industrial gate operators — sliding, swing, and barrier. DC24V safety voltage. Factory-direct from Shenzhen. Ships globally.` *(150 chars)*

**Commercial (`/commercial-gate-operator`)**
- Title: `Commercial Gate Operator Systems | Open Bear` *(44 chars)*
- Description: `Commercial gate operator solutions for warehouses, car parks, and commercial facilities. Heavy-duty, DC24V, factory-direct supply.` *(131 chars)*

**Residential (`/residential-gate-opener`)**
- Title: `Residential Gate Opener Supply | Open Bear` *(42 chars)*
- Description: `Reliable residential gate openers for housing developments and gated communities. Sliding, swing, and concealed floor models available.` *(135 chars)*

**Industrial (`/industrial-gate-operator`)**
- Title: `Industrial Gate Operator Supply | Open Bear` *(43 chars)*
- Description: `Industrial gate operators for factories, logistics centres, and high-traffic facilities. Up to 1,800 kg capacity. Factory-direct from Shenzhen.` *(144 chars)*

---

### Tier 3 — Product Pages

**Sliding Gate Operator (`/sliding-gate-operator`)**
- Title: `Sliding Gate Operator — Up to 1,800 kg | Open Bear` *(51 chars)*
- Description: `28 rack-and-pinion sliding gate operator for gates up to 1,800 kg. DC24V servo motor. -35°C to 70°C. Full kit. Factory-direct supply.` *(135 chars)*

**Heavy-Duty Swing (`/heavy-duty-swing-gate-operator`)**
- Title: `Heavy Duty Swing Gate Operator — 650 Nm | Open Bear` *(52 chars)*
- Description: `Heavy duty swing gate operator with 650 Nm torque. Handles gates up to 6 m long and 1,200 kg. DC24V, F-class thermal protection.` *(129 chars)*

**Side-Mounted Swing (`/side-mounted-swing-door-operator`)**
- Title: `Side Mounted Swing Door Operator | Open Bear` *(44 chars)*
- Description: `Side mounted swing door operator with Bluetooth, WiFi, and remote control. CE certified. 69.7°/s. Slim body. DC24V. Factory-direct.` *(132 chars)*

**Floor Swing (`/floor-swing-door-operator`)**
- Title: `Floor Swing Door Operator — Concealed Mount | Open Bear` *(55 chars)*
- Description: `Concealed floor swing door operator for architectural installations. 250 kg capacity. DC24V. Invisible hardware. Factory-direct supply.` *(136 chars)*

**Top-Mounted Swing (`/top-mounted-swing-door-operator`)**
- Title: `Top Mounted Swing Door Operator | Open Bear` *(43 chars)*
- Description: `Top mounted swing door operator — slim aluminium profile, 5.3 kg, 200 kg capacity. Ideal for commercial glass doors. DC24V. Factory-direct.` *(141 chars)*

**Barrier Gate (`/barrier-gate-operator`)**
- Title: `Barrier Gate Operator — 10 Million Cycles | Open Bear` *(53 chars)*
- Description: `High-speed barrier gate operator rated for 10,000,000+ cycles. 0.7 s trip speed. Arms up to 6 m. DC24V. Built for parking and access control.` *(144 chars)*

---

### Tier 3 — Blog Posts

**How it works (`/blog/how-a-gate-operator-system-works`)**
- Title: `How Does a Gate Operator System Work? | Open Bear` *(50 chars)*
- Description: `Learn how a gate operator system works — motor drive, control board, safety sensors, and battery backup. Buyer's guide from the manufacturer.` *(143 chars)*

**Swing vs Sliding (`/blog/swing-gate-vs-sliding-gate`)**
- Title: `Swing Gate vs Sliding Gate Operator | Open Bear` *(47 chars)*
- Description: `Swing gate vs sliding gate operator — how to choose. Compare torque, clearance, weight limits, and cost. Practical guide from the manufacturer.` *(145 chars)*

**DC24V vs AC (`/blog/dc24v-vs-ac-gate-motors`)**
- Title: `DC24V vs AC Gate Motor: Why Voltage Matters | Open Bear` *(55 chars)*
- Description: `DC24V gate motor vs AC: safety, efficiency, and compliance differences explained. Why factory-direct operators run on 24V DC by default.` *(138 chars)*

**How to size (`/blog/how-to-size-a-gate-motor`)**
- Title: `How to Size a Gate Motor for Your Installation | Open Bear` *(57 chars)*
- Description: `Step-by-step guide to sizing a gate motor — gate weight, torque requirements, operator type, and safety sensors. From the manufacturer.` *(137 chars)*

---

## SILO Linking Rules

### What You Must Do
1. Every Tier 3 page links UP to its Tier 2 parent (`/gate-operators`) and Tier 1 (`/`)
2. Every Tier 2 page links UP to `/` and DOWN to its relevant product children
3. Homepage links DOWN to all 4 Tier 2 pages + top 3 priority product pages directly
4. Blog posts always link UP to Tier 1 or Tier 2 — never sideways to other blog posts
5. Anchor text must always be the exact primary keyword of the destination page

### What You Must NOT Do
1. Do NOT link from `/sliding-gate-operator` directly to `/barrier-gate-operator` — cross-silo
2. Do NOT link from a product page down to a blog post
3. Do NOT use generic anchor text — never "click here", "read more", "this page", "here"
4. Do NOT nest URLs — all pages sit at root level (except `/blog/`)
5. Do NOT change a URL slug after the site goes live — 301 redirects required if you do

### Anchor Text Reference

| Destination | Correct Anchor Text |
|---|---|
| `/` | automatic gate opener |
| `/gate-operators` | gate operators |
| `/gate-operators/sliding` | sliding gate operator |
| `/gate-operators/swing` | swing gate operator |
| `/gate-operators/barrier` | barrier gate operator |
| `/commercial-gate-operator` | commercial gate operator |
| `/residential-gate-opener` | residential gate opener |
| `/industrial-gate-operator` | industrial gate operator |
| `/sliding-gate-operator` | sliding gate operator |
| `/heavy-duty-swing-gate-operator` | heavy duty swing gate operator |
| `/side-mounted-swing-door-operator` | side mounted swing door operator |
| `/floor-swing-door-operator` | floor swing door operator |
| `/top-mounted-swing-door-operator` | top mounted swing door operator |
| `/barrier-gate-operator` | barrier gate operator |

---

## PSEO Pages — Silo Tier & Linking Rules

PSEO pages sit outside the core silo hierarchy. They link UP into the silo but do not receive links from core pages. This keeps the core silo clean while PSEO pages accumulate their own long-tail authority.

### PSEO Linking Rules

| Page Type | Links UP to | Does NOT link to |
|---|---|---|
| Market pages | `/gate-operators` + relevant product page | Other PSEO pages |
| Application pages | `/gate-operators` + relevant product page | Other PSEO pages |
| B2B pages | `/gate-operators` + all 6 product pages | Core solution pages |
| Alternative pages | `/gate-operators` + all 6 product pages | Competitor sites (comparison table only) |

**Core rule:** PSEO pages are leaf pages — they receive no internal links from core pages and link only upward into the silo. They do not cross-link to each other.

### PSEO URL Slugs

| Page | URL | Template |
|---|---|---|
| Sliding gate — Australia | `/sliding-gate-operator-australia` | `pseo-market` |
| Swing door — UAE | `/swing-door-operator-uae` | `pseo-market` |
| Swing door — hospitals | `/swing-door-operator-for-hospitals` | `pseo-application` |
| Sliding gate — warehouses | `/sliding-gate-operator-for-warehouses` | `pseo-application` |
| Sliding gate manufacturer | `/sliding-gate-operator-manufacturer` | `pseo-b2b` |
| OEM swing door operator | `/oem-swing-door-operator` | `pseo-b2b` |
| NICE alternative | `/nice-gate-operator-alternative` | `pseo-alternative` |
| FAAC alternative | `/faac-gate-operator-alternative` | `pseo-alternative` |

### PSEO Anchor Text Reference

| Destination | Correct Anchor Text |
|---|---|
| `/sliding-gate-operator-australia` | sliding gate operator Australia |
| `/swing-door-operator-uae` | swing door operator UAE |
| `/swing-door-operator-for-hospitals` | swing door operator for hospitals |
| `/sliding-gate-operator-for-warehouses` | sliding gate operator for warehouses |
| `/sliding-gate-operator-manufacturer` | sliding gate operator manufacturer |
| `/oem-swing-door-operator` | OEM swing door operator |
| `/nice-gate-operator-alternative` | NICE gate operator alternative |
| `/faac-gate-operator-alternative` | FAAC gate operator alternative |

---

## Internal Link Count Per Page (Minimum)

| Page | Min Links | Targets |
|---|---|---|
| Homepage `/` | 8 | All 4 Tier 2 pages + top 3 product pages + 1 blog |
| `/gate-operators` | 8 | All 6 product pages + `/` |
| Each product page | 3 | `/gate-operators` + `/` + 1 relevant solution page |
| Each solution page | 5 | `/` + `/gate-operators` + 2–3 relevant product pages |
| Each blog post | 3 | `/` + `/gate-operators` + 1 product page |
