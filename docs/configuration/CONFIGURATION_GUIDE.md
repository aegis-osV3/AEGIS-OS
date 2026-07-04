# Configuration Guide

## Configuration Model

The root `.env` file is the active local runtime configuration. It is ignored by git and created from `.env.example` by bootstrap when missing.

Profile templates live in:

```text
config/env/
```

## Profiles

| Profile | Template |
| --- | --- |
| Development | `config/env/.env.development.example` |
| Testing | `config/env/.env.testing.example` |
| Demonstration | `config/env/.env.demonstration.example` |
| Production | `config/env/.env.production.example` |

## Validation

```powershell
.\scripts\aegis.ps1 validate
.\scripts\aegis.ps1 verify-platform
```

The backend validates environment names, ports, database URL shape, public API URL shape, JWT secret length, and production placeholder secrets.

## Port Overrides

If host port `5432` is occupied by an existing PostgreSQL service, set `POSTGRES_PORT` in `.env` before bootstrap. The container still listens on `5432`; only the host-published port changes.

## Secret Handling

- Never commit `.env`.
- Never place real secrets in documentation.
- Replace placeholder secrets before shared, staging, or production use.
- Production startup rejects known placeholder secrets.
