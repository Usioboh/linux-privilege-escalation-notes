# SUID Environment Variables 2
It's a privilege escalation technique that exploits SUID binaries even when they use full paths.

## How to Find it
find / -perm -4000 2>/dev/null
## How to Prevent it
Use execve() instead of system() in C code — it bypasses shell function resolution
