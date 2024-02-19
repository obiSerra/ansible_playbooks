# Ansible playbooks

Collection of Ansible playbooks for various tasks.


## Requirements

- file `inventory.ini` in the root directory of the repository containing the hosts
- file `.vault_key` in the root directory of the repository containing the vault password
- file `resources/hosts_password.yml` containing the password for the hosts encrypted with the vault password


## Usage

```bash

$ ansible-playbook --extra-vars @resources/hosts_password.yml --vault-password-file .vault_key <playbook>.yml
```
## Playbooks

- `bootstrap.yml` - Setup a new host with all the basic tools
- `adafruit-lcd.yml` - Install Adafruit LCD and run the stats script
