---
applyTo: "automation-api/**/*.{ts,tsx,js}"
---
## Automation API Rules

### TypeScript & Safety
- Use strict mode; explicit types at module boundaries (DTOs, tool I/O)
- Validate all external inputs with zod; return 400 with safe errors
- Implement "Approval-Required" flags for shell commands or DB writes

### Logging & Secrets
- Never log secrets, tokens, or raw payloads from external services
- Redact sensitive fields in examples; use `.env.example` placeholders only

### Workflow Design
- Provide correlation IDs for workflow runs
- Idempotent endpoints where possible to avoid duplicate side effects

### Skill Pattern
- Define agent tools as standalone TypeScript modules in `/automation-api/src/tools/`
- Keep tool contracts stable and versioned when breaking changes happen
