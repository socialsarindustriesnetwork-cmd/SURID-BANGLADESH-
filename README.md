# SURID Bangladesh — GitHub Pages public site

A trust-first, accessible and responsive public-information website for SURID Bangladesh.

## Live site

https://socialsarindustriesnetwork-cmd.github.io/SURID-BANGLADESH-/

## Pages v2.0

The polished release replaces the original single-page prototype with a structured 12-page public site and a reusable design system.

Included:

- Responsive multi-page information architecture
- English/Bangla interface controls for key public copy
- Light and dark appearance modes
- Accessible navigation, skip links, focus states and reduced-motion support
- Programme filtering and structured intervention-sector content
- Governance and registration information with verification labels
- Reports index that does not invent unavailable publications
- Safe donation-instructions request flow
- Dedicated safeguarding/PSEA, privacy and accessibility pages
- Search metadata, canonical URLs, Open Graph data, JSON-LD, sitemap and robots rules
- Progressive Web App manifest, offline fallback, service worker and custom 404 page
- Automated internal-link, document-structure and safety-language validation

## Safety boundaries

- GitHub Pages does not process payments, confirm donations or issue receipts.
- Donation actions request verified instructions from SURID Bangladesh.
- The public static site does not accept safeguarding/PSEA case reports through a general form or mailbox.
- Reports, registrations, metrics and programme claims must be verified against authorized organizational records before publication.
- The server-backed Next.js APIs, private webhooks, AI assistant and protected case-management integrations require a separate Node.js deployment.

## Deployment

The GitHub Actions workflow reconstructs the checksummed release bundle, validates all static pages and local asset references, and publishes the resulting `_site` artifact to GitHub Pages after every push to `main`.

Release checksum:

```text
7acb001318b0bda844171775d6410c1538a9b813ae0f515391f1a7b531cd45bb  SURID-Bangladesh-Pages-v2.0.0.tar.xz
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
