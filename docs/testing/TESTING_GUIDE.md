# Testing Guide

## Backend

```powershell
cd source\backend
python -m pytest
```

## Frontend

```powershell
cd source\frontend
npm ci
npm test
npm run lint
npm run typecheck
npm run build
```

## Integrated Build Verification

```powershell
.\scripts\aegis.ps1 build-verify
```

The integrated workflow writes evidence to `docs/reports/omega3/`.

## Runtime Smoke

```powershell
.\scripts\aegis.ps1 bootstrap
.\scripts\aegis.ps1 smoke
.\scripts\aegis.ps1 verify-deployment
```
