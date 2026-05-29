# Slice-Library.md — Open Bear Slice Registry
> Single source of truth for all reusable page sections.
> Design.md covers colours, typography, spacing. This file covers everything about slices.
> Wireframe preview: `slices/wireframe.html`

---

## How to Use This File

**Writers** — when selecting a section during the outline step, pick a shortcode + variation from this file. Write only content fields — no layout descriptions.

**Developers** — build each slice variation once. Every page is assembled from this registry. No custom layout work per page.

**Format in `.md` files:**
```
### [shortcode·var-a]
field-name: content here
field-name: content here
```

---

## Naming Convention

`[group-descriptor]` — all lowercase, hyphen-separated.

Variation suffix: `·var-a` or `·var-b` appended when referencing in page files.

---

## Sub-Components

These are elements used *inside* slices. They are not standalone slices and do not appear in the wireframe as separate rows.

| Sub-Component | Used Inside | Description |
|---|---|---|
| `product-card` | `[product-archive]`, `[product-strip]` | Image + category tag + name + description + 4 spec chips + 2 CTAs |
| `product-card-list` | `[product-archive·var-b]` | Horizontal card — image left, content right |
| `spec-chip` | `[features-cards]`, `[specs-strip]`, `[hero-product]` | Small pill: label + value |
| `breadcrumb` | `[hero-product]`, `[hero-page·var-b]` | Home > Category > Page Name |
| `filter-sidebar` | `[product-archive]` | Sticky sidebar: category checkboxes, weight range, gate type, apply/reset buttons |
| `tab-bar` | `[product-tabs]` | Horizontal tab labels — Overview / Specs / Contents / Installation |
| `accordion-row` | `[content-accordion]` | Single Q&A row — question + expand chevron + collapsible answer |

---

## GROUP 1 — GLOBAL

Shown once on every page. No per-page variation. Shown once at top of wireframe.

---

### `[global-announcement]` — Announcement Bar

**Purpose:** Thin persistent bar above nav. Promo message + phone number.

| Field | Value |
|---|---|
| `message` | Short text — e.g. "Factory-direct pricing. Ships globally." |
| `phone` | Clickable phone number |

**Variation:** 1 only.

---

### `[global-nav]` — Navigation

**Purpose:** Sticky top navigation on all pages.

| Field | Value |
|---|---|
| `logo` | SVG or image file |
| `links` | Home, Products (dropdown), Solutions (dropdown), Resources (dropdown) |
| `cta-label` | Button text — "Get a Quote" |
| `cta-url` | `/contact` |

**Variation:** 1 only.

---

### `[global-footer]` — Footer

**Purpose:** Full-width footer. 5-column layout.

| Field | Value |
|---|---|
| `col-1` | Brand name + tagline + contact snippet |
| `col-2` | Products links |
| `col-3` | Solutions links |
| `col-4` | Resources links |
| `col-5` | Company links |
| `copyright` | Copyright line |
| `tagline` | "Secure. Reliable. Automatic." |

**Variation:** 1 only.

---

## GROUP 2 — HERO

---

### `[hero-home]` — Hero — Homepage

**Purpose:** Full-height first impression. Homepage only.

| Field | Var A | Var B |
|---|---|---|
| `bg-image` | Full-width background image | Full-width background image |
| `h1` | Large centered headline | Large headline, left-aligned |
| `subtext` | 1 sentence centered | 1 sentence left-aligned |
| `cta-primary` | Button label + URL | Button label + URL |
| `cta-secondary` | Ghost button label + URL | — |
| `product-image` | — | Product hero image, right side |

**Var A:** Full-width bg image. Dark overlay. Centered H1 + subtext + dual CTA buttons.
**Var B:** Full-width bg image. Dark overlay. Text block left panel. Product image right panel.

---

### `[hero-page]` — Hero — Interior Page

**Purpose:** Standard hero for all interior pages. Dark background.

| Field | Var A | Var B |
|---|---|---|
| `eyebrow` | Category label, uppercase | Category label, uppercase |
| `h1` | Page headline | Page headline |
| `subtext` | 1 sentence | 1 sentence |
| `badge-1` | Pill text | Pill text |
| `badge-2` | Pill text | Pill text |
| `badge-3` | Pill text | Pill text |
| `image` | — | Scene or product image, right side |

