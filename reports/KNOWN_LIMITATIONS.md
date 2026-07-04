# Known Limitations

Date: 2026-07-01

## Runtime

- Docker daemon was not reachable on this host during the Phase 4 demo pass.
- Docker CLI and Docker Compose are installed, and Compose configuration validates, but containers were not started in this pass.
- Local host port `5432` was occupied. The local demo environment was adjusted to use `POSTGRES_PORT=5433`.
- Demo seed data was not applied during this pass because the application runtime did not launch.

## Configuration

- `.env.example` contains placeholder local-evaluation secrets.
- `POSTGRES_PASSWORD` and `JWT_SECRET_KEY` must be replaced before shared, staging, or production use.
- Production email, OAuth, and external provider credentials are not configured in the local package.

## Evaluation

- Implemented frontend routes and backend endpoints are inspectable in source and prior evidence, but current live browser validation was not completed because Docker was unavailable.
- No claim is made that this package is production deployed.
