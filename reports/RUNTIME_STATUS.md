# Runtime Status

Date: 2026-07-01

Current status: PARTIALLY AVAILABLE.

## Current Validation

The documented startup command was attempted from `AEGIS_OS_V3/`:

```powershell
.\scripts\aegis.ps1 bootstrap -NoBrowser -TimeoutSeconds 300
```

## Confirmed

- Required product files are present.
- Docker Compose syntax is valid.
- Docker CLI is available.
- Docker Compose is available, version `5.1.4`.
- Python is available, version `3.11.8`.
- Node is available, version `v24.13.1`.
- Disk and memory checks passed.
- Ports `5433`, `8000`, and `3000` are available after local configuration.

## Blocked

Docker daemon is not reachable:

```text
failed to connect to the docker API at npipe:////./pipe/dockerDesktopLinuxEngine
```

Runtime launch, login, health endpoint confirmation, dashboard checks, and seed execution require Docker Desktop or Docker Engine to be running.
