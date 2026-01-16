# Architecture Overview

## High-level flow
1. Ingest vendor communications (mock emails / issue logs)
2. Run sentiment scoring + drift detection (trend over time)
3. Evaluate SLA status (due dates vs delivered)
4. Compute Vendor Health Score + Risk Level
5. Generate executive summaries (PDF artifacts)
6. Expose results via API endpoints (FastAPI)

## Repo structure
- `app/` — FastAPI entry, models, schemas, CRUD
- `core/` — sentiment engine, SLA watchdog, risk scoring
- `db/` — database session and base
- `data/` — mock emails + generated reports
- `tests/` — risk logic + API tests
