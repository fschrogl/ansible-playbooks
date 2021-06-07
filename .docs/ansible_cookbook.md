# Ansible Cookbook

## General

Ansible only executes a play if the final/target state differs from the current state.
Ansible can only determine if states differ when using appropriate modules for tasks
and not general purpose shell commands, hence that's the reason one should use
appropriate modules whenever possible!

## Executing ad-hoc commands

The general pattern for executing ad hoc commands is:

```shell
ansible [pattern] -m [module] -a "[module options]" [--become] [--ask-become-pass]
```

Now some examples:

```shell
# Execute module "ping" on group/hosts
ansible atom -m ping

# Execute an ad-hoc command (default CLI only supports simple things, no pipes etc)
ansible atom -a "/bin/echo hello"

# Execute ad-hoc with builtin shell (for pipes, vars, etc.)
# When using double quotes $TERM would be evaluated on the local machine not on atom!
ansible atom -m ansible.builtin.shell -a 'echo $TERM'

# Execute a single playbook
ansible-playbook mybook.yaml

# Gather facts (information) about a system
ansible atom -m ansible.builtin.setup
```

## Privileges escalation

Privilege escalation is necessary if you want to execute an Ansible command/play
with a user different to the one that started Ansible in the first place.

## Writing playbooks

*todo*
