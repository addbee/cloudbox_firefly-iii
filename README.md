# cloudbox_mod-firefly-iii
Firefly ansible role for Cloudbox based on cloudbox_mod template

- [Firefly iii](https://github.com/firefly-iii/firefly-iii) - a self-hosted financial manager
- [Cloudbox](https://github.com/Cloudbox/Cloudbox) - Automated Cloud Media Server


## How to use

1. Clone this repo:
1. CD into the repo folder:
1. If you have an Ansible vault password file, add the location to `ansible.cfg`:

    To edit:

    ```bash
    nano ~/cloudbox_mod/ansible.cfg
    ```

    Add line (with path to your vault password file):
    ```ini
    vault_password_file = ~/.ansible_vault
    ```

    Final result:
    ```ini
    [defaults]
    inventory = ~/cloudbox/inventories/local
    callback_whitelist = profile_tasks
    command_warnings = False
    retry_files_enabled = False
    hash_behaviour = merge
    role_path = ~/cloudbox/roles
    vault_password_file = ~/.ansible_vault
    ```
1. Run the Ansible role:

    ```bash
    sudo ansible-playbook cloudbox_mod.yml --tags firefly 
    ```
