# CLAUDE.md — C7 Intelligence Website

## Project Overview

Corporate presence website for **C7 Intelligence**, the AI integration & custom software development business unit. C7 Intelligence is a DBA of **Cyber7 Group LLC** (cyber7group.com), the umbrella company for three DBAs:

| DBA | Focus | Domain |
|---|---|---|
| C7 MSP | Managed IT / cybersecurity for SMBs | c7msp.com |
| C7 Infrastructure | Data center / systems integration | c7infrastructure.io |
| C7 Intelligence | AI integration / custom software dev | c7intelligence.io (this repo) |

The three DBA sites are intentionally **visually distinct**. This site must NOT drift toward the MSP look (dark ops-center, amber/teal, Space Grotesk) or the Infrastructure look (deep-blue enterprise, Sora/JetBrains Mono, blueprint).

**Positioning:** pragmatic, anti-hype AI. "AI that actually ships." Small pilots, fast proof, production-grade. Honest about what AI can't do.

## Tech Stack & Hosting

- Pure static HTML/CSS — single `index.html`, no build step. JS is limited to inline onclick handlers that close the mobile menu.
- Hosted on GitHub Pages — deploy from `main` branch, root folder.
- Custom domain: c7intelligence.io (GoDaddy DNS → GitHub Pages A records + www CNAME).
- Public repo — no secrets, keys, client names, or internal info, ever.

## Repo Structure

```
index.html                      # entire site (markup + CSS in one file)
CLAUDE.md                       # this file
assets/
  c7-shield.png                 # Cyber7 shield mark (nav)
  c7group-logo-dark.png         # full parent logo w/ dark wordmark (unused currently; for light bg if needed)
  favicon.png                   # 64px shield favicon
```

## Design System (distinct from siblings)

- **Fonts:** Fraunces (serif display headings), Manrope (body/UI), Fira Code (mono labels/terminal)
- **Palette (CSS variables in `:root`):**
  - `--paper` #faf9f6, `--paper-2` #f1efe9 — warm light backgrounds (site is LIGHT overall)
  - `--carbon` #191722, `--carbon-2` #221f2e — near-black (terminal card, belief band, buttons)
  - `--violet` #6d28d9, `--violet-bright` #8b5cf6, `--magenta` #d946ef — gradient accent pair
  - `--text` #26232f, `--muted` #6b6579
- **Feel:** warm editorial light theme + violet→magenta gradients; serif display type; pill/rounded shapes (100px radius buttons, 16px card radii — softest of the three sites); radial gradient glows; a fake terminal card in the hero demoing a RAG query with citations; "// label" mono section markers.

## Page Sections (in order)

1. Header/nav (sticky, blurred) — shield + "C7 Intelligence", links, Start a Project button; below 960px a `<details>` hamburger menu (links close it via a one-line inline onclick)
2. Hero — headline "Your team's busywork, handled." ("AI that actually ships" kept as the pill tagline) + plain-English lead (any size/industry, demo in ~2 weeks) + fact row + animated "assistant" card: owner asks "What needs my attention today?" and gets a plain-English morning summary (QuickBooks invoices, AR reminders, CRM leads, flagged bills, and a before/after panel: "2 days of data entry" → "Done by 7am"). CSS-only animation; reduced-motion shows the final state
3. Trust strip — 4 items: demo in ~2 weeks, security (Cyber7 Group), works with your tools, Charlotte & nationwide
4. What We've Built (`#examples`) — 5 real project types (AP automation, AR automation, QuickBooks integrations, dashboards & reporting, CRM build-outs) + dark "Something else entirely?" card
5. Services (`#services`) — 6 cards, each with icon, plain-English description, a "For example:" box, and tech tag pills
6. Our approach (`#philosophy`) — dark band, large statement + short supporting paragraph
7. How It Works (`#process`) — 4 steps: Discover (week 1) → Demo (~2 weeks) → Build (depends on scope) → Scale (ongoing), each with a "You get" line
8. FAQ (`#faq`) — `<details>` accordion: who we work with, speed, cost, tools, data safety, location, "what if AI isn't the fit"
9. CTA (`#contact`) — violet→magenta gradient panel, email + phone buttons, "Serving Charlotte and clients nationwide"
10. Footer — brand + "A Cyber7 Group company", site links, contact. No LinkedIn, no sibling cross-links (consistent with owner's choice on the Infrastructure site).

SEO: meta description, canonical, Open Graph/Twitter tags, and ProfessionalService JSON-LD in `<head>` — keep them in sync with copy/contact changes.

## Key Content Facts

- **Phone:** 502-473-5020
- **Service area:** Core client base in the Charlotte area; clients nationwide (work is largely remote)
- **Customers:** not niche — any size, any industry
- **Primary CTA:** free 30-minute workflow review (owner-approved offer) — used in nav, hero, examples card, process step 1, FAQ, and contact panel
- **Timeline claim:** working demo in ~2 weeks for most projects; full build depends on scope. No pricing on site (quoted per project)
- **Email:** info@c7intelligence.io (mailbox confirmed working by owner, 2026-09-24)
- Service credibility draws on real experience: Azure AI Foundry, Azure AI Search, SharePoint indexing, embeddings/RAG builds, RPA (Playwright), infrastructure background
- Tone rules: anti-hype, concrete, honest ("we'll tell you honestly why it won't work"). Avoid buzzword salads and inflated AI claims.

## Known Issues / TODO

- No case studies yet — a case-study section can be added once shippable references exist (mirror the Infrastructure site's pattern if desired, restyled to this design).
- No imagery/video — terminal card serves as the hero visual. Real product screenshots could be added later.
- Consider a DBA-specific shield color variant if per-brand marks are created.

## Conventions for Edits

- Keep everything in the single `index.html`.
- Maintain the warm-light + violet/magenta identity and Fraunces/Manrope/Fira Code type stack.
- Keep total page weight low; compress any added media (<1MB per asset).
- Footer must retain "A Cyber7 Group company" attribution. Do not add LinkedIn or sibling-site links unless the owner asks.
- Keep copy anti-hype: no "revolutionary," no "cutting-edge," no unverifiable claims.
