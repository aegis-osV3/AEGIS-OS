# Bootstrap Guide

## Engineering Objective

Provide one documented, repeatable workflow that prepares configuration, starts the platform, and verifies health without tribal knowledge.

## Supported Command

```powershell
.\scripts\aegis.ps1 bootstrap
```

`start` remains supported for backward compatibility, but `bootstrap` is the Omega 3 documented workflow.

## Execution Flow

1. Resolve the repository root.
2. Create `.env` from `.env.example` when missing.
3. Validate repository files, Docker, Compose, ports, disk, memory, and environment variables.
4. Build Docker images unless `-SkipBuild` is supplied.
5. Start PostgreSQL, backend, and frontend through Docker Compose.
6. Wait for backend health, backend readiness, and frontend availability.
7. Verify health again.
8. Open the login page unless `-NoBrowser` is supplied.

## Idempotency

Running bootstrap repeatedly reuses existing `.env` and Docker volumes. It does not overwrite user configuration. Use `reset-demo` only when an intentional database volume reset is required.

## Environment Adaptation

- Set `POSTGRES_PORT` when host port `5432` is occupied by another PostgreSQL service.
- Set explicit `AEGIS_*_PATH` variables when Git, Docker, OpenSSL, Java, Trivy, or OWASP Dependency-Check are installed outside `PATH`.
- Docker CLI detection does not prove runtime readiness; bootstrap still requires a reachable Docker daemon.

## Reports

Run deployment verification after bootstrap:

```powershell
.\scripts\aegis.ps1 verify-deployment
```

This creates JSON and Markdown evidence under `docs/reports/omega3/`.
