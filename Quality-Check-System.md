# Quality Check System — Open Bear Copywriting

> This document defines exactly HOW every quality check is executed.
> Not what to look for — how to test it. Every check has a method, a pass condition, and a fail condition.
> Read this before running any quality check on any page.

---

## Overview — Two-Tier Quality System

| Tier | When | Purpose |
|---|---|---|
| **Tier 1 — Section Check** | After each section is written | Catch failures early. Fix before they accumulate. |
| **Tier 2 — Three-Pass System** | After full page is compiled | Refine a page that is already clean. Not rescue work. |

---

## TIER 1 — Section-Level Quality Check

Run this on every section immediately after writing it. Before showing it to the user. Before moving to the next section.

There are five checks. Each one has a specific test method. Not a general impression — a specific test.

---

### Check 1 — Banned Phrase Scan

**What it is:** A mechanical search for words and phrases that make copy sound AI-generated, generic, or salesy. These phrases are banned because they carry no information. They signal to the reader that nobody has thought carefully about what they are saying.

**How to run it:**

Read through the section and search for every item on this list. Read word by word if needed — do not skim.

**Full banned list:**

| Category | Banned words and phrases |
|---|---|
| AI filler adjectives | cutting-edge, state-of-the-art, world-class, next-generation, innovative, revolutionary, game-changing, industry-leading, advanced, powerful (alone, without a number), high quality, premium (alone), robust, seamless, seamlessly |
| Corporate verbs | leverage, elevate, empower, revolutionize, transform, optimize, streamline, unlock, harness, pioneer |
| Vague descriptors | reliable (without a spec number), durable (without a cycle count), versatile, flexible, comprehensive, holistic, end-to-end, tailor-made, bespoke |
| Opening clichés | In today's world, In the modern era, In an ever-changing landscape, In today's fast-paced, As technology evolves |
| Soft openers | Whether you're looking for, Look no further, If you're searching for, The good news is |
| False authority | Our team of experts, Dedicated team, Passionate professionals, Years of experience (without a number), Trusted by thousands |
| Weak CTAs | Learn more, Click here, Find out more, Discover more, Read more, See more |
| Filler phrases | Don't hesitate to contact us, Feel free to reach out, We would love to hear from you |
| Brand chest-beating | At Open Bear, we believe, We are proud to, We are committed to, Our mission is to |
| Emotional manipulation | Peace of mind (replace with a specific outcome), Don't miss out, Act now, Limited time |

**Pass condition:** Zero matches found.

**Fail condition:** Any match found. Replace immediately before moving forward. Do not adjust — remove or rewrite the sentence entirely.

**Replacement rule:** When a banned phrase is found, the replacement must carry a real number or a real outcome. "Reliable" becomes "runs for 10,000,000 cycles before the motor needs service." "Advanced motor" becomes "DC24V servo motor — the same voltage class used in commercial access control." The word is not the problem — the absence of information behind it is the problem.

---

### Check 2 — Claims Verification

**What it is:** Every factual claim in the section must be traceable to a source. The source is `CLIENT-DATA-MAP.md` or the product specification PDFs in `product specification/`. If a claim cannot be traced, it is removed.

**Why this matters:** Unverified claims erode trust. A homeowner who buys based on "handles heavy gates" and then finds the gate operator fails at 800 kg has a legitimate complaint. A claim in copy is a promise. Every promise must be backed.

**How to run it:**

Go through the section sentence by sentence. For every sentence that makes a factual claim, answer these three questions:

1. **Is there a number in this sentence?**
   - If yes — find that exact number in `CLIENT-DATA-MAP.md` or the spec sheet. If it is not there, remove the number and the claim.
   - If no — ask whether the sentence needs a number. If it is making a performance claim without one (e.g. "handles heavy gates"), it fails.

2. **Is there a product capability claim?** (e.g. "works in extreme temperatures", "compatible with smart home systems", "solar compatible")
   - Trace it. Open `CLIENT-DATA-MAP.md` and find the line that confirms this. If confirmed, the claim stands. If not found, remove it.

