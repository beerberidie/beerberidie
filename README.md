# Garason Griesel

Backend and API integration developer in South Africa (UTC+2). I build and fix the parts of business systems that clients don't see: APIs, database security, scheduled jobs, and data pipelines.

Before freelancing I spent 4 years supporting payments infrastructure at Mercantile Bank (now Capitec). I still work the way the bank taught me: every change reversible, and every fix proven from the logs.

**Hire me on Upwork:** https://www.upwork.com/freelancers/~01aeeb8c3a6fed5b69

## Public work

| Repo | What it shows |
|---|---|
| [scratchv3-content-pipeline](https://github.com/beerberidie/scratchv3-content-pipeline) | FastAPI automation pipeline: AI content generation, Redis-locked scheduler, WordPress REST publishing as drafts, encrypted API-key storage, 89 tests |
| [MT5_UI](https://github.com/beerberidie/MT5_UI) | FastAPI + Celery workstation for MetaTrader 5: rule-based trade ideas that need human approval, config-driven risk limits, 151 tests |

## Private client work (walkthroughs on request)
- **Security retrofit of a live Supabase app.** Closed anonymous access to password hashes and an API key, moved every write behind a verified server proxy, and staged it through reversible migrations, including recovering from a same-day incident.
- **Multi-tenant REST API** (FastAPI, PostgreSQL, Alembic): agency and branch isolation taken from the JWT, with tests proving cross-tenant access is denied.
- **Delivery scheduler for OutaAfrica** with driver permissions enforced by Row-Level Security and a locked-down RPC.
- **PDF report extraction** into de-duplicated database rows and Excel (SHA-256 content fingerprinting).

## Stack
Python · FastAPI · PostgreSQL · Supabase · SQLAlchemy/Alembic · Redis · Docker · Node.js · React · TypeScript
