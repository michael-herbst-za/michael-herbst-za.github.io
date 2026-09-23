# Michael Herbst &middot; CV

A multi-page HTML CV hosted on GitHub Pages. No build step, no JavaScript; shared styling lives in `assets/style.css`.

**Live site:** [https://michael-herbst-za.github.io](https://michael-herbst-za.github.io)

## Pages

- `index.html`: Broad public CV, aligned to the active Default baseline, with summary, evidence strip, eight core capability rows, experience, learning, education, languages and contact details.
- `skills.html`: Role-focused inventory across infrastructure and identity, application support and data, service delivery, security, commercial operations, web and demonstrated working style.
- `experience.html`: Full professional history, including Kouga Digital, the Civilsoft Systems technical, application-support, account and public-sector record, and earlier roles from 2014.
- `learning.html`: Current study, held credential, applied practice and the evidence-based learning approach.
- `interests.html`: Personal interests and side projects.
- `traits.html`: Capability statements, working style with evidence, and the recurring themes.
- `404.html`: Not-found page (GitHub Pages serves this automatically).
- `documents/Michael_Herbst_CV.pdf`: Verified two-page standing public CV built from the active Default Markdown baseline.

Every page shares the same header (wordmark, descriptor, button navigation with an active state) and the same footer with secondary navigation.

## Content source

Page content is derived from the private canonical job-search content set held outside the published site: `01_LOCKED_FACTS.md` (identity, dates, titles and guardrails) and `02_EVIDENCE_BANK.md` (claim scope and reusable evidence), cross-checked against the active six-variant CV suite and its standing public copy. Site content was last reconciled against the final 23 September 2026 suite. Where the locked-facts/evidence files and a CV Markdown export disagree, **the locked-facts and evidence files are authoritative**. A CV file does not prove a claim merely by repeating it.

Rules the site content must keep to:

- Civilsoft's official title is `Client Support Administrator`; the approved descriptive qualifier is `sole IT operations and infrastructure resource`.
- No vehicle, own-transport or reliable-transport claim anywhere. The Code 08 licence and the Jeffreys Bay base may be stated.
- University studies read `Studies toward B.Eng. Computer Engineering and B.Com. Law (2015–2017), not completed`, with no reason given, anywhere.
- Civilsoft dates are presented as `December 2019–May 2026`; earlier roles use year-only dates where exact months remain unresolved.
- Civilsoft reach is `270+ South African offices, with clients in Namibia, Botswana, Eswatini, Ireland and Australia`.
- Support volume is an estimated `10 to 30 support requests a day`, never an average, derived total, Freshdesk-ticket count or SLA metric.
- `At least 15 public bodies` is an organisation count, not a bid, award or contract count. No win-rate or universal no-loss claim is used.
- Bid documentation reads `MBD, SBD, CSD and PPPFA` (SBD confirmed 21 September 2026).
- The four published account-scale examples remain distinct. The approximately 300-user consultancy is never merged with the separate 10-branch consultancy.
- Private Civilsoft client names and the two product names are not published. Public bodies may be named.
- Database work is framed as application database support and SQL report development, not software development or enterprise database engineering. SSRS and Crystal Reports are never claimed.
- No reason is volunteered for any role ending.
- The Civilsoft video-training/user-guide programme is described as proposed and approved, never as launched or as a channel.
- Kouga Digital's Google Workspace Business administration is stated as one configured, maintained and solely administered environment. Vault, migrations, Gmail routing, Shared Drives and organisational-unit management remain familiarity-level items.
- CompTIA Security+, eJPT, PNPT and OSCP remain in progress or in practical study. TechSmith Snagit is the only completed certification named.
- Civilsoft-attributed CAINE, hash-ledger, TryHackMe or named AI-tooling examples are not used without separate employer or project evidence.
- Public pages use the professional email as the default and do not expose the private address or other sensitive information.

## Design system

Aligned to the live Kouga Digital design system (kougadigital.co.za, 2026-07 revision): IBM Plex Mono (headings, labels, metadata) and IBM Plex Sans (body); ink/graphite/slate/mist/accent tokens with the WCAG-AA deep teal (`#0a7a70`) for text on light grounds; header wordmark and nav buttons; brand stripe; dark ink hero with kicker and lede; numbered section headings; card, callout, badge, stat-strip, tag and item-row components; CTA band; ink footer; skip link, visible focus states and reduced-motion support.

The 2026-08 revision adds a **semantic token layer** (`--bg`, `--surface`, `--text`, `--rule`, `--link` …) mapped from the raw brand palette. Component rules reference only the semantic tokens, so:

- `prefers-color-scheme: dark` is supported by redefining tokens alone, with no duplicated component CSS.
- `data-theme="light"` / `data-theme="dark"` on the root element overrides the system preference, so a toggle can be added later without a rewrite.
- The print stylesheet forces the tokens back to the light palette, so a dark-mode visitor still prints ink on white.

Tokens and components live in `assets/style.css`; CV-specific extensions (job cards, stat strip, print rules) are marked in their own blocks. Favicon is `assets/favicon.svg`.

## SEO and metadata

Each page carries a canonical URL, Open Graph and Twitter card metadata, and a unique description. `index.html` carries a JSON-LD `Person` graph including `worksFor`, `alumniOf` and `knowsAbout`. `sitemap.xml`, `robots.txt` and `site.webmanifest` are at the root.

GitHub Pages does not expose a repository-level response-header file, so each
HTML page carries a restrictive Content Security Policy in a `<meta>` element.
The policy allows the current JSON-LD block by SHA-256 hash. Recalculate that
hash if the structured data in `index.html` changes.

The social preview image is `assets/og.png` (1200×630), referenced from every page as `og:image` / `twitter:image` with `twitter:card` set to `summary_large_image`. It is generated from `assets/og-source.html`; edit that file and re-render with headless Chrome or Edge:

```bash
msedge --headless=new --disable-gpu --hide-scrollbars --window-size=1200,630 --screenshot=assets/og.png --virtual-time-budget=8000 assets/og-source.html
```

Social platforms cache preview images aggressively. After replacing `og.png`, re-scrape the URL in the LinkedIn Post Inspector or Facebook Sharing Debugger to force a refresh.

## Local preview

Open `index.html` in any browser. No server or build step required.

## License

Content &copy; Michael Herbst. HTML/CSS structure reusable freely.
