# Ansible docs

# Infra setup from scratch

## Pre-tasks

* Make sure that ansible (>=2.16), ansible-playbook and ansible-galaxy are installed
* Get the secret key for the vault and put it in `~/.hackeriet_vault_pass.txt`
  - Doesn't work properly yet, TODO: fix


## Running the playbooks

When all nodes are set up/in Tailscale, run `ansible-playbook playbooks/site.yml` to do the rest of the setup.

## Adding user

To grant youself (or someone else) access, do the following:

1. Add pubkey file to `pubkeys/` named `<username>.pub` i.e. `bob.pub`. Can contain multiple lines, one pubkey per line.
2. Add your username to the list of `ssh_users` in `playbooks/group_vars/all/vars.yml`