**Var A:** Dark bg. Centered: eyebrow + H1 + subtext + 3 badge pills.
**Var B:** Dark bg. Text left panel (eyebrow + H1 + subtext + badges). Image right panel.

---

### `[hero-product]` — Hero — Product Page

**Purpose:** Product detail hero. White background. Image-led.

| Field                     | Description                            |
| ------------------------- | -------------------------------------- |
| `breadcrumb`              | Home > Gate Operators > [Product Name] |
| `category-tag`            | e.g. "Sliding Gate Operator"           |
| `product-image`           | Large clean product photo, white bg    |
| `h1`                      | Product name (exact keyword)           |
| `spec-1` through `spec-4` | Key spec chips: label + value          |
| `description`             | 2 short paragraphs                     |
| `cta-primary`             | "Get a Quote"                          |
| `cta-secondary`           | "Download Spec Sheet"                  |

**Var A:** Product image left (large). Breadcrumb + tag + H1 + spec strip + description + CTAs right.
**Var B:** Product image full-width top. Specs + description + CTAs below in 2-col layout.

---

### `[hero-market]` — Hero — PSEO Market

**Purpose:** Market-specific hero for PSEO country pages.

| Field | Description |
|---|---|
| `eyebrow` | Country/region name — uppercase |
| `h1` | Exact-match primary keyword including country |
| `subtext` | 1 sentence — what Open Bear offers this market |
| `badge-1` | e.g. "Ships to [Country]" |
| `badge-2` | "Factory-Direct Pricing" |
| `badge-3` | "DC24V Safe" |
| `region-image` | Optional: map region or market scene image |

**Var A:** Dark bg. Eyebrow in red. H1 + subtext + 3 badge pills. Centered.
**Var B:** Dark bg. Text left. Region image or product image right.

---

## GROUP 3 — INTRO

---

### `[intro-split]` — Intro — Split

**Purpose:** 2-column section. Body copy one side, image other side.

| Field | Description |
|---|---|
| `eyebrow` | Optional section label |
| `h2` | Section headline |
| `body-1` | Paragraph 1 |
| `body-2` | Paragraph 2 |
| `body-3` | Paragraph 3 (optional) |
| `image` | Image file name |
| `image-alt` | Alt text |

**Var A:** Text left. Image right.
**Var B:** Image left. Text right.

---

### `[intro-centered]` — Intro — Centered

**Purpose:** Single-column centered intro. Category pages, about.

| Field | Description |
|---|---|
| `eyebrow` | Optional label |
| `h2` | Headline |
| `body` | 2–3 sentences max, centered |

**Var A:** Eyebrow + H2 + body. Centered. Max 700px wide. White bg.
**Var B:** Large eyebrow stat (number only) above H2 + body. Centered.

---

### `[intro-stat-lead]` — Intro — Stat Lead

**Purpose:** Opens with a dominant proof number. B2B and trust-heavy pages.

| Field | Description |
|---|---|
| `stat-number` | e.g. "50,000" |
| `stat-label` | e.g. "units per year" |
| `h2` | Headline |
| `body` | 2 paragraphs |
| `stat-2` | Second stat (Var B) |
| `stat-3` | Third stat (Var B) |

**Var A:** Large stat dominant left. H2 + body right. 2-col.
**Var B:** 3 inline stat chips above full-width H2 + body block.

---

## GROUP 4 — SPECS / DATA

---

### `[specs-strip]` — Specs Strip

**Purpose:** Quick-scan key numbers. Appears on all product and PSEO pages.

| Field | Description |
|---|---|
| `spec-1-label` | e.g. "Max Gate Weight" |
| `spec-1-value` | e.g. "1,800 kg" |
| `spec-2-label` | e.g. "Operating Temp" |
| `spec-2-value` | e.g. "-35°C to 70°C" |
| `spec-3-label` | e.g. "Running Noise" |
| `spec-3-value` | e.g. "≤60 dB" |
| `spec-4-label` | e.g. "Output Torque" |
| `spec-4-value` | e.g. "≥150 Nm" |
| `spec-5` to `spec-6` | Var B small chips only |

**Var A:** 4 equal stat chips in a horizontal row. White bg with border.
**Var B:** 2 large primary chips (dominant specs) + 4 smaller chips below.

