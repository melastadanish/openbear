# Design.md — Open Bear Design System & Page Templates
> This file defines the visual language, component names, and page templates.
> Content writers reference component names when structuring page `.md` files.
> Developers implement these components from this specification.

---

## 1. Brand Colors

| Name | Hex | Usage |
|---|---|---|
| **Brand Red** | `#C0392B` | CTAs, active states, eyebrows, accents |
| **Dark** | `#1A1A1A` | Hero backgrounds, footer, headings |
| **Near-Black** | `#111111` | Footer background |
| **Body Text** | `#333333` | Standard paragraph text |
| **Muted Text** | `#666666` | Secondary text, descriptions |
| **Faint Text** | `#888888` / `#AAAAAA` | Labels, meta text, footer copy |
| **Light Background** | `#FAFAFA` | Alternating section backgrounds |
| **White** | `#FFFFFF` | Default background |
| **Border** | `#E8E8E8` | Card borders, dividers |
| **Spec Background** | `#F5F5F5` | Spec chips inside product cards |

---

## 2. Typography

| Style | Size | Weight | Usage |
|---|---|---|---|
| H1 | 32–52px (fluid) | 800 | Page heroes |
| H2 | 26–38px (fluid) | 800 | Section headings |
| H3 | 20–24px | 700 | Card titles, subsection headings |
| H4 | 15–17px | 700 | Step titles, item headings |
| Body | 15–17px | 400 | Paragraphs |
| Small / Label | 12–14px | 400 / 600 | Spec labels, tags, meta |
| Eyebrow | 11–12px | 700 | Section labels above H2, uppercase, letter-spaced |
| CTA Button | 14–15px | 600–700 | Button text |

**Font:** Inter (Google Fonts)
**Line height:** 1.5–1.6 for body, 1.15–1.2 for headings

---

## 3. Components

### Component: `announcement-bar`
Thin red bar at very top of page.
- Background: Brand Red
- Text: White, 13px
- Contains: short message + clickable phone number + dismiss X

### Component: `nav`
Sticky top navigation.
- Logo left, links center, CTA button right
- Active link: Brand Red, bold
- CTA: Brand Red button, white text, "Get a Quote"
- Dropdowns: Solutions, Resources

### Component: `page-hero`
Dark full-width hero for interior pages.
- Background: Dark (`#1A1A1A`)
- Eyebrow: Brand Red, uppercase, letter-spaced
- H1: White, large
- Subtext: Muted (`#AAAAAA`)
- Badges row: 3 pill-shaped stats/claims below subtext

### Component: `hero-full` *(Homepage only)*
Full-height hero with background image/video.
- Overlay: Dark semi-transparent
- H1: White, very large
- Subtext + dual CTA buttons

### Component: `filter-sidebar`
Left sidebar for archive/listing pages.
- Sticky positioned
- Filter groups: Category, Gate Weight, Gate Type
- Checkboxes with Brand Red accent
- Apply Filters button (Brand Red) + Reset All (ghost)

### Component: `product-grid`
3-column product grid (right of filter sidebar).
- Header row: product count left, sort dropdown + view toggle right
- Cards: `product-card` component

### Component: `product-card`
Individual product card in grid.
- Image area: Light background, category tag (top-left, Brand Red pill)
- Body: Product name (H4), short description (2–3 lines), 4 spec chips (2×2 grid), footer with View Product + Get Quote buttons
- Hover: lift shadow + slight upward translate

### Component: `product-card-list` *(alternate view)*
Full-width horizontal product card for list view.
- Image left, content right
- Same spec chips, same CTAs

### Component: `section-technical`
Two-column educational section.
- Left: Eyebrow + H2 + subtitle + numbered steps (icon + title + body)
- Right: Factory or R&D photo
- Background: Light (`#FAFAFA`)

### Component: `section-buyer-advice`
Two-column advisory section.
- Left: Photo (portrait orientation)
- Right: Eyebrow + H2 + subtitle + mistake list (✕ icon + title + body)
- Background: White

### Component: `comparison-table`
Full-width table on dark background.
- Background: Dark (`#1A1A1A`)
- Eyebrow + H2 + subtitle centered above table
- Table: 6–7 rows, 6 columns. Last column: colored "Best For" pill

