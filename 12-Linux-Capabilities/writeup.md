# Linux Capabilities
It's a privilege escalation technique that abuses Linux capabilities assigned to binaries. Capabilities give programs specific root powers without full SUID. 
## How to Find it
getcap -r / 2>/dev/null

Look for dangerous capabilities like cap_setuid, cap_net_raw or cap_dac_override.
## How to Prevent it
only assign capabilities that are absolutely necessary

Remove unnecessary capabilities with:

bashsetcap -r /path/to/binary