---

### `[specs-table]` — Specs Table

**Purpose:** Full technical specification table. Product pages.

| Field | Description |
|---|---|
| `eyebrow` | "Technical Specifications" |
| `rows` | Array of param + value pairs |

**Var A:** 2-col table. Alternating row bg. White page bg.
**Var B:** 2-col table. Dark background. White text.

---

### `[specs-compare]` — Specs Compare

**Purpose:** Side-by-side comparison.

| Field | Var A | Var B |
|---|---|---|
| `eyebrow` | Section label | Section label |
| `h2` | Comparison headline | "Open Bear vs [Brand]" |
| `columns` | 6 product columns | 2 columns: Open Bear + Competitor |
| `rows` | Spec rows | Spec rows |
| `highlight-col` | "Best For" pill last col | Open Bear column highlighted |
| `disclaimer` | — | "[Brand] specs from public data." |

**Var A:** Multi-product comparison table. Dark bg. "Best For" pill on last column.
**Var B:** 2-col side-by-side. Open Bear vs competitor. Open Bear column highlighted.

---

## GROUP 5 — FEATURES / PROOF

---

### `[features-cards]` — Features — Cards

**Purpose:** Core features section. Used on homepage, product, solutions, PSEO pages.

| Field | Description |
|---|---|
| `eyebrow` | Section label |
| `h2` | Section headline |
| `card-1-icon` | Icon name |
| `card-1-title` | 3–4 word card headline |
| `card-1-body` | 2 sentences — proof number embedded naturally in the second sentence |
| *(repeat for cards 2–4)* | |

**Var A:** 3-col card grid. Icon + H4 + 2 sentences. Light bg.
**Var B:** 4-col card grid. Icon + H4 + 1 sentence. White bg.

---

### `[features-proof-list]` — Features — Proof List

**Purpose:** Stacked proof rows. Outcome headline → proof sentence with number embedded. Product pages and PSEO pages.

| Field | Description |
|---|---|
| `eyebrow` | Section label |
| `h2` | Section headline |
| `row-1-headline` | 5–8 word outcome headline |
| `row-1-sentence` | 1 sentence — proof number embedded naturally inside the sentence |
| *(repeat for rows 2–4)* | |

**Var A:** Full-width stacked rows. Headline left, proof sentence right.
**Var B:** 2-col grid of proof rows. 4 rows split into 2 columns.

> Numbers are always embedded in the sentence — never in a separate chip field.

---

### `[features-objection]` — Features — Objection/Answer

**Purpose:** Pre-emptive objection handling. PSEO pages, product pages.

| Field | Description |
|---|---|
| `h2` | Section headline |
| `q-1` | Objection question |
| `a-1` | Answer — outcome first, spec as proof |
| `chip-1` | Spec chip |
| *(repeat for q/a 2–3)* | |

**Var A:** 3 cards. Question as card H4. Answer as body. Spec chip at base.
**Var B:** Inline list. Question bold left. Answer right. Chip at end of answer.

---

### `[features-use-cases]` — Features — Use Cases

**Purpose:** Where this product is used. Product pages.

| Field | Description |
|---|---|
| `eyebrow` | "Applications" or "Where It's Used" |
| `h2` | Section headline |
| `use-1-icon` | Icon name |
| `use-1-title` | Use case name |
| `use-1-body` | 1 line description (Var A only) |
| *(repeat for 3–4 use cases)* | |

**Var A:** 3-col cards. Icon + title + 1-line body.
**Var B:** 4-col icon grid. Icon + title only. No body.

---

### `[features-requirements]` — Features — Requirements

**Purpose:** What this sector demands + how Open Bear meets it. Application PSEO pages.

| Field | Description |
|---|---|
| `eyebrow` | e.g. "What Hospital Buyers Need" |
| `h2` | Section headline |
| `req-1-title` | Requirement name |
| `req-1-body` | How Open Bear meets it |
| `req-1-spec` | Proof spec chip |
| *(repeat for 3–4 requirements)* | |

**Var A:** 3 cards. Requirement title + body + spec chip.
**Var B:** 4 cards. Icon + requirement + spec only (no body).

---

## GROUP 6 — PRODUCTS

---

### `[product-archive]` — Product Archive

