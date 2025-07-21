# Linux Backup & System Health Check Scripts

## 📌 Description
Automated Bash scripts for Linux to manage system backups and health checks. Features include compressed backups, logging, error handling, and Cron scheduling. The health check script monitors disk space, memory, running services, and updates, providing actionable recommendations.

---

## 🛠️ Installation

Clone the repository:

```bash
https://github.com/AymanQarout02/Linux-Backup-System-Health-Check-Scripts.git
cd linux-backup-health-check

chmod +x backupv1.sh
chmod +x health_check.sh

▶️ Usage
✅ Backup Script (backupv1.sh)
Run the backup script:


./backupv1.sh -s "/path/to/folder1 /path/to/folder2" -d "/path/to/backup" -c
Options:

-s : Source directories to back up (multiple directories can be separated by spaces) (required)

-d : Destination directory for backup (default: Desktop)

-c : Compress backup files (.tar.gz) (optional)

-h : Show help message

Logs are saved in the destination folder as backup.log.

Example: Schedule a daily backup at 5 AM using Cron:

0 5 * * * /path/to/backupv1.sh -s "/path/to/project" -d "/path/to/backup" -c


✅ System Health Check Script (health_check.sh)
Run the health check script:

./health_check.sh
The script will:

Display and log:

Disk space usage

Memory usage

Running services

Recent package updates

Provide recommendations:

Warn if disk usage exceeds 80% (lists top 10 largest files).

Warn if free memory is below 200 MB (lists top memory-using processes).

Check if important services (cron, dbus, rsync) are running.

Suggest upgrading packages if updates are available.

Logs are saved in health_check.log.

📄 Documentation
For full details, refer to the complete 📥 Documentation (PDF).
