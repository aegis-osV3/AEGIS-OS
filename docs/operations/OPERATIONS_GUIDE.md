# Operations Guide

## Command Surface

All supported operations route through:

```powershell
.\scripts\aegis.ps1 <command>
```

Key commands:

| Task | Command |
| --- | --- |
| Bootstrap | `.\scripts\aegis.ps1 bootstrap` |
| Stop | `.\scripts\aegis.ps1 stop` |
| Restart | `.\scripts\aegis.ps1 restart` |
| Status | `.\scripts\aegis.ps1 status` |
| Logs | `.\scripts\aegis.ps1 logs` |
| Health | `.\scripts\aegis.ps1 health` |
| Smoke test | `.\scripts\aegis.ps1 smoke` |
| Backup | `.\scripts\aegis.ps1 backup` |
| Restore | `.\scripts\aegis.ps1 restore -BackupFile <path>` |

## Normal Shutdown

```powershell
.\scripts\aegis.ps1 stop
```

This stops containers without deleting the database volume.

## Clean Demonstration Reset

```powershell
.\scripts\aegis.ps1 reset-demo
```

This deletes the Compose database volume. Use only when a clean evaluation state is intended.