### Component: `section-cta`
Full-width CTA block.
- Background: Dark (`#1A1A1A`)
- H2 + subtext + two buttons (Primary Red + Ghost White)
- Centered layout

### Component: `section-stats`
3–4 column stats strip.
- Background: Brand Red or White
- Each stat: large number + label
- Used on homepage and about page

### Component: `section-features`
Grid of feature cards (3 or 4 across).
- Icon + H4 + short body
- Used to highlight tech advantages (DC24V, servo motors, etc.)

### Component: `product-hero` *(Single product pages)*
Hero for individual product pages.
- Left: Product image (large, clean white background)
- Right: Breadcrumb + Category tag + H1 + key specs strip + description + CTA buttons (Get Quote + Download Spec)
- Background: White

### Component: `product-specs-table` *(Single product pages)*
Full specifications table.
- Two-column: Parameter | Value
- Alternating row background
- Section heading above

### Component: `product-features-section` *(Single product pages)*
Key selling points section for one product.
- 3–4 feature blocks: icon + title + body
- Background: Light (`#FAFAFA`)

### Component: `product-applications` *(Single product pages)*
Where this product is used.
- Eyebrow + H2 + 3–4 use case cards (icon + title + 1 line)

### Component: `related-products`
3-card strip of other products.
- At bottom of single product pages
- H3 "You May Also Need" + 3 `product-card` components

### Component: `footer`
Full-width footer.
- Background: Near-Black (`#111111`)
- 5-column grid: Brand info + 4 link columns (Products, Solutions, Resources, Company)
- Bottom bar: copyright left, tagline right

---

## 4. Page Templates

Each page in `Pages/` follows one of these templates. The template defines which components appear in order.

---

### Template: `archive-page` → `Pages/products-archive.md`

```
announcement-bar
nav
page-hero
  — eyebrow: "Our Products"
  — h1: main headline
  — subtext: 1 sentence
  — badges: 3 claim pills
[products section — full width]
  filter-sidebar (left)
  product-grid (right)
    — product-grid-header
    — product-card × 6
section-technical
  — topic: How a gate operator system works
  — 4 steps
  — factory photo right
section-buyer-advice
  — topic: Mistakes when buying a gate operator
  — 5 mistakes
  — factory photo left
comparison-table
  — all 7 SKUs
section-cta
  — "Can't find what you're looking for?"
footer
```

---

### Template: `single-product-page` → `Pages/product-[slug].md`

```
announcement-bar
nav
[breadcrumb: Home > Products > [Product Name]]
product-hero
  — product image left
  — category tag
  — h1: product name
  — 4-stat key specs strip
  — 2-paragraph intro
  — CTA: Get Quote + Download Spec Sheet
product-specs-table
  — full technical specification table
product-features-section
  — 3–4 unique selling points with numbers
section-technical
  — how this specific product works / installation overview
product-applications
  — 3–4 use cases with icons
[optional: comparison strip — this product vs. similar models]
section-cta
  — product-specific message
related-products
  — 3 other products
footer
```

---

### Template: `homepage` → `Pages/home.md`

```
announcement-bar
nav
hero-full
  — headline + subtext + dual CTA
section-stats
  — 4 key numbers (50,000 units/yr, 6 product categories, 10M+ cycles, etc.)
[product categories strip — 6 category cards with icon + name + link]
section-features
  — 4 tech advantages (DC24V, servo motor, temp range, QC testing)
section-technical
  — "Why Factory-Direct Matters" or "Our Manufacturing Process"
[social proof / market presence — regions we serve]
section-buyer-advice
  — or testimonials/certifications if available
section-cta
footer
```

---

### Template: `solution-page` → `Pages/solutions-[type].md`

```
announcement-bar
nav
page-hero
  — eyebrow: "Solutions"
  — h1: [Residential / Commercial / Industrial] Gate Automation
[intro section: 2 columns — copy left, image right]
[relevant products grid — filtered to that solution type]
section-features
  — requirements specific to that sector
section-cta
footer
```

---

### Template: `about-page` → `Pages/about.md`

