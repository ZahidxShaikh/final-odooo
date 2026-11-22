# Alpha Sports Club — Odoo × LPU Hackathon

Full-stack sports-club management demo with React/Vite UI and Python FastAPI backend. Includes member bookings, front desk, pro shop, cafe, CRM, HR, finance, and owner dashboards.

## Local setup

Python 3.11+ and Node.js 20+ are required.

```bash
pip install -r requirements.txt
npm ci
npm run setup
npm run dev
```

## Vercel setup

Build: `npm run build` (Vite). API: `api/index.py` (FastAPI), routed through `vercel.json`.

Production environment variables: `DATABASE_URL` (Neon PostgreSQL connection string, encrypted on Vercel) and `JWT_SECRET` (secure random value). Configure Gmail, Telegram, or Gemini integration keys only if you use those features. For local development without `DATABASE_URL`, the app continues to use SQLite.

**Neon persistent storage enabled:** production database records now persist independently of serverless restarts. Existing SQLite demo records were not imported from ephemeral Vercel instances; this is a fresh PostgreSQL demo seed. **Demo only:** publicly known seeded demo credentials remain enabled, so do not use real customer data or real payment processing without replacing demo accounts, strengthening authorization, and reviewing transaction safety. Neon free-tier quotas still apply.

Promotional video may load from the original public GitHub repository; redundant original high-resolution images were left out to keep deployment manageable.
