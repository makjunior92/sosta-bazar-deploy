# Sosta Bazar — Full Docker Stack

Run the entire platform with **one command**. No local Node/Python install needed.

## Start

```bash
cd sosta-bazar-deploy
docker compose up --build -d
```

## Open in browser

| URL | What |
|-----|------|
| **http://localhost:8080** | Main app (search, deals, compare prices) |
| http://localhost:8080/docs | API documentation |
| http://localhost:8080/health | API health check |

## Stop

```bash
docker compose down
```

## Rebuild after code changes

```bash
docker compose up --build -d
```

## Services

- **nginx** (port 8080) — single entry point
- **web** — Next.js frontend
- **api** — FastAPI backend
- **worker** — Celery scraper workers
- **beat** — scheduled price refresh
- **postgres** — database
- **redis** — cache + job queue
