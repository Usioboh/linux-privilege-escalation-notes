# SSH Keys
It is a privilege escalation technique that involves finding private SSH keys left on the system with weak permissions.

## Check permissions on keys
ls -la /root/.ssh/

ls -la /home/*/.ssh/

## How to Prevent it
Set strict permissions on SSH keys — private keys should be 600

Never leave private keys in readable locations