**Purpose:** Filter sidebar + product grid. Archive and category filter pages.

| Field | Description |
|---|---|
| `page-count` | "Showing X products" |
| `sort-options` | Most Popular / Price / Newest |
| `filter-categories` | Category checkboxes |
| `filter-weights` | Weight range checkboxes |
| `products` | Array of product-card sub-components |

**Var A:** Filter sidebar left (260px). 3-col product card grid right.
**Var B:** Filter sidebar left (260px). Full-width list view (product-card-list) right.

---

### `[product-strip]` — Product Card Strip

**Purpose:** Horizontal strip of product cards. Related products, B2B range.

| Field | Description |
|---|---|
| `eyebrow` | Optional label |
| `h2` | e.g. "You May Also Need" |
| `products` | 3–4 product-card sub-components |

**Var A:** 3-card horizontal strip. Full product-card layout.
**Var B:** 4-card strip. Condensed — name + 2 spec chips + link only.

---

### `[product-tabs]` — Product Detail Tabs

**Purpose:** Tabbed content container on product pages.

| Field | Description |
|---|---|
| `tab-labels` | Overview / Specs / Contents / Installation |
| `overview-content` | Body paragraphs for Overview tab |
| `specs-content` | Points to `[specs-table]` |
| `contents-list` | What's in the box items |
| `installation-steps` | Points to `[content-how-it-works]` |

**Var A:** Horizontal tab bar. Active tab = Overview. Content below tab bar.
**Var B:** Accordion stack. First item (Overview) open. Others collapsed.

---

## GROUP 7 — EDITORIAL / CONTENT

---

### `[content-how-it-works]` — How It Works

**Purpose:** Numbered educational steps + supporting image. Replaces old `section-technical`.

| Field | Description |
|---|---|
| `eyebrow` | Section label |
| `h2` | Section headline |
| `subtitle` | 1 sentence context |
| `step-1-title` | Step name |
| `step-1-body` | 2–3 sentences |
| *(repeat steps 2–4)* | |
| `image` | Factory or R&D photo |
| `image-alt` | Alt text |

**Var A:** Steps left (numbered list). Image right. Light bg.
**Var B:** Steps full-width. Icon per step. No image. Horizontal step flow.

---

### `[content-buyer-advice]` — Buyer Advice

**Purpose:** Mistake list or checklist. Advisory tone. Replaces old `section-buyer-advice`.

| Field | Description |
|---|---|
| `eyebrow` | Section label |
| `h2` | e.g. "5 Mistakes Buyers Make" |
| `subtitle` | 1 sentence |
| `mistake-1-title` | Mistake name |
| `mistake-1-body` | Explanation |
| *(repeat for 4–5 mistakes)* | |
| `image` | Advisory/product photo |

**Var A:** Photo left. Mistake list right (✕ icon + title + expandable body). White bg.
**Var B:** Mistake list full-width. 2-col grid. No photo.

---

### `[content-steps-process]` — Process Steps

**Purpose:** Linear process (quote → order → ship). Contact and B2B pages.

| Field | Description |
|---|---|
| `eyebrow` | Section label |
| `h2` | Section headline |
| `step-1-icon` | Icon |
| `step-1-name` | Step label |
| `step-1-desc` | 1 sentence |
| *(repeat steps 2–4)* | |

**Var A:** 4-step horizontal strip. Icon + step name + desc. Connector line between steps.
**Var B:** 4-step vertical list. Connecting line left edge. Step name + desc right.

---

### `[content-accordion]` — FAQ Accordion

**Purpose:** Expandable Q&A rows. FAQ page and product pages.

| Field | Description |
|---|---|
| `categories` | Tab labels for filter (optional) |
| `search-placeholder` | Search bar placeholder text (optional) |
| `q-1` | Question text |
| `a-1` | Answer text |
| *(repeat for all Q&A pairs)* | |

**Var A:** Category filter tabs above. Q&A accordion rows below. First row open.
**Var B:** Search bar above. All Q&A rows listed. First row open. No category tabs.

---

### `[content-timeline]` — Timeline

**Purpose:** Company history milestones. About page.

| Field | Description |
|---|---|
| `eyebrow` | "Our History" |
| `h2` | Section headline |
| `year-1` | Year |
| `event-1` | Milestone description |
| *(repeat for all milestones)* | |

