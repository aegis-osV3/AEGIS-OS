# Repository Map

```text
AEGIS_OS_V3/
  source/
    backend/              FastAPI backend, app factory, routes, models, services, tests
    frontend/             Next.js frontend, app routes, components, services, tests
    shared/               Reserved shared contracts
  database/
    migrations/           Migration mirror and schema history
    schema/               Schema documentation
    seeds/                Demo and enterprise seed data
  infrastructure/
    docker/               Backend and frontend Dockerfiles
    deployment/k8s/       Kubernetes manifests
    deployment/helm/      Helm chart
    scripts/              Legacy-compatible operational scripts
  scripts/
    aegis.ps1             Canonical operator entry point
    omega3.ps1            Omega 3 verification and reporting harness
    bootstrap/            Discoverable bootstrap wrapper
    build/                Discoverable build-verification wrapper
    verification/         Platform and deployment verification wrappers
    security/             Security verification wrapper
  config/
    env/                  Development, testing, demo, and production templates
  docs/
    getting-started/      Quick start, install, bootstrap
    repository/           Repository guide and map
    architecture/         System architecture
    development/          Developer and build guides
    deployment/           Docker and verification guides
    operations/           Operations and health guides
    platform/             Cross-platform support
    security/             Security guide
    troubleshooting/      Troubleshooting guide
    reports/omega3/       Omega 3 logs, audits, reports, and generated evidence
```

## Fast Navigation

- Start here: `docs/getting-started/QUICK_START.md`
- Bootstrap: `scripts/aegis.ps1 bootstrap`
- Build verification: `scripts/aegis.ps1 build-verify`
- Deployment verification: `scripts/aegis.ps1 verify-deployment`
- Platform verification: `scripts/aegis.ps1 verify-platform`
- Configuration templates: `config/env/`
- Backend API code: `source/backend/app/api/v1/`
- Frontend routes: `source/frontend/app/`
