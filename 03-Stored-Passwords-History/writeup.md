# What it is
A privilege escalation technique that involves searching through shell history files for previously executed commands containing passwords or sensitive information.
## How to Find it

cat ~/.bash_history
## How to Prevent it

Clear history files regularly:

bashhistory -c

Disable history logging for sensitive commands by adding a space before them

Never type passwords directly into the terminal — use config files with proper permissions or password managers instead