**Var A:** Horizontal. Year nodes across top. Milestone text below each node.
**Var B:** Vertical. Alternating left/right entries. Connecting line center.

---

### `[content-blog-grid]` — Blog Grid

**Purpose:** Blog post card listing. Blog listing page.

| Field | Description |
|---|---|
| `category-filters` | Filter tab labels |
| `post-image` | Post thumbnail |
| `post-category` | Category label |
| `post-title` | Post headline |
| `post-date` | Publish date |
| `post-url` | Link |

**Var A:** 3-col card grid. Image + category + title + date.
**Var B:** Featured post full-width top + 3 smaller cards below.

---

### `[content-article]` — Blog Article

**Purpose:** Long-form blog post layout. Blog post pages.

| Field | Description |
|---|---|
| `title` | Article H1 |
| `date` | Publish date |
| `category` | Category tag |
| `featured-image` | Full-width article image |
| `body` | Article markdown content |
| `toc` | Table of contents links |

**Var A:** Sidebar TOC left (fixed). Article content right (wider column).
**Var B:** Full-width single column. No sidebar. TOC inline at top.

---

## GROUP 8 — TRUST / PROOF

---

### `[trust-stats]` — Stats Strip

**Purpose:** Key proof numbers at a glance. Replaces old `section-stats`.

| Field | Description |
|---|---|
| `stat-1-number` | e.g. "50,000" |
| `stat-1-label` | e.g. "units per year" |
| *(repeat stats 2–4)* | |

**Var A:** White bg. 4 stats. Large number + label.
**Var B:** Brand Red bg. 4 stats. White text. Large number + label.

---

### `[trust-markets]` — Markets / Regions Served

**Purpose:** Shows where Open Bear products are available. Consumer-facing. Homepage only.

| Field | Description |
|---|---|
| `eyebrow` | Section label |
| `h2` | Section headline |
| `region-1-name` | Region name — e.g. "North America" |
| `region-1-countries` | Countries — e.g. "United States · Canada" |
| `region-1-note` | 1-line buyer note — e.g. "Ships direct from Shenzhen" |
| *(repeat for regions 2–5)* | |

**Var A:** 3-col card grid. Region name + countries + shipping note. Light bg.
**Var B:** World map graphic with region labels overlaid. Regions highlighted on hover.

---

### `[trust-supply]` — Supply Terms

**Purpose:** Distributor-facing supply info. PSEO market and B2B pages. Replaces old `market-supply-strip`.

| Field | Description |
|---|---|
| `eyebrow` | "Supplying [Country] Distributors Direct From Factory" |
| `moq` | Minimum order quantity |
| `lead-time` | e.g. "15–20 working days" |
| `supply-type` | e.g. "OEM/ODM available" |
| `capacity` | "50,000 units/year" |
| `contact-name` | Gerry Yang |

**Var A:** 3-col table: MOQ · Lead Time · OEM/ODM. Light bg.
**Var B:** Horizontal chips: same data as pills. White bg.

---

### `[trust-factory]` — Factory Gallery

**Purpose:** Factory credibility photos. About and B2B pages.

| Field | Description |
|---|---|
| `eyebrow` | Section label |
| `h2` | Section headline |
| `image-1` through `image-4` | Factory photo file names |
| `caption-1` through `caption-4` | Short captions |

**Var A:** 4-image equal grid. Captions below each image.
**Var B:** 1 large image + 3 smaller images mosaic. Captions on hover.

---

### `[trust-certifications]` — Certifications Strip

**Purpose:** CE and partner certification logos. About and relevant product pages.

| Field | Description |
|---|---|
| `eyebrow` | "Certifications & Standards" |
| `cert-1-logo` | Logo image |
| `cert-1-label` | Cert name |
| `cert-1-desc` | Short description (Var B only) |

**Var A:** Horizontal logo row. Cert badges + label below each.
**Var B:** 2-col rows. Badge left. Name + description right.

---

### `[trust-testimonials]` — Testimonials

**Purpose:** Client quotes. About and solutions pages.

| Field | Description |
|---|---|
| `eyebrow` | "What Clients Say" |
| `h2` | Section headline |
| `quote-1` | Quote text |
| `name-1` | Client name |
| `role-1` | Client role/company |
| *(repeat for 2–3 quotes)* | |