```
announcement-bar
nav
page-hero
  — eyebrow: "About Open Bear"
  — h1: company positioning statement
[company story — 2-column: copy + factory photo]
section-stats
  — Founded 2015 / 50,000 units/yr / 25 staff / 6 product categories
[manufacturing section — factory photos with captions]
[quality section — QC process, oscilloscope testing, F-class thermal]
[global reach — markets map or list]
section-cta
footer
```

---

---

### Template: `pseo-market` → `Pages/[product]-[country].md`

Used for: product × country pages targeting buyers in a specific market.
What changes per page: country name, market-specific body copy, local pain points, shipping note.
What stays fixed: layout, component order, CTA structure.

```
announcement-bar
nav
page-hero
  — eyebrow: [COUNTRY] — uppercase, Brand Red
  — h1: [Primary Keyword] — exact match, includes country
  — subtext: 1 sentence — what Open Bear offers this market
  — badges: 3 pills — e.g. "Ships to [Country]" · "Factory-Direct" · "DC24V Safe"
[market-intro — 2 columns]
  — left: 2–3 paragraphs — why this product fits this market, local context
  — right: product image or market region graphic
[pseo-specs-strip — 4 stat chips]
  — key specs for the featured product (weight capacity, temp range, torque/speed, cycles)
section-features
  — 3 feature cards specific to why this product suits this market
  — e.g. "Handles Australian heat" → -35°C to 70°C spec
[market-supply-strip — full width, Light background]
  — heading: "Supplying [Country] Distributors Direct From Factory"
  — 3 columns: Factory Capacity · Lead Time · Minimum Order
section-cta
  — "Request a Quote for [Country] Supply"
footer
```

**Variable slots (developer fills from data table):**
- `[country]` — e.g. Australia, UAE, USA
- `[product]` — e.g. sliding gate operator, swing door operator
- `[market-pain-point]` — local context sentence
- `[shipping-note]` — ships to [country] direct from Shenzhen

---

### Template: `pseo-application` → `Pages/[product]-for-[application].md`

Used for: product × use case pages targeting buyers by industry or building type.
What changes per page: application name, use case copy, relevant spec callouts.
What stays fixed: layout, component order, CTA structure.

```
announcement-bar
nav
page-hero
  — eyebrow: [APPLICATION TYPE] — e.g. "HEALTHCARE" or "WAREHOUSE"
  — h1: [Primary Keyword] — product for application
  — subtext: 1 sentence — what problem this solves for this application
  — badges: 3 pills — top 3 specs relevant to this use case
[application-intro — 2 columns]
  — left: 2–3 paragraphs — use case context, what buyers in this sector need
  — right: application photo (hospital entrance, warehouse gate, etc.)
[application-requirements — 3-column card grid]
  — heading: "What [Application] Buyers Need"
  — 3 cards: requirement + how Open Bear meets it + spec number
[pseo-specs-strip — 4 stat chips]
  — key specs for the featured product
section-buyer-advice
  — "What to check before buying a [product] for [application]"
  — 3–4 checklist items with spec references
[product-card — featured product only]
  — single prominent card with full spec chips + CTAs
section-cta
  — "Get the spec sheet for [application] use"
footer
```

**Variable slots:**
- `[application]` — e.g. hospitals, warehouses, hotels, parking lots
- `[product]` — the relevant operator type
- `[requirement-1/2/3]` — what this sector demands
- `[application-photo]` — image file name

---

### Template: `pseo-b2b` → `Pages/[product]-manufacturer.md` or `oem-[product].md`

Used for: B2B intent pages — manufacturer, supplier, OEM, wholesale, distributor searches.
What changes per page: intent keyword (manufacturer vs OEM vs supplier), product, key B2B proof points.
What stays fixed: layout, factory credibility structure, CTA.

```
announcement-bar
nav
page-hero
  — eyebrow: "FACTORY-DIRECT SUPPLY"
  — h1: [Primary Keyword] — e.g. "sliding gate operator manufacturer"
  — subtext: 1 sentence — factory capacity + global shipping
  — badges: 3 pills — "50,000 Units/Year" · "Factory-Direct Pricing" · "OEM/ODM Available"
[b2b-intro — 2 columns]
  — left: 2–3 paragraphs — why Open Bear as a supply partner
  — right: factory production line photo
[supply-proof — 4-column stat strip, Brand Red background]
  — Founded 2015 · 50,000 Units/Year · 25-Person Team · Ships Globally
[b2b-capabilities — 3-column card grid]
  — heading: "What Open Bear Offers B2B Buyers"
  — cards: OEM/ODM · Private Label · Custom Specs
[product-range-strip]
  — heading: "Full Range Available for Distribution"
  — 6 product cards (condensed — name + 2 key specs + link)
[b2b-process — numbered steps]
  — heading: "How to Start a Supply Partnership"
  — 4 steps: Enquiry → Sample → Order → Fulfilment
section-cta
  — "Request a wholesale price list"
footer
```