3. **Is there a company claim?** (e.g. "factory-direct", "ships complete", "50,000 units per year capacity")
   - Same rule — find it in the client data. If it is there, it stands. If not, remove it.

**The specificity ladder — apply this to every claim that passes verification:**

```
Level 1 (fails): "Handles heavy gates"
Level 2 (fails): "Handles very heavy gates"
Level 3 (passes): "Handles gates up to 1,800 kg"
Level 4 (best): "Handles gates up to 1,800 kg — the full range of farm, estate, and industrial gate weights"
```

Every verified claim should reach Level 3 minimum. Level 4 is the target — the number plus the real-world context that makes it meaningful to a homeowner.

**Pass condition:** Every factual claim traced to source data. Every performance claim has a specific number at Level 3 or higher.

**Fail condition:** Any claim that cannot be sourced, or any performance claim sitting at Level 1 or 2.

**Special cases:**
- Certifications — only claim CE certification for the Side-Mounted Swing model. No other model has confirmed certification. Do not write "certified" for any other product.
- Years in business — do not write "15+ years". Open Bear was founded 2015, gate automation began 2018. Do not use unverified founding or experience claims.
- Installation count — do not write any install count figures. Unverified. Use factory capacity instead: 50,000 units per year.

---

### Check 3 — Consumer Readability Test

**What it is:** A structured method for verifying that the section is readable by a homeowner with no technical background. Not an impression — a test with specific failure signals.

**Why this matters:** The audience is end consumers — homeowners, property managers, rural owners. They are not gate automation engineers. They do not know what "duty cycle" means. They do not know the difference between a servo motor and a brushless motor. If the copy assumes knowledge they do not have, it loses them. A lost reader does not become a buyer.

**How to run it — the Four Tests:**

**Test A — The stranger test**
Read the section aloud as if explaining it to a neighbour who has never thought about gate openers. Every time you reach a word or phrase you would need to explain, it is a failure. Mark it.

Common failure words in gate automation copy:
- Duty cycle → explain as "how many times the gate opens and closes per day before the motor needs to cool down"
- Torque → explain as "the pulling force that moves the gate"
- Servo motor → explain as "a motor that adjusts its speed and force to match the gate's weight, rather than running at one fixed power"
- Encoder → explain or remove
- IP rating → explain as "the weather protection level — IPX4 means protected against rain from any direction"
- Limit switch → explain or remove in consumer copy

Rule: Technical terms are allowed if they are explained in the same sentence. They are not allowed if the reader must already know what they mean.

**Test B — The sentence length test**
Count the words in every sentence. Flag any sentence over 25 words. These are almost always carrying two ideas that should be split.

Target distribution per section:
- 30% short sentences: 5–10 words
- 50% medium sentences: 11–20 words
- 20% longer sentences: 21–25 words (maximum)
- 0% sentences over 25 words

**Test C — The passive voice test**
Identify every sentence where the subject is receiving the action rather than doing it.

Passive (fails): "The gate is opened by the motor using DC24V power."
Active (passes): "The DC24V motor opens the gate — quietly and without jolt."

Passive (fails): "Obstacle detection is included as standard."
Active (passes): "Obstacle detection stops the gate the moment it contacts anything in its path."

Every passive construction must be rewritten in active voice.

**Test D — The jargon ratio test**
Count the number of technical terms in the section. Count the number that are explained inline. The ratio of unexplained to explained must be zero. Every technical term that appears must be explained in the same sentence or the sentence immediately following.

**Pass condition:** All four tests pass. Zero flagged sentences.

**Fail condition:** Any sentence fails any single test. Fix before moving forward.

---

### Check 4 — Benefit-First Test

**What it is:** A structural test that verifies every sentence leads with what the buyer gains, not what the product has. This is the single most common failure in product copy. Feature-first writing is how engineers describe products. Benefit-first writing is how buyers decide to purchase them.

**Why this matters:** A homeowner does not care that the motor is DC24V. They care that their children cannot get an electric shock from touching it. The product feature is the same. The writing angle is completely different. Benefit-first writing makes that translation automatic.

**How to run it — the FAB Test:**