**Var A:** 3-col quote cards. Quote + name + role.
**Var B:** Single large featured quote. Full-width. Name + role below.

---

### `[trust-team]` — Team Bios

**Purpose:** Leadership team introduction. About page.

| Field | Description |
|---|---|
| `eyebrow` | "Our Team" |
| `h2` | Section headline |
| `photo-1` | Headshot image |
| `name-1` | Full name |
| `role-1` | Job title |
| `bio-1` | 1-line bio (Var A) or 2–3 sentences (Var B) |

**Var A:** 4-col grid. Photo + name + role + 1-line bio.
**Var B:** 2-col rows. Photo left. Name + role + longer bio right.

---

## GROUP 9 — CTA

---

### `[cta-banner]` — CTA Banner

**Purpose:** Closing CTA on every page. Replaces old `section-cta`.

| Field | Description |
|---|---|
| `h2` | CTA headline |
| `subtext` | 1 sentence |
| `cta-primary-label` | Button text (specific action) |
| `cta-primary-url` | Button URL |
| `cta-secondary-label` | Ghost button text (Var B only) |
| `cta-secondary-url` | Ghost button URL |

**Var A:** Dark bg. Centered H2 + subtext + 1 primary button.
**Var B:** Dark bg. Centered H2 + subtext + 2 buttons (primary red + ghost white).

---

### `[cta-contact-strip]` — CTA Contact Strip

**Purpose:** Contact methods inline. Contact page and product pages.

| Field | Description |
|---|---|
| `phone` | Phone number |
| `phone-hours` | e.g. "Mon–Sat, 9am–6pm" |
| `whatsapp` | WhatsApp number + response promise |
| `email` | Email address |
| `form-fields` | Name / Email / Message (Var B only) |

**Var A:** 3-col: Phone · WhatsApp · Email. Each with icon + detail.
**Var B:** 2-col: Contact methods left. Compact form right.

---

### `[cta-form]` — Contact Form

**Purpose:** Full contact form. Contact page.

| Field | Description |
|---|---|
| `h2` | Form section headline |
| `subtext` | 1 sentence |
| `field-name` | Full Name input |
| `field-phone` | Phone Number input |
| `field-email` | Email Address input |
| `field-country` | Country dropdown |
| `field-message` | Property/requirements textarea |
| `submit-label` | Button text |
| `privacy-note` | Privacy assurance line |

**Var A:** Full form: all fields listed above.
**Var B:** Compact form: Name / Email / Message only.

---

## GROUP 10 — UTILITY

---

### `[util-search]` — Search Bar

**Purpose:** Search input for FAQ page.

| Field | Description |
|---|---|
| `placeholder` | e.g. "Search questions..." |
| `filter-labels` | Category chip labels (Var B only) |

**Var A:** Full-width centered input. Light bg.
**Var B:** Left-aligned input. Category filter chips to the right.

---

### `[util-downloads]` — Downloads Grid

**Purpose:** PDF and document download cards. Downloads page.

| Field | Description |
|---|---|
| `eyebrow` | Section label |
| `h2` | Section headline |
| `file-1-title` | Document name |
| `file-1-desc` | 1-line description |
| `file-1-format` | "PDF" |
| `file-1-size` | e.g. "2.4 MB" |
| `file-1-url` | Download URL |

**Var A:** 3-col grid. PDF icon + title + desc + download button.
**Var B:** List view. Title left. Format + size + button right.

---

### `[util-category-nav]` — Category Nav

**Purpose:** Filter/navigation tabs for archive and category pages.

| Field | Description |
|---|---|
| `tabs` | Tab labels + URLs + product count |

**Var A:** Horizontal tabs with product count badge. Active tab underlined.
**Var B:** Vertical sidebar list. Active item highlighted.

---

## Page Assembly Maps

Slice sequences for every page type. Writers and developers reference these.

---

### Homepage `/`
```
[global-announcement]
[global-nav]
[hero-home·var-a]
[trust-stats·var-b]
[features-cards·var-b]
[content-how-it-works·var-a]
[product-strip·var-b]
[trust-markets·var-a]
[cta-banner·var-b]
[global-footer]
```

