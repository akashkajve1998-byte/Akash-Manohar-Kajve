#Introduction to Ansible
● Ansible is an automation tool used for configuration management, application deployment, and task automation.
● In simple terms, it helps us manage multiple servers at the same time without logging into each server manually.
● For example, if I want to install software on 10 servers, I can write an Ansible playbook and run one command, and it will install the software on all servers automatically.
● Ansible is agentless, which means we don’t need to install any extra software on target machines; it works using SSH.
● It uses YAML language to write playbooks, which is easy to read and understand.

*Note:*
GUI version of Ansible is Ansible Automation Platform (old name was Ansible Tower)
CLI version of Ansible i.e opensource version called ansible-core
-------------------------------------------------------------------------------------------------------------------------------------------------------------------------

#Ansible Architecture
+----------------------+
| Control Node |
| (Ansible Installed) |
+----------+-----------+
|
-----------------------------------------
| | |
| | |
+---------+ +---------+ +---------+
|Inventory| |Playbook | | Modules |
|(Hosts) | | (YAML) | | (Tasks) |
+---------+ +---------+ +---------+
|
| SSH (Agentless)
v
-----------------------------------------
| |
+---------------+ +---------------+
| Managed Node | | Managed Node |
| (Server 1) | | (Server 2) |
+---------------+ +---------------+

● Ansible architecture is simple.
● It has two main parts: control node and managed nodes.
○ Control node is the system where Ansible is installed
○ Managed nodes are the target servers.
● Ansible connects to servers using SSH, so no agent is required.
● It uses an inventory file to store server details and playbooks (YAML) to define tasks.


------------------------------------------------------------------------------------------------------------------------------------------------------------------------
#Ansible Flow is: 
Control Node → Inventory → Playbook → Tasks run on Managed Nodes.
