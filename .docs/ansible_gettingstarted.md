# Ansible Crashcourse

## Glossary

* **Inventory** - index with all nodes that should be managed with/by Ansible
* **Collections** - can be downloaded from Ansible Galaxy (community work)
* **Modules** - for using commands/programms within playbooks/tasks
* **Tasks** - unit of action in Ansible. Each Tasks calls an Ansible module.
* **Play** - consists of one or more Tasks
* **Playbooks** - contains one or more Plays
* **Roles** - describes the desired role of a host (e.g. Webserver, DB server, etc.)

## Ansible Basics

* Playbooks are executed from top to bottom
* Tasks are also executed from top to bottom