### Products Archive `/gate-operators`
```
[global-announcement]
[global-nav]
[hero-page·var-a]
[util-category-nav·var-a]
[product-archive·var-a]
[content-how-it-works·var-a]
[content-buyer-advice·var-a]
[specs-compare·var-a]
[cta-banner·var-b]
[global-footer]
```

### Category Filter Page `/gate-operators/[type]`
```
[global-announcement]
[global-nav]
[hero-page·var-a]
[util-category-nav·var-a]
[product-archive·var-a]
[cta-banner·var-b]
[global-footer]
```

### Product Page `/[product-slug]`
```
[global-announcement]
[global-nav]
[hero-product·var-a]
[product-tabs·var-a]
[features-cards·var-a]
[content-how-it-works·var-b]
[features-use-cases·var-a]
[product-strip·var-a]
[cta-banner·var-b]
[global-footer]
```

### Solution Page `/[commercial|residential|industrial]-gate-operator`
```
[global-announcement]
[global-nav]
[hero-page·var-b]
[intro-split·var-a]
[features-requirements·var-a]
[features-cards·var-a]
[product-strip·var-b]
[cta-banner·var-b]
[global-footer]
```

### About Page `/about`
```
[global-announcement]
[global-nav]
[hero-page·var-a]
[intro-split·var-a]
[trust-stats·var-a]
[content-timeline·var-a]
[trust-factory·var-b]
[trust-team·var-a]
[trust-certifications·var-a]
[trust-testimonials·var-a]
[cta-banner·var-b]
[global-footer]
```

### FAQ Page `/faq`
```
[global-announcement]
[global-nav]
[hero-page·var-a]
[util-search·var-a]
[content-accordion·var-a]
[cta-contact-strip·var-a]
[global-footer]
```

### Contact Page `/contact`
```
[global-announcement]
[global-nav]
[hero-page·var-a]
[cta-form·var-a]
[content-steps-process·var-a]
[global-footer]
```

### Downloads Page `/downloads`
```
[global-announcement]
[global-nav]
[hero-page·var-a]
[util-downloads·var-a]
[cta-contact-strip·var-a]
[global-footer]
```

### Blog Listing `/blog`
```
[global-announcement]
[global-nav]
[hero-page·var-a]
[content-blog-grid·var-b]
[cta-banner·var-a]
[global-footer]
```

### Blog Post `/blog/[slug]`
```
[global-announcement]
[global-nav]
[hero-page·var-a]
[content-article·var-a]
[product-strip·var-a]
[cta-banner·var-b]
[global-footer]
```

### PSEO Market Page `/[product]-[country]`
```
[global-announcement]
[global-nav]
[hero-market·var-a]
[intro-split·var-a]
[specs-strip·var-a]
[features-cards·var-a]
[trust-supply·var-a]
[cta-banner·var-b]
[global-footer]
```

### PSEO Application Page `/[product]-for-[application]`
```
[global-announcement]
[global-nav]
[hero-page·var-b]
[intro-split·var-a]
[features-requirements·var-a]
[specs-strip·var-a]
[content-buyer-advice·var-b]
[product-strip·var-a]
[cta-banner·var-b]
[global-footer]
```

### PSEO B2B Page `/[product]-manufacturer` or `/oem-[product]`
```
[global-announcement]
[global-nav]
[hero-page·var-a]
[intro-split·var-b]
[trust-stats·var-b]
[intro-stat-lead·var-a]
[features-proof-list·var-a]
[product-strip·var-b]
[content-steps-process·var-a]
[cta-banner·var-b]
[global-footer]
```

### PSEO Alternative Page `/[brand]-gate-operator-alternative`
```
[global-announcement]
[global-nav]
[hero-page·var-a]
[intro-centered·var-a]
[specs-compare·var-b]
[features-cards·var-a]
[product-strip·var-b]
[cta-banner·var-b]
[global-footer]
```

---

## Registry Summary

| Group | Slices | Variations |
|---|---|---|
| Global | 3 | 3 |
| Hero | 4 | 8 |
| Intro | 3 | 6 |
| Specs | 3 | 6 |
| Features | 5 | 10 |
| Products | 3 | 5 |
| Editorial | 7 | 14 |
| Trust | 7 | 14 |
| CTA | 3 | 5 |
| Utility | 3 | 6 |
| **Total** | **41** | **77** |
