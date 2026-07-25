# SURID Bangladesh Web Platform

Production-oriented Next.js platform for SURID Bangladesh. The project includes the public organization website, verified server-backed contact workflows, a fail-safe donation-instructions request, an isolated safeguarding integration point, and an optional Gemini information assistant.

## Safety model

- A form displays success only after its configured HTTPS webhook confirms delivery.
- Donation submission is a **request for verified instructions**, not a payment transaction or receipt.
- PSEA/safeguarding reporting is disabled by default and cannot share the ordinary forms endpoint.
- The AI assistant does not accept safeguarding reports or confirm donations.
- API routes validate payloads, apply request limits, bound message size, and return generic public errors.

## Requirements

- Node.js 22.6 or newer
- npm 10 or newer
- HTTPS webhook receivers for any enabled submission workflows
- Optional Gemini API key for the public information assistant

## Local setup

```bash
cp .env.example .env.local
npm install
npm run dev
```

Open `http://localhost:3000`.

## Required environment variables

See `.env.example` for the complete list.

At minimum, configure:

```env
NEXT_PUBLIC_SITE_URL="https://suridbangladesh.com"
FORMS_WEBHOOK_URL="https://your-secure-endpoint.example/forms"
FORMS_WEBHOOK_SECRET="replace-with-a-long-random-secret"
DONATION_WEBHOOK_URL="https://your-secure-endpoint.example/donations"
DONATION_WEBHOOK_SECRET="replace-with-a-different-long-secret"
```

Keep safeguarding disabled until an isolated protected case-management endpoint is operational:

```env
NEXT_PUBLIC_PSEA_FORM_ENABLED="false"
PSEA_WEBHOOK_URL=""
PSEA_WEBHOOK_SECRET=""
```

## Quality commands

```bash
npm run typecheck
npm run lint
npm test
npm run build
npm run check
```

## Deployment

The application requires a Node.js runtime because it contains API routes. It is not a static-export-only site.

```bash
npm install
npm run build
npm run start
```

See `docs/DEPLOYMENT.md`, `docs/WEBHOOKS.md`, and `SECURITY.md` before production release.

## Production release gate

Before publishing:

1. Verify registration numbers, office details, executive names, public metrics, field stories, partner references, and all program claims with authorized SURID records.
2. Replace placeholder/stock photography with approved images and documented consent/licensing.
3. Configure monitored webhook endpoints and test failure handling.
4. Keep PSEA disabled until the safeguarding focal point approves the protected workflow.
5. Confirm donation instructions through the receiving desk and payment provider; never infer payment status from a browser submission.
6. Run `npm run check` in CI.
