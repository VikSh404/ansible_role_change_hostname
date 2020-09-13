# ansible_role_change_hostname

### Required inventory:
```ansible
[all:vars]
ansible_user='root'
all_swarm_labels='["master", "worker", "postgresql", "rabbitmq"]'

[initial_manager]
10.10.10.1

[managers]
10.10.10.1

[nodes]
10.10.10.1 hostname="manager_01" swarm_labels='["master"]'
10.10.10.2 hostname="worker_01" swarm_labels='["worker", "postgresql"]'
10.10.10.3 hostname="worker_02" swarm_labels='["worker", "rabbitmq"]'
10.10.10.3 hostname="worker_03" swarm_labels='["worker", "rabbitmq"]'


[workers]
10.10.10.2
10.10.10.3
10.10.10.3

```
