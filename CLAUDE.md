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

- Pure static HTML/CSS — single `index.html`, no build step, no JS beyond a CSS cursor-blink animation.
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

1. Header/nav (sticky, blurred) — shield + "C7 Intelligence", links, Start a Project button
2. Hero — "AI that actually ships." + terminal card showing a grounded RAG query answering with cited sources
3. What We Build (`#services`) — 6 cards: AI Integration, RAG & Knowledge Systems, Custom Software Development, Workflow Automation, AI Readiness & Infrastructure, Advisory & Roadmapping (each with tech tag pills)
4. Philosophy (`#philosophy`) — dark band, single large statement: grounded in your data / secured like production / boring enough to trust
5. Process (`#process`) — 3 steps: Discover → Prove (pilot in weeks) → Ship & Scale
6. CTA (`#contact`) — violet→magenta gradient panel, email + phone buttons
7. Footer — brand + "A Cyber7 Group company", site links, contact. No LinkedIn, no sibling cross-links (consistent with owner's choice on the Infrastructure site).

## Key Content Facts

- **Phone:** 502-473-5020
- **Email:** info@c7intelligence.io  ← NOTE: mailbox may not exist yet; verify/update once mail is set up for this domain
- Service credibility draws on real experience: Azure AI Foundry, Azure AI Search, SharePoint indexing, embeddings/RAG builds, RPA (Playwright), infrastructure background
- Tone rules: anti-hype, concrete, honest ("we'll tell you honestly why it won't work"). Avoid buzzword salads and inflated AI claims.

## Known Issues / TODO

- Verify `info@c7intelligence.io` mailbox exists before launch.
- No case studies yet — a case-study section can be added once shippable references exist (mirror the Infrastructure site's pattern if desired, restyled to this design).
- No imagery/video — terminal card serves as the hero visual. Real product screenshots could be added later.
- Consider a DBA-specific shield color variant if per-brand marks are created.

## Conventions for Edits

- Keep everything in the single `index.html`.
- Maintain the warm-light + violet/magenta identity and Fraunces/Manrope/Fira Code type stack.
- Keep total page weight low; compress any added media (<1MB per asset).
- Footer must retain "A Cyber7 Group company" attribution. Do not add LinkedIn or sibling-site links unless the owner asks.
- Keep copy anti-hype: no "revolutionary," no "cutting-edge," no unverifiable claims.
