# Release Validation Checklist

Date: 2026-07-01

| Item | Classification | Evidence |
| --- | --- | --- |
| Complete source code | PRESENT | `source/AEGIS_OS_V3/source/` |
| Documentation | PRESENT | `docs/` and `source/AEGIS_OS_V3/docs/` |
| Configuration files | PRESENT | `config/` and product root config files |
| Environment templates | PRESENT | `config/.env.example` |
| Docker configuration | PRESENT | `config/docker-compose.yml`, `config/docker-compose.prod.yml`, Dockerfiles under source snapshot |
| Startup scripts | PRESENT | `scripts/START_AEGIS.ps1`, `scripts/START_AEGIS.bat`, `scripts/STOP_AEGIS.bat` |
| Build scripts | PRESENT | Dockerfiles, Compose files, package manifests, and operator scripts |
| Installation instructions | PRESENT | `transfer/INSTALLATION_REFERENCE.md`, demo quick start, and product `INSTALL.md` |
| Demo information | PRESENT | `demo/DEMO_ACCOUNT_INFORMATION.md`, `demo/DEMO_DATA_SUMMARY.md` |
| Repository structure | PRESENT | `transfer/REPOSITORY_MAP.md` and product repository guide |
| Commercial documentation | PRESENT | `reports/` and `source/AEGIS_OS_V3/Sales_Package/` |
| Asset inventory | PRESENT | `reports/ASSET_DELIVERY_REPORT.md` and `assets/` |
| License documentation | PRESENT | `licenses/` |
| Transfer documentation | PRESENT | `transfer/` |
| Known limitations | PRESENT | `reports/KNOWN_LIMITATIONS.md` |
| Runtime validation in Phase 5 | NOT APPLICABLE | Phase 5 explicitly prohibits runtime validation/debugging. |
| Executable installer | OPTIONAL | Not generated. Simple startup scripts are provided. |
| TAR archive | OPTIONAL | ZIP archive is generated; TAR is optional. |
