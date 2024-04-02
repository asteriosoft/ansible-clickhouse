Clickhouse
=========

Role for clickhouse deployment and management. 

Role Variables
--------------

To do

Example Playbook
----------------
```
- hosts: servers
  become: yes
  gather_facts: yes

  vars:
    clickhouse_dbs_custom:
      - name: test
        state: present
    clickhouse_users_custom: 
      - name: "admin"
        password: "password"
        host: LOCAL
        grant: 'ALL ON *.*'
        grant_option: true
    clickhouse_prometheus_endpoint: true

  roles:
    - vault
```

