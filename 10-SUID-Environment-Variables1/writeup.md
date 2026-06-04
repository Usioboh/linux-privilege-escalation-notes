# SUID Environment Variables 1
It's a privilege escalation technique that exploits SUID binaries calling commands without full paths.
## How to find
find / -perm -4000 2>/dev/null

## Check what commands the binary calls
strings /path/to/binary
## How to Prevent it
Always use full absolute paths in scripts and binaries

Never trust the PATH environment variable in privileged programs
