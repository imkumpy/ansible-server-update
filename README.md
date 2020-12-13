# Ansible playbook for updating my lab PCs
runs your typical apt/yum update && upgrade depending on OS type and last time server was updated.

If you intend to use this yourself, you will need to recreate the group_vars files and encrypt them with ansible-vault. You can then set up a vault password file called 'vault.pass' (in this example) and set up appropriate permissions for it.
```
ansible-playbook -i inventory.ini --vault-password-file vault.pass playbook.yml
```

You may modify the 'hosts' field in 'playbook.yml' as a way to restrict execution to a specific group of hosts.

'inventory.ini' may be updated to include any new servers.
