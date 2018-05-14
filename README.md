# rancher-ansible
Ansible playbooks for deploying Rancher 2 with baremetal Kubernetes on Ubuntu 16.04 servers

# Usage

```shell
## Clone repository
git clone https://github.com/gorilych/rancher-ansible.git

## Modify ansible variables describing your environment
vim group_vars/all/vars
# add sensitive information into vault file
rm group_vars/all/vault
ansible-vault create group_vars/all/vault
ansible-vault edit group_vars/all/vault
# add servers with ips into hosts file
vim hosts
# copy license file into path you specified in group_vars/all/vars

## Run playbook for installation, see https://github.com/gorilych/ansible-docker
docker run -ti --rm --volume `pwd`:/ansible gorilych/ansible ansible-playbook site.yml
```
