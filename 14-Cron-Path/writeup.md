# Cron Path Exploitation

## What It Is
It is a privilege escalation technique that abuses cron jobs calling scripts without full paths. Cron has its own PATH variable. So if a directory you control appears first in that PATH, you can plant a malicious script that runs as root when cron executes.

## How to find it
To find the path, you can simply just type "cat /etc/crontab"

## How to prevent it
Always use full paths in cron jobs and audit crontab regularly for misconfigurations






