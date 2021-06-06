# FSDev Ansible Playbooks

Some Ansible playbook for setting up my computers.

## Documentation

* [Ansible @ ArchLinux Wiki](https://wiki.archlinux.org/index.php/Ansible)
* [Ansible Installation Guide](https://docs.ansible.com/ansible/latest/installation_guide/index.html)
* [Ansible User Guide](https://docs.ansible.com/ansible/latest/user_guide/index.html)
  * [Module/Plugin Index](https://docs.ansible.com/ansible/latest/collections/all_plugins.html)
  * [Playbook Reference](https://docs.ansible.com/ansible/latest/reference_appendices/playbooks_keywords.html)

## How to use this repo

### Executing playbooks and roles

This Ansible setup is geared towards my private infrastructure. It can be executed using
``ansible-pull`` or ``ansible`` like so:

```shell
# Using ansible-pull
ansible-pull --only-if-changed --url <this-repos-url>

# Using ansible-playbook on the controller (ion in example)
ansible-playbook local.yml --limit ion --connection local
```
### Required Ansible Modules / Collections

To successfully execute these playbooks some Ansible modules/collections must be available on the controller.
To install an Ansible module/collection execute: 

```shell
ansible-galaxy collection install <collection>
```

Required modules / collections:

* *community.general*

## Disclaimer

Idea for this kind of repo taken from [Jay LaCroix @ LearnLinuxTV](https://github.com/LearnLinuxTV/personal_ansible_desktop_configs.git)
