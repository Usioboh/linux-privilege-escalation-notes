# Weak File Permissions
It's a privilege escalation technique that exploits incorrectly set permissions on sensitive system files. If critical files like /etc/passwd or /etc/shadow are writable by regular users you can modify them directly to add a root user or change an existing password to gain root access.
## How to Find it
ls -la /etc/passwd

ls -la /etc/shadow
## How to Prevent it
Set correct permissions on sensitive files:
