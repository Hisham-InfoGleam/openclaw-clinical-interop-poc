---
applyTo: "db/**/*"
---
## Database Rules

- Use only synthetic seed data; never commit real user data
- Prefer migrations over manual schema edits; document rollback steps
- Design scheduling/queue tables to prevent overlaps (constraints + transactions)
- Isolate database containers in `docker-compose.yml`; bind to localhost only
- Never commit connection strings; use `.env.example` with placeholders
