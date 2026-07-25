# SURID Bangladesh — modern GitHub Pages application

A trust-first, accessible and responsive public-information platform and design system for SURID Bangladesh.

## Live site

https://socialsarindustriesnetwork-cmd.github.io/SURID-BANGLADESH-/

## Pages v3.0

Version 3 expands the site into an 18-page static web application with a reusable modern component and asset library.

### Modern interface

- Animated gradient-mesh backgrounds and ambient visual effects
- Responsive bento grids, glass panels, cards, badges and metric widgets
- Light/dark modes and English/Bangla interface controls
- Reading progress, scroll reveals, animated counters and progress indicators
- Keyboard-accessible command search with Ctrl/Command + K
- Mobile navigation, filters, tabs, accordions and structured calls to action

### Components, charts and assets

- Reusable buttons, links, forms, navigation, alerts and feedback elements
- SVG icon sprite and branded vector illustrations
- Dedicated UI component reference page
- Downloadable media and asset library page
- Accessible chart widgets with semantic tables and descriptions
- Programme, report and resource filtering controls

### Pages

- Home
- About
- Programmes
- Impact
- Stories
- Partners
- Reports
- Media library
- Component library
- Governance
- FAQ
- Contact
- Donation instructions
- Privacy
- Safeguarding/PSEA
- Accessibility
- Offline fallback
- Custom 404

### Platform features

- Responsive SEO metadata, canonical URLs, Open Graph data and JSON-LD
- Sitemap and robots rules
- PWA manifest, service worker and offline behavior
- Automated internal-link, local-asset, document-structure and safety-language validation
- GitHub Actions deployment with bundle checksum and JavaScript syntax checks

## Safety boundaries

- GitHub Pages does not process payments, confirm donations or issue receipts.
- Donation actions request verified instructions from SURID Bangladesh.
- The public static site does not accept safeguarding/PSEA case reports through a general form or mailbox.
- Charts present programme taxonomy and interface-readiness data, not unverified beneficiary statistics.
- Reports, registrations, metrics and programme claims must be verified against authorized organizational records before publication.
- Server-backed APIs, private webhooks, AI processing and protected case-management integrations require a separate secured backend.

## Deployment

The GitHub Actions workflow reconstructs the checksummed v3 release, validates all pages and local references, verifies JavaScript syntax and publishes the resulting `_site` artifact to GitHub Pages after every push to `main`.

```text
05b4580b104d0940adb1f9dbc3b787edd27d20d021b87af494ce2057b71e0397  SURID-Bangladesh-Pages-v3.0.0.tar.xz
```

## Local validation

```bash
python3 scripts/validate_site.py
node --check assets/js/app.js
node --check sw.js
```

## Production content gate

Before treating the public site as the organization’s final authoritative record:

1. Verify office details, registrations, governance names, programme metrics and operational areas.
2. Upload only approved photographs with documented consent and licensing.
3. Publish annual reports and policies only after organizational approval.
4. Confirm the official donation channel directly with the responsible finance team.
5. Keep safeguarding reporting separate from ordinary contact and donation workflows.
