# Repository Guide

## Objective

Make repository ownership understandable to an engineering team that has never worked on AEGIS OS.

## Canonical Product Root

The engineering product is contained in:

```text
AEGIS_OS_V3/
```

The larger workspace may include buyer, brand, outreach, and website packages. Product source, deployment, verification, and operations live in `AEGIS_OS_V3/`.

## Ownership Boundaries

| Area | Path | Ownership |
| --- | --- | --- |
| Backend | `source/backend/` | FastAPI API, services, models, migrations runtime, tests. |
| Frontend | `source/frontend/` | Next.js UI, routes, components, services, tests. |
| Database | `database/` | Schema overview, migration mirror, seed data. |
| Infrastructure | `infrastructure/` | Dockerfiles, Compose-adjacent deployment assets, Kubernetes and Helm templates. |
| Scripts | `scripts/` | Supported bootstrap, build, verification, security, and operational entry points. |
| Configuration | `config/` and `.env.example` | Environment profiles and runtime templates. |
| Documentation | `docs/` | Engineering documentation and release evidence. |
| Acquisition | `acquisition/` | Buyer and transfer review assets. |

## Standardization Decision

The existing product layout is preserved because backend, frontend, infrastructure, scripts, docs, and acquisition material already have clear boundaries. Omega 3 standardization adds missing documentation hierarchy, config profiles, verification scripts, and evidence reports instead of moving working business modules.
