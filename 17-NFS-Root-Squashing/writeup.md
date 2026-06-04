# What it is
NFS (Network File System) allows a machine to share folders over a network. Root squashing is a security feature that prevents root on a client machine from having root access on the NFS share.
Root squashing enabled = safe
Root squashing disabled = vulnerable
If root squashing is disabled you can create a SUID binary on the NFS share from your attacking machine and execute it on the target to get root.

## How to Find it
On the target machine check what NFS shares exist:

cat /etc/exports

Look for shares with no_root_squash:

/tmp *(rw,sync,insecure,no_root_squash,no_subtree_check)

That no_root_squash is your vulnerability.
## How To Prevent
Enable Root Squashing

Root squashing is configured in the /etc/exports file on the NFS server.

Vulnerable configuration (no_root_squash):

/tmp *(rw,sync,insecure,no_root_squash)

Secure configuration (root_squash):

/tmp *(rw,sync,insecure,root_squash)

Just replace no_root_squash with root_squash.
