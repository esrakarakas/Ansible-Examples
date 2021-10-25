# Trendyol-DevOps-Case


This repository contains the Ansible installation files of applications for Centos 7.

Host addresses bind to 0.0.0.0 for be able to access applications after installations.


## Requirements:
- OS: Centos 7
- Ansible must be installed.
- Host name and Ansible user should be edited in the hosts file.


## Installations:

### Kubernetes Installation:
This step creates a Kubernetes cluster consisting of 1 master and 1 worker node.

```shell
cd build-k8s
ansible-playbook -i hosts main.yml -k -K
```

### ELK Installation:

- Elasticsearch: http://8.208.14.99:9200/ 
- Kibana: http://8.208.14.99:5602/

```shell
cd install-ELK
ansible-playbook main.yml -k -K
```

### Consul Server Installation:

- Consul: http://8.208.92.184:8500 

```shell
cd install-consul
ansible-playbook -i hosts main.yml -k -K
```

### Deploy Prometheus on Kubernetes:

```shell
cd prometheus-on-k8s
ansible-playbook -i hosts main.yml -k -K
```

### Gitlab Installation:

- Gitlab: http://8.208.14.99/ 

```shell
cd install-gitlab
ansible-playbook -i hosts.target gitlab-ce.yml -k -K
```


