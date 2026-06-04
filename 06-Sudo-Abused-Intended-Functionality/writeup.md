# Sudo Abused Intended Functionality
Similar to shell escaping but instead of breaking out of a program you abuse its legitimate features to read or write privileged files or execute commands as root.
## How to Find it
sudo -l
## How to Prevent it
only give users sudo access to what they absolutely need

Avoid giving sudo access to file reading or writing tools
