# Bot AI — Premium AI Platform Starter

A separate starter project for Bot AI. It does not modify the existing DexAI project.

## Included
- Responsive premium landing page and chat interface
- Express backend and health endpoint
- Optional OpenAI chat integration
- Basic API rate limiting
- Optional Stripe subscription Checkout endpoint
- Environment-variable configuration; no secrets committed

## Run locally
1. Install Node.js 20+.
2. Copy `.env.example` to `.env`.
3. Run `npm install`.
4. Run `npm start`.
5. Open `http://localhost:3000`.

The UI works in preview mode without keys. Live AI requires `OPENAI_API_KEY`. Billing requires `STRIPE_SECRET_KEY` and valid recurring Stripe Price IDs. Configure secrets only in environment settings, never in frontend code or Git.

## Render deployment
Create a **new** Web Service and connect this separate repository.
- Runtime: Node
- Build command: `npm install`
- Start command: `npm start`
- Add environment variables from `.env.example` in Render Environment settings.
- Choose a region close to the intended audience.

## Production gaps
This is a starter, not a production-ready SaaS. Before public signups or accepting payments, add authentication, persistent user records, Stripe webhooks, per-user quotas, terms/privacy pages, abuse prevention, monitoring, and tests. Start with Stripe test mode.
