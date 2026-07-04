# Installation Guide

## Supported Environments

Officially supported:

- Windows 11 with Docker Desktop
- Windows 11 with WSL2 and Docker Desktop integration
- Linux with Docker Engine and Docker Compose plugin
- Docker Compose deployment

Future-ready:

- macOS with Docker Desktop

## Required Software

- Git
- Docker
- Docker Compose plugin
- PowerShell
- Python 3.12-compatible runtime for backend engineering
- Node.js 22-compatible runtime and npm for frontend engineering
- OpenSSL, Java, Trivy, and OWASP Dependency-Check for security validation workflows

The repository detects these tools. It does not install or vendor them.

If a tool is installed outside `PATH`, set the matching `AEGIS_*_PATH` override described in `scripts/README.md`. The supported workflow detects explicit overrides before checking `PATH`.

## Install And Validate

```powershell
.\scripts\aegis.ps1 verify-platform
.\scripts\aegis.ps1 validate
```

`verify-platform` produces a report under `docs/reports/omega3/`. `validate` checks the runtime files, Docker, Compose, ports, disk, memory, and required configuration variables.

If another local PostgreSQL service owns host port `5432`, set `POSTGRES_PORT=5433` or another free host port in `.env` before startup.

## Start

```powershell
.\scripts\aegis.ps1 bootstrap
```

Use `-NoBrowser` for headless validation:

```powershell
.\scripts\aegis.ps1 bootstrap -NoBrowser
```
