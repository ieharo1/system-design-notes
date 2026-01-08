# SQL Backup at Scale – Case Study

## Context

Multiple SQL Server instances on Windows Server 2016.

---

## Requirements

- Daily automated backups
- Compression
- NAS offloading
- Cleanup
- Alerting

---

## Implemented Solution

- PowerShell automation
- ZIP compression
- NAS via SMB
- Telegram Bot notifications

---

## Observed Benefits

- Reduced disk usage
- Faster failure detection
- Zero manual intervention

---

## Lessons Learned

- Backups without alerts are useless
- Visibility matters more than complexity
