# RDO

Install & configure RDO

## Requirements

```
```

## Var

```
rdo_repo: https://trunk.rdoproject.org/centos9/component/tripleo/current/python3-tripleo-repos-0.1.1-0.20230111082341.c73cb0f.el9.noarch.rpm
openstack_release: zed
undercloud_public_host: 10.1.1.2
undercloud_admin_host: 10.1.1.3
nodes:
  - name: controller0
    mac_addr: 52:54:00:93:AC:CF
    pm_type: ipmi
    pm_addr: 127.0.0.1
    pm_user: admin
    pm_pass: admin
    pm_port: 6001
    capabilites: "profile:control,boot_option:local"
  - name: controller1
    mac_addr: 52:54:00:97:7A:EF
    pm_type: ipmi
    pm_addr: 127.0.0.1
    pm_user: admin
    pm_pass: admin
    pm_port: 6002
    capabilites: "profile:control,boot_option:local"
  - name: controller2
    mac_addr: 52:54:00:D3:EC:72
    pm_type: ipmi
    pm_addr: 127.0.0.1
    pm_user: admin
    pm_pass: admin
    pm_port: 6003
    capabilites: "profile:control,boot_option:local"
```

## Playbook

```
- name: OSP
  hosts: undercloud
  gather_facts: yes
  roles:
    - rdo
```
