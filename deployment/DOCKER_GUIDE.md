# Docker Guide

## Compose Files

| File | Purpose |
| --- | --- |
| `docker-compose.yml` | Local evaluation and development runtime. |
| `docker-compose.prod.yml` | Production-oriented template requiring explicit secrets. |

## Images

| Service | Dockerfile |
| --- | --- |
| Backend | `infrastructure/docker/backend.Dockerfile` |
| Frontend | `infrastructure/docker/frontend.Dockerfile` |

The frontend image uses `npm ci` to enforce the committed lockfile.

## Start

```powershell
.\scripts\aegis.ps1 bootstrap
```

Manual Compose startup is supported for debugging only:

```powershell
copy .env.example .env
docker compose up -d --build
```

Then verify:

```powershell
.\scripts\aegis.ps1 verify-deployment
```
