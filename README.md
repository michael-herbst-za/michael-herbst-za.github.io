# Michael Herbst &middot; CV

A multi-page HTML CV hosted on GitHub Pages. No build step, no JavaScript; shared styling lives in `assets/style.css`.

**Live site:** [https://michael-herbst-za.github.io](https://michael-herbst-za.github.io)

## Pages

- `index.html`: Full one-page CV — hero summary, at-a-glance stat strip, nine core skill rows, experience, learning, education, languages, contact band.
- `skills.html`: Full skills inventory across seven groups (core stack, infrastructure, security, service delivery, business and leadership, web/AI/design, soft skills).
- `experience.html`: Full professional history — current practice, the Civilsoft Systems record including public-sector tendering, earlier professional roles, and earlier roles 2014–2018.
- `learning.html`: Certifications and learning, split into in progress, applied and complete, how I learn, and planned.
- `interests.html`: Personal interests and side projects.
- `traits.html`: Capability statements, working style with evidence, and the recurring themes.
- `404.html`: Not-found page (GitHub Pages serves this automatically).

Every page shares the same header (wordmark, descriptor, button navigation with an active state) and the same footer with secondary navigation.

## Content source

Page content is derived from the canonical CV content archive (`CV_Content_Status_Index.md` and its seven companion files), regenerated 17 August 2026 after the CV suite was cut from thirteen variants to five. Where the archive and an individual CV markdown file disagree, **the archive is authoritative** — some CV markdown exports predate the August upgrade and the 17 August contact-line ruling.

Rules the site content must keep to:

- Employment title is exactly `Client Support Administrator`, with no parenthetical appended.
- No vehicle, own-transport or reliable-transport claim anywhere. The Code 08 licence and the Jeffreys Bay base may be stated.
- "Discontinued" against the B.Com. Law entry carries no reason, anywhere.
- "Self-taught" appears in the learning material only, never in a skills row or summary.
- Beginner and actively-learning languages live on `learning.html`, never in a skills row.
- Civilsoft dates are presented year-only (2019 – 2026) per the 14 August 2026 ruling.
- No reason is volunteered for any role ending.

## Design system

Aligned to the live Kouga Digital design system (kougadigital.co.za, 2026-07 revision): IBM Plex Mono (headings, labels, metadata) and IBM Plex Sans (body); ink/graphite/slate/mist/accent tokens with the WCAG-AA deep teal (`#0a7a70`) for text on light grounds; header wordmark and nav buttons; brand stripe; dark ink hero with kicker and lede; numbered section headings; card, callout, badge, stat-strip, tag and item-row components; CTA band; ink footer; skip link, visible focus states and reduced-motion support.

The 2026-08 revision adds a **semantic token layer** (`--bg`, `--surface`, `--text`, `--rule`, `--link` …) mapped from the raw brand palette. Component rules reference only the semantic tokens, so:

- `prefers-color-scheme: dark` is supported by redefining tokens alone, with no duplicated component CSS.
- `data-theme="light"` / `data-theme="dark"` on the root element overrides the system preference, so a toggle can be added later without a rewrite.
- The print stylesheet forces the tokens back to the light palette, so a dark-mode visitor still prints ink on white.

Tokens and components live in `assets/style.css`; CV-specific extensions (job cards, stat strip, print rules) are marked in their own blocks. Favicon is `assets/favicon.svg`.

## SEO and metadata

Each page carries a canonical URL, Open Graph and Twitter card metadata, and a unique description. `index.html` carries a JSON-LD `Person` graph including `worksFor`, `alumniOf` and `knowsAbout`. `sitemap.xml` and `robots.txt` are at the root.

The social preview image is `assets/og.png` (1200×630), referenced from every page as `og:image` / `twitter:image` with `twitter:card` set to `summary_large_image`. It is generated from `assets/og-source.html` — edit that file and re-render with headless Chrome or Edge:

```bash
msedge --headless=new --disable-gpu --hide-scrollbars --window-size=1200,630 --screenshot=assets/og.png --virtual-time-budget=8000 assets/og-source.html
```

Social platforms cache preview images aggressively. After replacing `og.png`, re-scrape the URL in the LinkedIn Post Inspector or Facebook Sharing Debugger to force a refresh.

## Local preview

Open `index.html` in any browser. No server or build step required.

## License

Content &copy; Michael Herbst. HTML/CSS structure reusable freely.
