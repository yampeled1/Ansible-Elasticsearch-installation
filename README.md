# Elasticsearch-installation-automation
An Ansible playbook installing Elasticsearch from scratch
## Prerequisites

- Ansible installed on master server
- Ansible superuser privileges on target server

## Execution example

```
ansible-playbook elastic_search_v1.yaml 
```

### Output example

A short example of an output
- in this case installing Elastic search from master server "yamp1" on target server "yamp2"

```
[ansible@yamp1 playbooks]$ ansible-playbook elastic_search_v1.yaml 
[DEPRECATION WARNING]: DEFAULT_SUDO_USER option, In favor of Ansible Become, which is a generic 
framework. See become_user. , use become instead. This feature will be removed in version 2.8. 
Deprecation warnings can be disabled by setting deprecation_warnings=False in ansible.cfg.

PLAY [elastic_search_v1.yaml ] ***************************************************************************************

TASK [Gathering Facts] ******************************************************************************
ok: [yamp2.mylabserver.com]

TASK [Installing Java version 1.8-openjdk] **********************************************************
changed: [yamp2.mylabserver.com]

TASK [install the elastic search rpm from a remote repo] ********************************************
changed: [yamp2.mylabserver.com]

TASK [Make sure elastic search service is running] **************************************************
changed: [yamp2.mylabserver.com]

PLAY RECAP ******************************************************************************************
yamp2.mylabserver.com   : ok=4    changed=3    unreachable=0    failed=0   



```

## Built With

* [Bash](https://www.gnu.org/software/bash/) - The GNU Project's shell
* [Ansible](https://www.ansible.com/) - Simple, agentless IT automation
* [Elastic-search](https://www.elastic.co/) -  distributed, JSON-based search and analytics engine designed for horizontal scalability, maximum reliability, and easy management.
## Versioning

Untill this point there is only ver 1.0

## Authors

* [Yam Peled](https://github.com/yampeled1)
