# test-playbook
test playbook to install nginx

# directory layout
https://docs.ansible.com/ansible/2.5/user_guide/playbooks_best_practices.html#directory-layout

# install role
`ansible-galaxy install -r requirements.yml -p roles`

# run playbook, dynamic inventory
`ansible-playbook main.yml`



Alternative, create containers in minikube, and expose, and add to inventory file.

# Starting docker containers in minikube
`minikube start`
`kubectl run debian --image=debian:latest -ndefault --port 22 --command -- sleep 1200`
`kubectl run centos --image=centos:latest -ndefault --port 22 --command -- sleep 1200`

`kubectl expose deployment debian --type=NodePort --name=debian-svc`
`kubectl expose deployment centos --type=NodePort --name=centos-svc`


`minikube ip`
192.168.99.100
