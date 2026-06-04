# What it is
A privilege escalation technique that involves searching for passwords or credentials left in plain text across the filesystem.
## How to Find it
cat ~/.bash_history

# Search for passwords in config files
grep -ri "password" /etc/ 2>/dev/null

# Check for credentials in common locations
cat /etc/passwd
find / -name "*.conf" 2>/dev/null | xargs grep -i "password"

## How to Prevent it

Never store plaintext passwords in config files or scripts

Clear bash history regularly or disable history logging for sensitive commands

Set strict file permissions on config files containing sensitive information