For every sentence that describes a product feature, apply the FAB chain:

```
Feature: What the product has
Advantage: What that feature does differently or better
Benefit: What the buyer experiences as a result
```

The sentence must lead with the Benefit. The Feature supports it. The Advantage connects them.

**Example applied:**

| FAB Level | Sentence |
|---|---|
| Feature only (fails) | "The operator includes a DC24V servo motor." |
| Feature + Advantage (partial) | "The DC24V servo motor runs below the electric shock threshold." |
| Benefit-first (passes) | "Safe to touch — even mid-cycle. The DC24V motor runs well below the voltage where electric shock becomes a risk." |

**The "So what?" method:**

Read every sentence and ask "So what?" after it. If the answer reveals important information that is not already in the sentence, the sentence is feature-first. Add the "so what" to the sentence.

Example:
- "The motor operates on 24V DC." — So what? → "It runs below the electric shock threshold." — So what? → "Your family and pets are safe around it even when the gate is moving."
- Final sentence: "The motor runs on 24V DC — below the electric shock threshold, so the gate is safe around children and pets even when it is in motion."

**The "which means that" bridge:**

When a feature-first sentence is found, connect it to its benefit using "which means that":

- "DC24V power system" + "which means that" = "which means that even direct contact during operation carries no electric shock risk"

Then rewrite the sentence benefit-first, dropping the bridge phrase:

- "No electric shock risk — the 24V power system sits well below the threshold where contact becomes dangerous."

**Pass condition:** Every sentence opens with the outcome or experience the buyer gets. Features appear as supporting evidence, never as the lead.

**Fail condition:** Any sentence opens with a product attribute before the buyer benefit. Rewrite using FAB or the "so what?" method before moving forward.

---

### Check 5 — CTA Specificity Test

**What it is:** A test for every call to action in the section. CTAs are the conversion mechanism of the page. A weak CTA tells the reader there is something to click. A strong CTA tells the reader exactly what they get when they click it and why they should do it now.

**Why this matters:** "Learn more" tells a homeowner nothing. They are already on the page — they came to learn more. The CTA must advance their journey, not repeat where they already are.

**How to run it — three-part test:**

**Part 1 — The substitution test**
Replace the CTA text with "Click here." If the meaning of the page does not change, the CTA fails. A passing CTA carries specific information that "Click here" cannot replace.

Fails substitution test:
- "Learn more" — click here means the same thing
- "Find out more" — click here means the same thing
- "Discover our range" — click here means almost the same thing

Passes substitution test:
- "Download the sliding gate operator spec sheet" — click here does not mean this
- "Compare all six models side by side" — click here does not mean this
- "Get a quote for your gate size" — click here does not mean this

**Part 2 — The value exchange test**
A CTA must answer: what does the reader get when they click? If the CTA does not clearly state what the reader receives, it fails.

Format that passes: **[Action verb] + [specific thing the reader gets]**

Examples:
- "Download the spec sheet" → action: download / thing: spec sheet ✅
- "Compare all models" → action: compare / thing: all models ✅
- "Get your gate size quote" → action: get / thing: a quote specific to their gate ✅
- "Request a distributor catalogue" → action: request / thing: distributor catalogue ✅

**Part 3 — The section alignment test**
The CTA must match what the section was about. A CTA that sends the reader somewhere unrelated to the section topic breaks trust.

- Hero section about gate safety → CTA: "Find the right opener for your gate" ✅
- Feature section about motor specs → CTA: "Download the full motor specification sheet" ✅
- Feature section about motor specs → CTA: "Browse our product range" ❌ (too vague, misaligned)

**Sections that do not require a CTA:**
- Technical spec tables (developer reference sections)
- Internal navigation sections (breadcrumbs, related products)
- Legal / compliance notes

Every other section requires one CTA. One — not two. Two CTAs create decision paralysis.

**Pass condition:** CTA passes all three parts of the test. Action verb present. Specific value stated. Aligned to section content.

**Fail condition:** Fails any single part. Rewrite before moving forward.

---

## TIER 2 — Three-Pass System

