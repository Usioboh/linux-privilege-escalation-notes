# SUID Symlinks
It's a privilege escalation technique that abuses SUID programs that read or write files by replacing those files with symbolic links pointing to sensitive system files. The SUID program follows the symlink and reads or writes the sensitive file as root.
## How to Find it
find / -perm -4000 2>/dev/null

## Check what files the binary reads or writes
strace /path/to/binary 2>&1
## How to Prevent it
Restrict write permissions on directories containing files used by SUID programs
