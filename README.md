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

Production environment variables: `JWT_SECRET` (secure random value), `DATABASE_PATH=/tmp/champions_club.db`. Configure Gmail, Telegram, or Gemini integration keys only if you use those features.

**Demo only:** Vercel `/tmp` is ephemeral and instance-local. SQLite changes will not persist reliably, and data may reset after cold starts. Do not use this deployment for real transactions or customer data. For production, switch to a persistent hosted database, disable seeded public demo users, and review authentication.

Promotional video may load from the original public GitHub repository; redundant original high-resolution images were left out to keep deployment manageable.