Run after the full page is compiled. The section checks above mean the page arriving here is already clean. The three passes are not rescue work — they are refinement. The goal is to make a good page excellent.

---

### Pass A — Quality Audit

**Purpose:** Read the full compiled page and produce an annotated failure list. Do not rewrite yet. Find everything, then score.

**How to run it:**

Read the full page from top to bottom in one pass. Mark every sentence that fails any of the five Tier 1 checks (banned phrases, unverified claims, consumer readability, benefit-first, CTA). Add any new failures you find at the full-page level that section-level reading missed.

Then score each of the six dimensions below using the failure count method — not impression.

**Scoring method — failure count to score:**

| Failures found in dimension | Score |
|---|---|
| 0 | 10/10 |
| 1 | 9/10 |
| 2–3 | 7–8/10 |
| 4–6 | 5–6/10 |
| 7–10 | 3–4/10 |
| 11+ | 1–2/10 |

**The six dimensions:**

**1. Clarity**
Test: Every sentence passes the stranger test (Check 3, Test A). No unexplained technical terms. No sentence over 25 words.
Count: Number of sentences with unexplained jargon + number of sentences over 25 words.

**2. Specificity**
Test: Every claim passes the claims verification (Check 2). Every performance claim reaches Level 3 on the specificity ladder.
Count: Number of unverified claims + number of Level 1 or Level 2 claims.

**3. Human Voice**
Test: Zero banned phrases (Check 1). No two consecutive sentences start with the same word. No sentence reads like it was assembled from parts rather than spoken.
Count: Number of banned phrases + number of consecutive same-word sentence starts + number of sentences that read as assembled rather than spoken.

The "assembled" test: Read the sentence aloud. If it sounds like it was built from a template, it was. Signs:
- Subject → verb → object with no variation
- Sentences that follow identical grammatical structure three or more times in a row
- Sentences that use the same level of formality throughout with no rhythm variation

**4. Consumer Fit**
Test: The page is written for a homeowner, not a technical buyer. Every section passes the FAB test (Check 4). No section assumes prior knowledge of gate automation.
Count: Number of feature-first sentences + number of sections with unexplained industry assumptions.

**5. Benefit-First**
Test: Every sentence leads with buyer outcome. Zero sentences open with a product attribute as the primary subject.
Count: Number of sentences where the product feature appears before the buyer benefit.

**6. Originality**
Test: Sentence structures vary throughout the page. No three consecutive sentences follow the same grammatical pattern. No phrase appears more than once across the page.
Count: Number of repeated phrases + number of structural repetition clusters (3+ sentences in same pattern).

**Pass A output — use this exact format:**

```
PASS A AUDIT — [Page Name]

Clarity: [X]/10 — [one line describing the main failure type found]
Specificity: [X]/10 — [one line describing the main failure type found]
Human Voice: [X]/10 — [one line describing the main failure type found]
Consumer Fit: [X]/10 — [one line describing the main failure type found]
Benefit-First: [X]/10 — [one line describing the main failure type found]
Originality: [X]/10 — [one line describing the main failure type found]

Overall: [average]/10

Failure list for Pass B:
- [Section name]: [exact sentence or phrase] — [which check it fails] — [what to do]
- [Section name]: [exact sentence or phrase] — [which check it fails] — [what to do]
[... full list of every failure found]
```

Every item on the failure list must include the exact sentence, the check it failed, and the instruction for fixing it. Vague notes like "rewrite this section" are not allowed. The note must say what specifically is wrong and what direction the fix should take.

---

### Pass B — Surgical Rewrite

**Purpose:** Fix every item on the Pass A failure list. Only those items. Do not rewrite sentences that passed. Do not improve things that are not broken. This is surgical — targeted cuts and replacements, not a wholesale rewrite.

**How to run it:**

Work through the Pass A failure list item by item. For each:

1. Open the section containing the failure
2. Find the exact sentence
3. Apply the fix instruction from Pass A
4. Verify the fix does not introduce a new failure (banned phrase introduced in the replacement, claim now unverified, etc.)
5. Move to the next item

**Eight rewriting rules — apply to every fix:**

