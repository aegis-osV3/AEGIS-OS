# Troubleshooting Guide

## Docker Daemon Not Reachable

Start Docker Desktop or Docker Engine, wait until it reports running, then retry:

```powershell
.\START_AEGIS.ps1
```

Verify Docker manually:

```powershell
docker info
docker compose version
```

## PostgreSQL Port Conflict

This package uses host PostgreSQL port `5433` for local demo startup. If another service uses that port, run:

```powershell
.\START_AEGIS.ps1 -PostgresPort 5434
```

## Frontend or Backend Port Conflict

Free ports `3000` and `8000`, then retry startup. The current buyer wrapper does not remap those ports.

## Clean Demo Reset

When Docker is running:

```powershell
.\scripts\aegis.ps1 reset-demo
.\scripts\aegis.ps1 seed-omega2
```

## Logs

```powershell
.\scripts\aegis.ps1 logs
```
