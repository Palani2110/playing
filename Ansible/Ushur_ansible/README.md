## Create playbook
ansible-galaxy init find_java_version

## Set ANSIBLE_CONFIG

```
CWD="$(pwd)"
ANSIBLE_CONFIG = "$CWD/ansible.cfg"
export ANSIBLE_CONFIG
```

## Connectivity check.
* list the ansible hosts

ansible --list-hosts all
ansible --list-hosts ushurplatform_server
ansible ushurplatform_server -m ping -vv

## Copy code int to Jenkins Slave

scp -rp "G:\Other computers\UshurLaptop02\bk_workspace\git_repos\inline_replace" centos@devjs01:/home/centos/bk_workspace



## Execution:
cd /home/centos/bk_workspace/inline_replace
ansible-playbook inline_replace.yml -vv -e ""

