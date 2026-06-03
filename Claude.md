# CLAUDE.md — Open Bear
> Read first. These rules override all defaults. Then read Last-Session.md + Memory.md.

**Client:** Open Bear — gate automation products for homeowners and property owners. English only.
**Rule:** Write content in `.md` files only. No HTML, CSS, or JavaScript. Developer handles templates.
**Data:** All specs from `Reference/CLIENT-DATA-MAP.md` only. Never invent numbers. CE cert confirmed on Side-Mounted Swing only.
**Voice:** Second person. Benefit-first. Numbers in sentences — never as standalone labels. Max 3 sentences per paragraph.

## Session Start Order
1. Read `Last-Session.md` → find resume point and next action
2. Read `Memory.md` → confirm page status and locked decisions
3. Load task files on demand — see load order below

## On-Demand Load Order
| Task | Load these files |
|---|---|
| Starting a new page | `System/Workflow.md` + relevant `Reference/Keyword-Clusters/` file |
| Writing copy | `System/Writing-System.md` |
| Running quality checks | `System/Writing-System.md` (Section 7) |
| Verifying specs | `Reference/CLIENT-DATA-MAP.md` |
| Checking components | `System/Design.md` |
| SEO questions | `System/Writing-System.md` (Section 6) |
| Reusable blocks | `System/Reusable-Sections.md` |
| Locked decisions | `System/Decisions.md` |

## File Structure
```
Pages/core/       — home, products archive
Pages/products/   — one file per product
Pages/categories/ — sliding, swing, barrier category pages
Pages/pseo/       — programmatic SEO pages
System/           — Workflow, Writing-System, Reusable-Sections, Design, Decisions
Reference/        — CLIENT-DATA-MAP, specs, manuals, keyword clusters
```
