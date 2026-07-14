# Michael Herbst &middot; CV

A multi-page HTML CV hosted on GitHub Pages. No build step; shared styling lives in `assets/style.css`.

**Live site:** [https://michael-herbst-za.github.io](https://michael-herbst-za.github.io)

## Pages

- `index.html`: Full one-page CV (summary in the hero, then skills, experience, learning, education, languages, contact band).
- `skills.html`: 10 expanded skill categories.
- `experience.html`: Full professional history, 10 roles.
- `learning.html`: Certifications and learning: in progress, completed, planned.
- `interests.html`: Personal interests and side projects.
- `traits.html`: Working-style traits with concrete examples.

Every page shares the same header: wordmark, descriptor, and button navigation with an active state for the current page.

## Design system

Aligned to the live Kouga Digital design system (kougadigital.co.za, 2026-07 revision): IBM Plex Mono (headings, labels, metadata) and IBM Plex Sans (body); ink/graphite/slate/mist/accent tokens with the WCAG-AA deep teal (`#0a7a70`) for text on light grounds; header wordmark and nav buttons; brand stripe; dark ink hero with kicker and lede; numbered section headings; card, callout, badge and item-row components; CTA band; ink footer; skip link, visible focus states and reduced-motion support. Tokens and components live in `assets/style.css`; CV-specific extensions (job cards, print rules) are marked in their own blocks. Favicon is `assets/favicon.svg`.

## Local preview

Open `index.html` in any browser.

## License

Content &copy; Michael Herbst. HTML/CSS structure reusable freely.
