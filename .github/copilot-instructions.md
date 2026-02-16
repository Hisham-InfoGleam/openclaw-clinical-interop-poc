# AI Automation POC — Copilot Instructions

You are assisting Hisham Alrashdan building "AI Automation Hub" as a portfolio-grade POC that demonstrates automation, integrations, and agentic workflows.

## Project Goals
- Build a clean, modular automation platform suitable for demos and learning.
- Prefer reproducible, testable workflows and clear boundaries between services.
- Keep examples synthetic; never embed secrets or real credentials.

## Permitted Tech Stack
- Orchestration: n8n or LangGraph (as needed)
- Backend: Node.js + TypeScript (strict) + Express or Fastify
- Validation: zod
- ORM: Prisma (preferred) or TypeORM
- Data: PostgreSQL or MariaDB (choose one per feature)
- Security: helmet, bcrypt, jsonwebtoken, dotenv

## Project Layout (Recommended)
- /automation-api — Core API (REST) and workflow endpoints
- /agents — Agent logic and tools
- /db — Schema, migrations, seed (synthetic only)
- /docs — Public docs only

## Engineering Workflow (Required)
1. Plan: Max 8 bullets explaining logic
2. Context: Use Context7 (mcp_context7_resolve-library-id) for new libraries
3. Diffs: List files to create/modify
4. Implement: Small, testable chunks (< 300 lines)
5. Security: Verify no secrets or PII in logs/tests
6. Gates: Run npm run lint and npm run test before finishing

## Output Format
- Keep changes under 300 lines unless approved
- Add MIT header to new logic files
- Add/adjust tests for non-trivial logic
- Ask 1-3 precise questions when uncertain

## Publishing (GitHub)
- Repo naming: use a clear slug without quotes (example: https://github.com/Hisham-InfoGleam/<project-name>)
- Before publishing: run npm run lint and npm run test
- README must include: project summary, tech stack, author, and license (MIT)
- Do not commit secrets, internal IPs, or private business content
- If not accepting contributions, add a short note in README instead of adding CONTRIBUTING.md

## Development Triggers (Hisham's Commands)
- "Prepare my POC for GitHub" → Generate Tier 1 docs + security checklist
- "Check before push" → Run pre-push security verification
