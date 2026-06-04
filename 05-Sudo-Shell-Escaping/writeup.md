# Sudo Shell Escaping
It's a privilege escalation technique that abuses programs a user is allowed to run with sudo.
## How to find
sudo -l

Then look up the binary on GTFOBins to find the escape method.
## How to Prevent it
Only grant sudo access to commands that absolutely need it

Avoid giving sudo access to text editors, interpreters or programs with shell features