**Variable slots:**
- `[intent]` — manufacturer / supplier / OEM / distributor
- `[product]` — the specific operator or "gate operators" (range)
- `[b2b-proof-point]` — relevant capacity stat

---

### Template: `pseo-alternative` → `Pages/[brand]-gate-operator-alternative.md`

Used for: capturing branded competitor searches from buyers comparing or switching.
What changes per page: competitor brand name, brand-specific comparison points.
What stays fixed: layout, comparison structure, Open Bear proof points.
Rule: factual comparison only — no negative claims, no trademark misuse, no copied content.

```
announcement-bar
nav
page-hero
  — eyebrow: "OPEN BEAR vs [BRAND]"
  — h1: [Brand] Gate Operator Alternative — Open Bear
  — subtext: 1 sentence — factual positioning (factory-direct, DC24V, global supply)
  — badges: 3 pills — "Factory-Direct" · "DC24V Safety Voltage" · "50,000 Units/Year"
[alternative-intro — full width]
  — 2 paragraphs — who Open Bear is, why buyers consider alternatives, no brand disparagement
[comparison-table — 2-column: Open Bear vs [Brand]]
  — rows: Origin · Motor Type · Voltage · OEM Available · Factory Capacity · Global Supply · Price Model
  — Open Bear column highlighted (Brand Red header)
  — Note: "All [Brand] specs from public data — verify direct for latest."
[open-bear-advantages — 3-column card grid]
  — 3 reasons buyers choose Open Bear
  — each with a spec number as proof
[product-range-strip]
  — heading: "The Full Open Bear Range"
  — 6 product cards (condensed)
section-cta
  — "Compare spec sheets — request a quote"
footer
```

**Variable slots:**
- `[brand]` — competitor name (NICE, FAAC, BFT, dormakaba, etc.)
- `[brand-origin]` — their country of manufacture
- `[brand-price-model]` — distributor markup vs factory-direct
- `[comparison-points]` — facts only, sourced from public data

---

## 5. Image Naming Convention

All image file names use kebab-case and describe the content:

| Type | Naming Pattern | Example |
|---|---|---|
| Product studio shot | `[product-slug]-[angle].jpg` | `sliding-door-operator-front.jpg` |
| Product kit | `[product-slug]-kit.jpg` | `heavy-duty-swing-kit.jpg` |
| Product internal | `[product-slug]-internal.jpg` | `sliding-door-operator-internal.jpg` |
| Factory photo | `factory-[description].jpg` | `factory-production-line.jpg` |
| Factory QC | `factory-qc-[description].jpg` | `factory-qc-oscilloscope.jpg` |
| R&D photo | `rd-[description].jpg` | `rd-engineer-testing.jpg` |

All product images: white background, 1:1 ratio minimum, high resolution.
All factory photos: landscape orientation preferred, 4:3 or 16:9.

---

## 6. Icon Sets

Use consistent icons across the site. Recommended: Phosphor Icons or Heroicons (outline style).

| Context | Icon |
|---|---|
| Temperature range | thermometer |
| Noise level | speaker-wave |
| Weight / capacity | scale |
| Speed | lightning-bolt |
| Safety | shield-check |
| Power / voltage | bolt |
| Installation | wrench |
| Connectivity (WiFi/BT) | wifi |
| Certificate | badge-check |
| Factory | building-factory |
| Global shipping | globe |

---

## 7. Spacing & Layout

- **Max content width:** 1280px (centered)
- **Section padding:** 64–80px top/bottom
- **Grid gap (cards):** 24px
- **Sidebar width:** 260px (product archive)
- **Border radius:** 4px (buttons, tags), 8px (cards, sections), 12px (large images)
- **Mobile breakpoint:** 768px — stack all grids to single column
