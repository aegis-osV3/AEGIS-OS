# Cross-Platform Guide

## Supported Platforms

| Platform | Status | Notes |
| --- | --- | --- |
| Windows 11 + Docker Desktop | Official | Primary local evaluation path. |
| Windows 11 + WSL2 | Official | Use Docker Desktop WSL integration or run from PowerShell. |
| Linux + Docker Engine | Official | Requires PowerShell or compatible script execution for the canonical launcher. |
| Docker Compose | Official | Runtime contract is Compose-based. |
| macOS | Future-ready | Expected to work with Docker Desktop and PowerShell, but not an official validation target. |

## Platform Verification

```powershell
.\scripts\aegis.ps1 verify-platform
```

This detects operating system, PowerShell, Git, Docker, Compose, Node, npm, Python, OpenSSL, Java, Trivy, Docker Scout, and OWASP Dependency-Check.

The verification command accepts explicit tool-path overrides for environments where tools are installed outside `PATH`:

| Tool | Override |
| --- | --- |
| Git | `AEGIS_GIT_PATH` |
| Docker CLI | `AEGIS_DOCKER_PATH` |
| Docker Compose | `AEGIS_DOCKER_COMPOSE_PATH` |
| Docker config directory | `AEGIS_DOCKER_CONFIG` |
| OpenSSL | `AEGIS_OPENSSL_PATH` |
| Java | `AEGIS_JAVA_PATH` |
| Trivy | `AEGIS_TRIVY_PATH` |
| OWASP Dependency-Check | `AEGIS_DEPENDENCY_CHECK_PATH` |
| Docker Scout | `AEGIS_DOCKER_SCOUT_PATH` |
| NVD API key for Dependency-Check updates | `AEGIS_NVD_API_KEY` |

Example:

```powershell
$env:AEGIS_GIT_PATH = "C:\Program Files\Git\cmd\git.exe"
.\scripts\aegis.ps1 verify-platform
```

Docker CLI detection is not enough for closure. The Docker daemon must also be reachable through the active Docker context before bootstrap, build verification, deployment verification, Docker Scout evidence, and runtime health checks can pass. AEGIS daemon probes are bounded and report a timeout when the daemon does not respond promptly.

AEGIS preserves the active Docker context by default. Use `AEGIS_DOCKER_CONFIG` only when an isolated Docker config directory is required for a repeatable validation run.

## File System Guidance

- Keep work inside `AEGIS_OS_V3/`.
- Avoid hardcoded absolute paths in source.
- Use `.env` for host-specific values.
- Keep generated reports under `docs/reports/omega3/`.
- Use `POSTGRES_PORT` when another local PostgreSQL service already owns host port `5432`.
- Keep line endings normalized by `.gitattributes`.
