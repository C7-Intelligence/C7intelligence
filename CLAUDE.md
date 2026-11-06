# CLAUDE.md — C7 Intelligence Website

## Project Overview

Corporate presence website for **C7 Intelligence**, the AI integration & custom software development business unit. C7 Intelligence is a DBA of **Cyber7 Group LLC** (cyber7group.com), the umbrella company for three DBAs:

| DBA | Focus | Domain |
|---|---|---|
| C7 MSP | Managed IT / cybersecurity for SMBs | c7msp.com |
| C7 Infrastructure | Data center / systems integration | c7infrastructure.io |
| C7 Intelligence | AI integration / custom software dev | c7intelligence.io (this repo) |

The three DBA sites are intentionally **visually distinct**. This site must NOT drift toward the MSP look (dark ops-center, amber/teal, Space Grotesk) or the Infrastructure look (deep-blue enterprise, Sora/JetBrains Mono, blueprint). It stays distinct through its light, editorial layout and serif headings; the red accent is shared with the parent logo on purpose.

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

- **Fonts:** Archivo (headings, buttons, labels; wide `font-stretch:110%` on h1/h2 to echo the CYBER7GROUP wordmark), IBM Plex Sans (body). Fraunces/Manrope/Fira Code were dropped on 2026-11-05 because the serif-display look read as AI-generated.
- **Palette (CSS variables in `:root`), taken from the Cyber7 shield logo:** `--accent` #bf3f2f brick red (logo red is #c04030; hover `--accent-ink` #962f23), silver-grey neutrals (`--bg` #fafaf9, `--bg-2` #f1f1ef, `--line` #e1e1de, `--muted` #73737a), near-black `--ink` #1c1c1e, charcoal `--dark` #1e1e21 for the assistant card and contact panel. **No purple/violet anywhere** — the owner replaced it on 2026-11-05 because it looked AI-generated and did not match the logo.
- **Feel (2026-11 redesign):** plain, sharp, corporate. White background, one accent (the logo red), thin rules instead of boxed cards, 3–4px corners, a 3px red bar on the header, a short red rule above each h2, the parent Cyber7 Group logo in the footer. No gradients, no serif display type, no icon tiles, no check-mark rows, no "// labels", no pill buttons. Owner asked for the site not to look AI-generated; keep it that way.

## Page Sections (in order)

1. Header/nav (sticky, blurred) — shield + "C7 Intelligence", links (What we do / How it works / Why C7 / FAQ), "Get a free review" button; below 900px a `<details>` hamburger menu
2. Hero — "Your team's busywork, handled." + two-sentence lead + primary/secondary buttons + three check-mark facts (free review, demo in ~2 weeks, nationwide). Right: dark "C7 assistant · example" card styled as a chat (question bubble, four result rows that fade in, before/after panel: 2 days of data entry → done by 7am). CSS-only animation; reduced-motion shows the final state.
3. What we can do for you (`#offers`) — 8 cards in a 4-column grid: AP, AR, QuickBooks & system integrations, dashboards & reporting, company handbook assistant, Microsoft 365 assistant, quotes/proposals/emails, CRM build-outs. Footer line points custom-software requests to #contact.
4. How it works (`#how`) — 3 numbered steps: free review (30 min) → working demo (~2 weeks) → build and support (scope-dependent)
5. Why work with us (`#why`) — 3 columns: security built in (Cyber7 Group), works with what you have, straight answers
6. FAQ (`#faq`) — 5 `<details>` questions, first open by default
7. Contact (`#contact`) — dark panel: email button (subject pre-filled "Free workflow review"), phone, Louisville office address
8. Footer — brand + "A Cyber7 Group company", site links, contact + address. No LinkedIn, no sibling cross-links.

Also in the repo (added 2026-10-08, separate dark Georgia styling, aimed at AI crawlers): `ai-integration.html`, `knowledge-assistants.html`, `workflow-automation.html`, `llms.txt`, `robots.txt`, `sitemap.xml`. Leave them as they are unless asked.

SEO: meta description, canonical, Open Graph/Twitter tags, and ProfessionalService JSON-LD (with the Louisville address) in `<head>` — keep them in sync with copy/contact changes.

## Key Content Facts

- **Phone:** 502-473-5020
- **Service area:** Nationwide (work is largely remote). Owner prefers NOT to name a city (e.g. Charlotte) on the site.
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
