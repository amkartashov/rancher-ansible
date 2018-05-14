# rancher-ansible
Ansible playbooks for deploying Rancher 2 with baremetal Kubernetes on Ubuntu 16.04 servers

# Usage

Note: to use [ansible-docker](https://github.com/gorilych/ansible-docker), prepend ansible commands with `docker run -ti --rm --volume \`pwd\`:/ansible gorilych/ansible`

```shell
# clone repository
git clone https://github.com/gorilych/rancher-ansible.git
# modify ansible variables describing your environment
vim group_vars/all/vars
# add sensitive information into vault file
rm group_vars/all/vault
ansible-vault create group_vars/all/vault
ansible-vault edit group_vars/all/vault
# add servers with ips into hosts file
vim hosts

# run playbook
ansible-playbook site.yml
```
