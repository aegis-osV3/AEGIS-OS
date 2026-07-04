# Startup Checklist

| Item | Status | Notes |
| --- | --- | --- |
| Docker Desktop or Docker Engine installed | PRESENT | Docker CLI and Compose were detected on this host. |
| Docker daemon running | REQUIRED | Not reachable during this pass. Start Docker before launch. |
| `.env.example` present | PASS | Present in product root. |
| `.env` present | PASS | Created by launcher during validation. |
| PostgreSQL host port | PASS | Local `.env` set to `POSTGRES_PORT=5433` to avoid a host conflict. |
| Backend port `8000` | PASS | Available during validation. |
| Frontend port `3000` | PASS | Available during validation. |
| Compose config | PASS | `docker-compose.yml` passed syntax validation. |
| Launch command | AVAILABLE | `.\START_AEGIS.ps1` or `.\scripts\aegis.ps1 bootstrap`. |
| Stop command | AVAILABLE | `STOP_AEGIS.bat` or `.\scripts\aegis.ps1 stop`. |
