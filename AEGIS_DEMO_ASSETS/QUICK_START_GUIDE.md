# Quick Start Guide

## Prerequisites

- Windows PowerShell or PowerShell 7
- Docker Desktop or Docker Engine with `docker compose`
- Ports `5433`, `8000`, and `3000` available
- At least 5 GB free disk space and 2 GB memory available to Docker

## Start

From `AEGIS_OS_V3/`:

```powershell
.\START_AEGIS.ps1
```

Or double-click:

```text
START_AEGIS.bat
```

The buyer wrapper sets `POSTGRES_PORT=5433` for local evaluation and calls the supported product launcher:

```powershell
.\scripts\aegis.ps1 bootstrap
```

## Stop

```text
STOP_AEGIS.bat
```

## URLs

- Frontend: `http://localhost:3000`
- Login: `http://localhost:3000/login`
- API: `http://localhost:8000/api/v1`
- API docs: `http://localhost:8000/docs`

## Demo Data

After the runtime is available, seed the official enterprise demo:

```powershell
.\scripts\aegis.ps1 seed-omega2
```

See `DEMO_ACCOUNT_INFORMATION.md` for accounts.
