# Deployment Verification Guide

## Objective

Prove that a deployment is operational, not merely started.

## Command

```powershell
.\scripts\aegis.ps1 verify-deployment
```

Run this after `.\scripts\aegis.ps1 bootstrap -NoBrowser` on a host where `docker info` succeeds. If host port `5432` is already occupied, set `POSTGRES_PORT` before bootstrap.

## Checks

- Docker Compose service inspection
- Backend health endpoint
- Backend readiness endpoint
- Backend version endpoint
- Frontend application root
- Frontend login page

## Evidence

The command writes:

- JSON report for automation
- Markdown report for engineering review

Reports are stored under:

```text
docs/reports/omega3/
```

Failures include a recommendation column so another engineering team can act without source-code archaeology.
