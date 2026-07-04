# Startup Status

Date: 2026-07-01

## Command Tested

```powershell
.\scripts\aegis.ps1 bootstrap -NoBrowser -TimeoutSeconds 300
```

## Result

PARTIAL PASS.

## Passing Checks

- Product files present
- `.env` present
- Docker CLI present
- Docker Compose present
- Compose config valid
- Python present
- Node present
- Required environment values present
- Disk and memory checks passed
- Ports `5433`, `8000`, and `3000` available

## Warnings

- Placeholder secrets are present for local evaluation only.

## Blocking Check

- Docker daemon is not reachable on this host.

## Required Buyer Action

Start Docker Desktop or Docker Engine, then run:

```powershell
.\START_AEGIS.ps1
```
