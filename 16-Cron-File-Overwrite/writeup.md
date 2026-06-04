# Cron File Overwrite
## What it is
A cron job runs as root and executes a script. If that script file has weak permissions (allows regular users to write to it), you can overwrite it with malicious code that runs as root when cron executes it.
## How to Find it
cat /etc/crontab

*Check permissions on the script being called
ls -la /path/to/script.sh

You're looking for a script owned by root but writable by everyone:
## How to Prevent it
Set correct permissions on scripts called by cron:

bashchmod 700 /path/to/script.sh

Only root should own and write to scripts executed by root cron jobs
