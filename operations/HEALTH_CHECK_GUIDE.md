# Health Check Guide

## Runtime Health Endpoints

| Endpoint | Purpose |
| --- | --- |
| `GET /api/v1/health` | Backend service health. |
| `GET /api/v1/liveness` | Process liveness. |
| `GET /api/v1/readiness` | Backend plus database readiness. |
| `GET /api/v1/version` | Version, environment, and profile metadata. |
| `GET /api/v1/metrics/runtime` | Runtime request metrics. |

## Commands

```powershell
.\scripts\aegis.ps1 health
.\scripts\aegis.ps1 verify-deployment
```

`health` is a fast operator check. `verify-deployment` creates durable report evidence.
