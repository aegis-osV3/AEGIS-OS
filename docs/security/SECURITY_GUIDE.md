# Security Guide

## Security Validation

```powershell
.\scripts\aegis.ps1 security-scan
```

The command detects OpenSSL, Java, Trivy, Docker Scout, and OWASP Dependency-Check. When Trivy is available, it runs repository configuration and filesystem scans. When Docker Scout is available, it attempts a bounded filesystem CVE scan. It also performs a local high-confidence committed-secret pattern scan while excluding generated dependency and build directories.

Security tools are resolved from explicit `AEGIS_*_PATH` overrides, then `PATH`, then known transfer-workstation tool locations. Supported overrides are documented in `scripts/README.md` and `docs/platform/CROSS_PLATFORM_GUIDE.md`.

Docker Scout may require Docker Desktop authentication or `docker login`. The filesystem scan is bounded and reports a warning if it times out. Do not store Docker credentials, access tokens, or registry secrets in the repository.

## Dependency-Check Database

OWASP Dependency-Check runs with `--noupdate` by default so a release scan does not silently change vulnerability inputs. Unless `AEGIS_DEPENDENCY_CHECK_DATA` is set, AEGIS uses the ignored repository-local cache path:

```text
var/security/dependency-check-data
```

On a machine where the Dependency-Check vulnerability database has not been initialized, the scan fails early with:

```text
No initialized vulnerability database was found under ...\var\security\dependency-check-data
```

Initialize or refresh the database explicitly:

```powershell
$env:AEGIS_DEPENDENCY_CHECK_ALLOW_UPDATE = "true"
$env:AEGIS_DEPENDENCY_CHECK_DATA = "var/security/dependency-check-data"
.\scripts\aegis.ps1 security-scan
```

The `var/` directory is ignored by git and is intended for generated local caches. After initialization, unset `AEGIS_DEPENDENCY_CHECK_ALLOW_UPDATE` to return to deterministic no-update scans.

For faster and more reliable first-run NVD updates, provide an API key through the shell environment:

```powershell
$env:AEGIS_NVD_API_KEY = "<redacted-api-key>"
```

Never store the NVD API key in `.env`, documentation, reports, or source control.

## Secure Defaults

- `.env` is ignored by git.
- Production rejects known placeholder secrets.
- Backend errors return stable JSON without exposing internal exception details.
- Frontend production image runs from Next.js standalone output.
- Kubernetes and Helm PostgreSQL manifests keep the official image UID/GID `999`; Trivy may report this as low severity. Treat it as a documented compatibility decision unless replacing PostgreSQL with a validated enterprise image.

## Follow-Up Security Work

Security reports should be regenerated before release certification and whenever dependency manifests change.