**Rule 1 — Sentence start variation**
No two consecutive sentences may start with the same word. After fixing a sentence, check the sentence before it and the sentence after it. If any start with the same word, vary one.

Wrong: "The motor handles gates up to 1,800 kg. The motor operates on DC24V power."
Right: "The motor handles gates up to 1,800 kg. DC24V power keeps it running quietly at any load."

**Rule 2 — Number grounding**
Every claim that was vague in Pass A must now include a specific number. Use `CLIENT-DATA-MAP.md` as the source. Do not estimate or approximate.

Wrong: "handles heavy gates" → Right: "handles gates up to 1,800 kg"
Wrong: "long-lasting motor" → Right: "rated for 10,000,000 operating cycles"
Wrong: "works in all climates" → Right: "operates from -35°C to 70°C"

**Rule 3 — Reading level discipline**
After rewriting a sentence, count its words. If over 25, split it. If it contains two ideas connected by "and" or "but", test whether they work better as two sentences. Usually they do.

Wrong: "The DC24V servo motor delivers 650 Nm of torque and operates below the electric shock threshold, making it safe for families and pets while still handling the heaviest residential and light commercial gates available."
Right: "650 Nm of torque moves the heaviest residential gates without strain. The DC24V system keeps it safe — operating well below the voltage where electric shock becomes a risk."

**Rule 4 — Active voice**
Every passive construction must be rewritten active. Find the agent (who or what is doing the action) and make it the subject.

Passive: "The gate is stopped automatically when an obstacle is detected."
Active: "The obstacle sensor stops the gate the instant it detects contact — no manual override needed."

**Rule 5 — One idea per sentence**
If a sentence contains a comma separating two independent clauses, test whether each clause is stronger alone. In most cases it is.

Wrong: "The motor is quiet, which makes it ideal for residential areas where noise regulations apply."
Right: "The motor runs at just 60 dB — below the level most residential noise regulations allow."

**Rule 6 — Sentence rhythm**
After completing all fixes in a section, read the section aloud. Count the beats. Short sentences punch. Long sentences explain. The rhythm should feel like a person talking — not a machine listing. If three or more sentences in a row feel the same length, vary one.

**Rule 7 — Buyer language**
Use the exact words buyers use. Do not rephrase them into "better" words.

They say: "gate opener" — not "access automation system"
They say: "opens and closes" — not "cycles"
They say: "heavy gate" — not "high load capacity application"
They say: "works in cold weather" — not "performs in low ambient temperature conditions"

When in doubt, write the way you would explain it to a neighbour.

**Rule 8 — No manufactured urgency**
Do not use urgency triggers in consumer copy for Open Bear. Homeowners researching gate openers are not making impulse decisions. They are comparing options over days or weeks. Urgency language ("limited stock", "act now", "order today") reads as manipulation to this buyer. It damages trust. Remove all urgency language without replacement.

**Pass B output:**

After completing all fixes, produce a short summary:

```
PASS B COMPLETE — [Page Name]

Items fixed: [count]
Sections touched: [list of section names]
Items that could not be fixed without new client data: [list, if any]
```

If any failure from Pass A could not be fixed because the required spec data does not exist in `CLIENT-DATA-MAP.md`, flag it here. Do not invent data. Remove the claim and note what data is needed from the client to restore it.

---

### Pass C — Consumer Marketing Review

**Purpose:** Read the page as a homeowner who has never heard of Open Bear. This is not a copy check — it is a conversion check. The question is not "is this well written?" The question is "would this page make me confident enough to contact Open Bear?"

**How to run it — the six tests:**

**Test 1 — The 3-second headline test**
Open each section and read only the headline. Give it 3 seconds — the amount of time a skimming reader spends on a headline before deciding to read or scroll.

Ask: Does this headline tell me — in those 3 seconds — something I want to know more about?

Passing headlines make a promise or state an outcome:
- "Your Gate. Your Phone. Anywhere." — passes (outcome: remote control from anywhere)
- "Silent at Every Speed." — passes (outcome: no noise)
- "Our Motor Technology" — fails (no outcome, no promise, no reason to keep reading)
- "Product Features" — fails (describes the section, does not sell the section)

