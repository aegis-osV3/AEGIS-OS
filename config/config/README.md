# Configuration Directory

This directory contains environment templates and configuration guidance used by the Omega 3 transfer workflows.

## Layout

| Path | Purpose |
| --- | --- |
| `env/.env.development.example` | Local Docker Compose and developer workstation defaults. |
| `env/.env.testing.example` | Local automated test profile using isolated test values. |
| `env/.env.demonstration.example` | Evaluation profile for the Omega 2 enterprise demonstration data set. |
| `env/.env.production.example` | Production-ready template with required secret placeholders and no committed secret values. |

The repository root `.env.example` remains the primary bootstrap template because Docker Compose automatically reads `.env` from the project root. Profile templates are copied manually only when a team needs to switch profiles.

## Policy

- Never commit `.env` or real secrets.
- Keep all runtime-specific values in environment variables or profile templates.
- Validate configuration with `.\scripts\aegis.ps1 validate` before startup.
- Use `.\scripts\aegis.ps1 bootstrap` for a full environment preparation and health verification run.
