# Overview

This is a simple script to update a remote host's certificate store with an enterprise's Man-In-The-Middle (MITM) root certificate.

Update the value of `local_cert_file` variable in the `playbook.yml` with the actual path of the ROOT certificate (in PEM format) placed somewhere in the host system.

Please make sure to update the `group_vars/all/vault.yml` with the relevant sensitive data of remote server IPs and ssh user id using the command

`ansible-vault edit group_vars/all/vault.yml`

### Executing playbook

```
$ ansible-playbook -i hosts -kK -v --ask-vault-pass playbook.yml
```
