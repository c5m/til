# Specify SSH key to use
There are several options such as

1. git config
```
git config core.sshCommand 'ssh -i private_key_file'
```
2. SSH config (`~/.ssh/config`)
```
Host gitserv
    Hostname remote.server.com
    IdentityFile ~/.ssh/id_rsa.github
    IdentitiesOnly yes # see NOTES below
```
and then use `git remote add origin git@gitserv:myrepo.git`  

NOTE: The IdentitiesOnly yes is required to prevent the SSH default behavior of sending the identity file matching the default filename for each protocol. If you have a file named ~/.ssh/id_rsa that will get tried BEFORE your ~/.ssh/id_rsa.github without this option.