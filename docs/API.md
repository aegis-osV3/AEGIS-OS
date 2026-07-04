# API Documentation

Date: 2026-06-27

The local API base URL is:

```text
http://localhost:8000/api/v1
```

Interactive OpenAPI documentation is provided by FastAPI at:

```text
http://localhost:8000/docs
```

## Identity

- `POST /auth/register`
- `POST /auth/login`
- `POST /auth/refresh`
- `POST /auth/logout`
- `POST /auth/forgot-password`
- `POST /auth/reset-password`
- `POST /auth/change-password`
- `POST /auth/change-email`
- `GET /auth/account-activity`
- `GET /auth/sessions`
- `GET /users/me`
- `PUT /users/{user_id}`

## Organizations And RBAC

- `POST /organizations`
- `GET /organizations`
- `GET /organizations/{organization_id}`
- `PUT /organizations/{organization_id}`
- `POST /organizations/{organization_id}/members`
- `GET /organizations/{organization_id}/members`
- `POST /organizations/{organization_id}/join`
- `POST /organizations/{organization_id}/roles/assign`
- `GET /roles`

## Workspace

- `GET /search`
- `GET /notifications`
- `POST /notifications/read`
- `POST /notifications/clear`
- `GET /executive/dashboard`
- `GET /security/dashboard`

## Health

- `GET /health`
- `GET /readiness`
- `GET /liveness`
- `GET /version`
- `GET /metrics/runtime`

## Security Notes

- API errors return friendly JSON with `detail` and `code`.
- Local development password reset can expose a reset token for evaluation.
- Production mode does not expose raw reset tokens.
