# FSDev Ansible Playbooks

Some Ansible playbook for setting up my computers.

## Documentation

* [Ansible Installation Guide](https://docs.ansible.com/ansible/latest/installation_guide/index.html)
* [Ansible User Guide](https://docs.ansible.com/ansible/latest/user_guide/index.html)
* [Ansible @ ArchLinux Wiki](https://wiki.archlinux.org/index.php/Ansible)

## How to use this repo

This Ansible setup is geared towards my private infrastructure. It can be executed using
``ansible-pull`` or ``ansible`` like so:

```shell
# Using ansible-pull
ansible-pull --only-if-changed -U <this-repos-url>

# Using plain ansible
ansible ...
```

## Disclaimer

Idea for this kind of repo taken from [Jay LaCroix @ LearnLinuxTV](https://github.com/LearnLinuxTV/personal_ansible_desktop_configs.git)
