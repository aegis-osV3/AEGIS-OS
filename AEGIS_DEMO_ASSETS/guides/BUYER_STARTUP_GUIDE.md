# Buyer Startup Guide

## Fast Path

1. Open `AEGIS_OS_V3/`.
2. Start Docker Desktop or Docker Engine.
3. Run:

```powershell
.\START_AEGIS.ps1
```

4. Open `http://localhost:3000/login`.
5. Seed demo data after first successful startup:

```powershell
.\scripts\aegis.ps1 seed-omega2
```

6. Sign in with a demo account from `DEMO_ACCOUNT_INFORMATION.md`.

## Stop

```text
STOP_AEGIS.bat
```

## Expected Behavior

When Docker is running and required ports are available, the launcher should build/start PostgreSQL, backend, and frontend containers, verify health/readiness endpoints, and open the browser.

## Current Host Status

On 2026-07-01 the package could not launch because Docker daemon was not reachable. No product code repair was attempted beyond local startup configuration.