Every failing headline must be rewritten as an outcome statement of 5–8 words.

**Test 2 — The first 10 words test**
Read only the first 10 words of each section's body copy (not the headline — the first sentence of the paragraph below it). Ask: do these 10 words tell me what I gain from this section?

If the first 10 words introduce the product, the company, or a feature — they fail. The first 10 words must introduce what the buyer receives.

Fails: "Open Bear's DC24V servo motor technology represents a significant advancement..."
Passes: "Your children and pets are safe around this gate — even mid-cycle..."

**Test 3 — The objection coverage test**
A homeowner buying a gate opener has these objections. Check the full page against this list. Every objection must be addressed somewhere on the page — directly, with a specific answer backed by a number.

| Objection | Must appear somewhere on page |
|---|---|
| "Will someone get an electric shock?" | DC24V — below shock threshold |
| "Will it handle my gate?" | Weight capacity in kg |
| "Will it work in my climate?" | Temperature range: -35°C to 70°C |
| "What if the power cuts out?" | Battery backup standard |
| "Is it too loud?" | dB rating — compared to familiar reference |
| "Can I control it from my phone?" | App/Bluetooth/WiFi compatibility |
| "Is it hard to install?" | Ships complete — or confirm installer support |
| "Is it safe for children and pets?" | Obstacle detection + voltage safety |

If any objection from this list has no answer on the page, the page fails Test 3. Add a section or expand an existing one to address the gap.

**Test 4 — The CTA journey test**
Read the page end to end and map every CTA. Ask: does each CTA advance the reader toward a decision, or does it loop them back to where they already are?

A passing CTA journey looks like this:
1. Hero CTA → find the right model (moves them to product selection)
2. Features CTA → download the spec sheet (moves them to verification)
3. Closing CTA → get a quote (moves them to conversion)

Each CTA should move the reader one step closer to contact or purchase. If two CTAs on the same page send the reader to the same destination, remove one.

**Test 5 — The differentiation test**
Read the page and answer this question from the perspective of a homeowner who has also looked at NICE: what does this page tell me that NICE's page does not?

Open Bear's differentiators — at least two must be explicitly stated on every product page:
- DC24V safety voltage — no electric shock risk (NICE uses AC in some models)
- Servo motor technology — smooth, load-aware operation
- Factory-direct from manufacturer — no middleman pricing
- 50,000 units/year capacity — proven scale, not a small operation
- Temperature range -35°C to 70°C — wider than most residential competitors

If the page reads as if it could be any gate opener brand, it fails. Specificity is differentiation.

**Test 6 — The read-aloud test**
Read the full page aloud from start to finish. Mark every moment where:
- You hesitate because the sentence does not flow naturally
- You read a sentence twice because the meaning is unclear on first pass
- You reach a phrase that sounds like it was written, not spoken

Every marked moment is a rewrite. A page that sounds like a person wrote it builds trust. A page that sounds like a machine assembled it creates distance.

**AI-Written Score — how to assess it:**

The AI-Written score is a judgement of how "generated" the copy feels. It is not a tool result — it is an informed reader's assessment based on these signals:

High AI-written signals (each present = +5% to the score):
- Three or more sentences in a row following the same subject-verb-object structure
- Any sentence containing "not only... but also"
- Any paragraph that builds systematically from general to specific without variation
- Vocabulary that is technically correct but not how a person would naturally say it
- Perfect parallelism in bullet points (every bullet the same length, same structure)
- Transitions like "Furthermore", "Additionally", "Moreover", "In conclusion"
- Any CTA that could apply to any product on any website

Low AI-written signals (each present = -5% from the score):
- Sentence fragments used intentionally for punch
- A sentence that starts with "And" or "But"
- A specific number that is not a round number (e.g. "1,250 kg" rather than "1,200 kg")
- A direct address to the reader mid-paragraph ("If your gate weighs over 800 kg, this is the model.")
- An unexpected analogy ("60 dB — quieter than a normal conversation")
- A rhetorical question that the next sentence answers

**Target: 15% or below.**

