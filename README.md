# Sosta Bazar Deploy

Production Docker Compose stack for the decoupled Sosta Bazar platform.

## Services

- **web** — Next.js frontend
- **api** — FastAPI backend
- **worker** — Celery scraper workers
- **beat** — Scheduled refresh jobs
- **postgres** — PostgreSQL database
- **redis** — Cache and job queue
- **nginx** — Reverse proxy

## Quick start

```bash
cp .env.example .env
# Edit .env with production values

docker compose -f docker-compose.prod.yml pull
docker compose -f docker-compose.prod.yml up -d
```

Visit `http://your-server` (port 80).

## Local dev

Run each repo separately:

```bash
# API
cd ../sosta-bazar-api && docker compose up

# Web
cd ../sosta-bazar-web && npm run dev
```

Frontend: http://localhost:3000  
API: http://localhost:8000/docs
