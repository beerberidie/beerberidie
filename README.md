# Garason Griesel

Backend and API integration developer in South Africa (UTC+2). I build and fix the parts of business systems that clients don't see: APIs, database security, scheduled jobs, and data pipelines.

Before freelancing I spent 4 years supporting payments infrastructure at Mercantile Bank (now Capitec). I still work the way the bank taught me: every change reversible, and every fix proven from the logs.

**Hire me on Upwork:** https://www.upwork.com/freelancers/~01aeeb8c3a6fed5b69

## Public work

| Repo | What it shows |
|---|---|
| [fieldagent-valuation-api](https://github.com/beerberidie/fieldagent-valuation-api) | Multi-tenant FastAPI + PostgreSQL API: agency/branch isolation taken from the JWT in one dependency, 10 Alembic migrations, 76 passing tests including cross-tenant denial tests |
| [scratchv3-content-pipeline](https://github.com/beerberidie/scratchv3-content-pipeline) | FastAPI automation pipeline: AI content generation, Redis-locked scheduler, WordPress REST publishing as drafts, encrypted API-key storage, 89 tests |
| [MT5_UI](https://github.com/beerberidie/MT5_UI) | FastAPI + Celery workstation for MetaTrader 5: rule-based trade ideas that need human approval, config-driven risk limits, 151 tests |

## Other production systems (walkthroughs on request)
- **Security retrofit of a live Supabase job board.** Closed anonymous access to password hashes and an API key, moved every write behind a verified server proxy, and staged it through reversible migrations, including recovering from a same-day incident.
- **Delivery scheduler** with driver permissions enforced by Row-Level Security and a locked-down RPC: the driver can change a job's status and nothing else.
- **PDF report extraction** into de-duplicated database rows and Excel (SHA-256 content fingerprinting).

## Stack
Python · FastAPI · PostgreSQL · Supabase · SQLAlchemy/Alembic · Redis · Docker · Node.js · React · TypeScript
