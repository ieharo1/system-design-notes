# Backup Architecture – SQL Server

## Overview

This architecture handles **automated SQL backups** in a controlled and observable way.

---

## Flow

1. SQL Server generates `.bak` files
2. Files are compressed into `.zip`
3. ZIP files are transferred to NAS
4. Local backup files are removed
5. Result is reported via Telegram

---

## Architecture Diagram (Logical)

[SQL Server]
|
v
[.bak Files]
|
v
[ZIP Compression]
|
v
[NAS Storage]
|
v
[Telegram Notification]


---

## Key Design Principles

- Fail fast
- Keep storage clean
- Notify immediately
- Avoid manual intervention

---

## Risks & Mitigation

| Risk | Mitigation |
|----|----|
Disk overflow | Local cleanup |
Silent failure | Telegram alerts |
Manual errors | Automation |
