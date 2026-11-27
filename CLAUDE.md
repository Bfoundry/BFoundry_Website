# BFoundry website: notes for Claude Code

Static marketing site for BFoundry (https://bfoundry.co.uk), hosted on GitHub Pages from the `main` branch root.
No build step, no framework: edit the HTML/CSS directly and push.

## Structure
- `index.html`, `fractional-executive.html`, `transformation.html`, `about.html`, `404.html`: one file per page.
- The header, footer and contact (CTA) band are **duplicated in every page**. When you change one, change all five files the same way.
- `assets/css/site.css`: all styles. Brand tokens are the CSS variables at the top. Don't add new colours.
- `assets/js/site.js`: sticky header, mobile menu, reveal-on-scroll, footer year. Keep it small and dependency-free.
- `assets/img/`: logos (SVG, from the brand pack; never edit or redraw them), headshot (`peter-480/960` as `.jpg` and `.webp`), `og-image.png`.
- `CNAME` must stay as `bfoundry.co.uk`. `.nojekyll` stops GitHub Pages from running Jekyll.
- `404.html` uses `<base href="/">` so its relative links work at any path. The other pages use plain relative links.

## Brand rules (from BFoundry-Brand-Assets v1.0)
- Colours: Midnight #14213D (text, dark bands), Midnight Tint #34497A, Copper #C8743A (accent and spark only, never small text),
  Copper Deep #9A5422 (links, buttons on light), Sand #F4EFE6 (page background), Linen #E9E2D5 (panels), Stone #5E636B (secondary text).
  On dark: #8A9BBF blocks / secondary text, #E7C9A9 copper text.
- Fonts: Space Grotesk 600 for headings, Inter for body.
- Descriptor "Build · Lead · Grow". Tagline "Forging what's next."
- Use FullColour logos on light backgrounds and Reversed on dark. Never stretch, recolour or rebuild the logo files.

## Content rules
- British English. Plain and senior: write as an experienced operator, not a marketing agency.
- Never invent clients, testimonials, results or credentials. Former employers' staff generally can't give references.
- Contact is by email only: enquiries@bfoundry.co.uk. There's no form, so no privacy notice is needed yet. Add one if a form or analytics is introduced.
- Company details: a limited company is expected around January 2027. Add the registered name, number and office to the footer when available.

## Checks before pushing
- Look at every changed page at 1366px and 390px wide. No horizontal scroll.
- Update `sitemap.xml` when you add or rename a page.