If the score is above 15%: identify the three highest-scoring AI-signal sentences. Rewrite those three first. Re-assess. Repeat until the score reaches 15% or below. Maximum two full loops. If still above 15% after two loops, present the remaining high-signal sentences to the user with a note on what data or direction is needed to resolve them.

**Pass C output — use this exact format:**

```
PASS C REVIEW — [Page Name]

3-second headline test: [pass/fail] — [note on any failing headlines]
First 10 words test: [pass/fail] — [note on any failing sections]
Objection coverage test: [pass/fail] — [list any uncovered objections]
CTA journey test: [pass/fail] — [note on any CTA gaps or loops]
Differentiation test: [pass/fail] — [list which differentiators appear and which are missing]
Read-aloud test: [pass/fail] — [list any sentences that failed]

Final changes made:
- [Exact change made and where]
- [Exact change made and where]

AI-Written Score: [X]% — [list the specific sentences that drove the score up, if any remain]

Page status: [READY FOR CHECKLIST / NEEDS FURTHER WORK]
```

---

## Quality Score Reference

| Score | Meaning | Action |
|---|---|---|
| 9–10/10 per dimension | Excellent | Pass B makes minimal changes |
| 7–8/10 per dimension | Good | Pass B fixes specific flagged items |
| 5–6/10 per dimension | Needs work | Pass B does significant rewriting in this dimension |
| Below 5/10 any dimension | Serious problem | Stop. Identify root cause. May require rewriting the section from scratch. |
| AI-Written score ≤15% | Target achieved | Page is ready |
| AI-Written score 16–25% | Needs Pass B loop | Identify top 3 AI-signal sentences, rewrite, reassess |
| AI-Written score above 25% | Significant problem | The section was likely written feature-first or without a clear buyer in mind. Rewrite the worst-scoring section completely. |

---

## Common Failure Patterns — Quick Reference

These are the most common failures found in gate automation copy. Check for these specifically on every page.

| Pattern | Example | Fix |
|---|---|---|
| Feature lead | "The operator includes a DC24V motor" | Rewrite benefit-first: "Safe to touch — the 24V motor runs below the shock threshold" |
| Vague weight claim | "Handles heavy gates" | Verify and specify: "Handles gates up to 1,800 kg" |
| Unanchored temperature claim | "Works in all climates" | Specify: "Operates from -35°C to 70°C" |
| Safety claim without voltage | "Safe for families" | Anchor: "Safe to touch — DC24V runs well below the electric shock threshold" |
| Noise claim without dB | "Quiet operation" | Specify: "Runs at just 60 dB — quieter than a normal conversation" |
| Speed claim without number | "Fast cycle times" | Specify: "Opens a 4-metre gate in under 15 seconds" (verify from spec) |
| Compatibility claim without model | "Smart home compatible" | Specify: "Works with Bluetooth and WiFi on the side-mounted model — compatible with most smart home platforms" |
| Generic CTA | "Contact us to learn more" | Rewrite: "Request a quote for your gate size and weight" |
| Unverified cert claim | "Certified and compliant" | Remove unless confirmed. Only Side-Mounted Swing has confirmed CE certification. |

---

## How the Two Tiers Work Together

```
SECTION WRITTEN
     ↓
Tier 1 — Five section checks run immediately
     ↓ (all pass)
USER APPROVES SECTION
     ↓
[repeat for all sections]
     ↓
FULL PAGE COMPILED
     ↓
Consumer journey read — does the page flow as a homeowner would read it?
     ↓
Tier 2 — Pass A: full-page audit, failure list built
     ↓
Tier 2 — Pass B: surgical fixes from failure list only
     ↓
Tier 2 — Pass C: conversion review, AI score assessed
     ↓
AI score ≤15%? → Page checklist
AI score >15%? → Identify top 3 AI-signal sentences → rewrite → reassess (max 2 loops)
```

The Tier 1 checks ensure the page arriving at Pass A is already clean. Pass A finds what Tier 1 missed at the full-page level. Pass B fixes it surgically. Pass C verifies it converts. The system only works if both tiers run — skipping Tier 1 turns the three passes into rescue work.
