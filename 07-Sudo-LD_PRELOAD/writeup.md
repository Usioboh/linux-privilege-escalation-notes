# Sudo LD_PRELOAD
It's a privilege escalation technique that abuses the LD_PRELOAD environment variable when sudo is configured to preserve it. LD_PRELOAD forces a program to load a specified shared library before anything else.
## How to Find it
sudo -l
## How to Prevent it
Never include LD_PRELOAD in env_keep in the sudoers file

Use env_reset in sudoers to clear all environment variables when running sudo commands
