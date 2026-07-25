# SURID Bangladesh — package-enhanced GitHub Pages application

A trust-first, accessible and responsive public-information platform for SURID Bangladesh. Version 4 expands the project into a 23-page static web application with modern UI components, structured content data, offline support and progressive package integrations.

## Live site

https://socialsarindustriesnetwork-cmd.github.io/SURID-BANGLADESH-/

## Pages v4.0

### Integrated packages

The static application loads version-pinned browser modules as progressive enhancements and keeps functional local fallbacks when a CDN package is unavailable.

- Fuse.js — fuzzy full-site search
- Chart.js — accessible dashboard and taxonomy charts
- Leaflet — interactive operational-area map
- Swiper — touch-enabled stories and media carousels
- GLightbox — keyboard-accessible media lightbox
- Tippy.js — contextual tooltips
- Motion — interface and scroll animations
- Day.js — dates and Bangladesh-local time formatting
- idb-keyval — IndexedDB persistence for bookmarks and drafts
- QRCode — shareable page QR codes

### Application features

- 23 responsive public pages
- Dashboard, map, search, tools and bookmarks workspaces
- English/Bangla controls and light/dark appearance modes
- Command search with Ctrl/Command + K
- Content bookmarks with IndexedDB/localStorage fallback
- Contact-form draft persistence
- Interactive charts, filters, accordions, tabs and metric widgets
- Operational-area map with structured location data
- Carousels, lightbox, tooltips and motion effects
- Web Share, clipboard, QR and print actions
- PWA installation controls, service worker and offline fallback
- Online/offline status feedback
- Reusable SVG icon, component and media libraries
- Responsive SEO metadata, canonical URLs, Open Graph, JSON-LD, sitemap and robots rules

### Pages

Home, About, Programmes, Impact, Stories, Partners, Reports, Media library, Component library, Dashboard, Map, Search, Tools, Bookmarks, Governance, FAQ, Contact, Donation instructions, Privacy, Safeguarding/PSEA, Accessibility, Offline fallback and custom 404.

## Static safety boundaries

- GitHub Pages does not process payments, confirm donations or issue receipts.
- Donation actions request verified instructions from SURID Bangladesh.
- The public website does not accept sensitive safeguarding/PSEA case reports through a general form or mailbox.
- Charts present programme taxonomy and interface-readiness data rather than unverified beneficiary outcomes.
- Server-backed APIs, private webhooks, AI processing and protected case-management integrations require a separate secured backend.

## Deployment

GitHub Actions reconstructs the checksummed v4 release archive, validates all pages and local references, verifies JavaScript syntax and publishes the complete `_site` artifact.

```text
8229183d03fe7307fd93043fe4d3b583b1632dcc94ef8646512a11c567d05de0  SURID-Bangladesh-Pages-v4.0.0.tar.xz
```

## Local validation and build

```bash
python3 scripts/validate_site.py
node --check assets/js/app.js
node --check assets/js/packages.js
node --check sw.js
node scripts/build.mjs
```

## Production content gate

Before treating the public site as the organization’s final authoritative record:

1. Verify office details, registrations, governance names, programme metrics and operational areas.
2. Upload only approved photographs with documented consent and licensing.
3. Publish annual reports and policies only after organizational approval.
4. Confirm the official donation channel directly with the responsible finance team.
5. Keep safeguarding reporting separate from ordinary contact and donation workflows.
