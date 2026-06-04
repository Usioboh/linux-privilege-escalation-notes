# Cron Wildcard Exploitation
## What it is
It is a privilege escalation technique that abuses cron jobs using wildcards (*) in commands like tar. When a wildcard expands Linux includes all filenames in the directory — including specially crafted filenames that look like command flags. If the cron job runs as root those fake flags execute malicious code with root privileges.
## How to Find it
"cat /etc/crontab"

Look for cron jobs running as root that use wildcards (*) especially with commands like tar, rsync or chown.

## How to Prevent it

Always use full explicit paths instead of wildcards in cron jobs

Use -- before the wildcard to tell tar to treat everything after as filenames not flags:

tar czf backup.tar.gz -- *
