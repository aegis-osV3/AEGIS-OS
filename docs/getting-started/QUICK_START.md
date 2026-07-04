# Quick Start

## Objective

Bring AEGIS OS V3 to a running, verified local deployment from a fresh clone or copied repository.

## Prerequisites

- Docker Desktop or Docker Engine with `docker compose`
- PowerShell
- Ports `5432`, `8000`, and `3000`
- At least 5 GB free disk space and 2 GB memory available to Docker

For local engineering checks, also expose Python 3.12-compatible tooling, Node.js 22-compatible tooling, and npm on `PATH`.

If a required tool is installed outside `PATH`, set the matching `AEGIS_*_PATH` override described in `scripts/README.md`. If another PostgreSQL service already owns host port `5432`, set `POSTGRES_PORT=5433` or another free port in `.env` before bootstrap.

## First Run

From the repository product root:

```powershell
cd "D:\AEGIS\Aegis OS\AEGIS_OS_V3"
.\scripts\aegis.ps1 bootstrap
```

Expected result:

- `.env` is created from `.env.example` when absent.
- Docker Compose builds backend and frontend images.
- PostgreSQL, backend, and frontend start.
- Backend health and readiness pass.
- Frontend and login page are reachable.
- Browser opens to `http://localhost:3000/login`.

## Verify

```powershell
.\scripts\aegis.ps1 verify-deployment
.\scripts\aegis.ps1 smoke
```

Verification reports are written to `docs/reports/omega3/`.

## First Login Journey

1. Open `http://localhost:3000/login`.
2. Register a user.
3. Create an organization.
4. Open the dashboard.
5. Optionally seed the demonstration data:

```powershell
.\scripts\aegis.ps1 seed-omega2
```
