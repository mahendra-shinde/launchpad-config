## Generate and Copy NEW SSH-Keys on all nodes

```
# Use Git Bash on Windows OR bash on linux/mac
$ ssh-keygen 
# Copy KEY to first node 
# [replace master with masternode IP address, user with username]
$ ssh-copy-id user@master
Enter password: [USERPASSWORD]
# Test connection 
$ ssh user@master
## NOW, YOU MUST BE INSIDE MASTER NODE
$ exit
## NOW, COPY KEY TO NEXT NODEs
$ ssh-copy-id user@node1
Enter password: [USERPASSWORD]
$ ssh-copy-id user@node2
Enter password: [USERPASSWORD]
```

## Enable Password-less SUDO access in all three nodes

```
# for Master node (repeate the same steps for all other nodes)
$ ssh user@master
$ cd /etc/sudoers.d/
# PLEASE REPLACE [USER] with actual username
# eg. mahendra-user if username is 'mahendra'
$ sudo nano [user]-user
Enter password: [USERPASSWORD]
# Copy following line (replace [USER] with actual username)
[USER] ALL=(ALL) NOPASSWD:ALL
# PRESS CTRL+X ENTER Y ENTER
```

