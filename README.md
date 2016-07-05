Role Name
=========

Ansible_PowerVC_deployVM provide a Playbook Ansible to work with PowerVC and Deploy an AIX VM.

Requirements
------------

This Role use the PowerVC API to provide AIX VM. So you must have set a PowerVC System before using it!

Role Variables
--------------

This Role includes any variables that are in vars/main.yml:


- __IP_PVC__		:	 PowerVC server IP or Hostname 
- __URL_PVC__		:	 Url to contact PowerVC server
- __PVC_USER__		:	 PowerVC User login
- __PVC_PWD__		:	 PowerVC User password
- __NETWORK__		:	 Network Name Target available on PowerVC
- __STOR_CONN_GROUP__	:	 Storage Connectivity Group available on PowerVC
- __STOR_TEMPLATE__	:	 Storage Template corresponding to Storage Connectivity Group
- __AGGREGATES__	:	 Host Group available on PowerVC (Be Careful Storage Connectivity Group)
- __PAUSE_IN_SEC__	:	 Pause before Poll Status (secondes)
- __nb_retry__		:	 Retries Number to poll Status 
- __nb_delay__		:	 Delay between Polling (secondes)
- __nb_timeout__	:	 Timeout waiting Active VM (secondes)


Example Playbook
----------------

How to use this role. You must have an AIX image available on PowerVC. For instance, I have an AIX 7.1 TL3 SP5 named here AIX_7100-03_05

```
# ansible-playbook DeployVM_PowerVC.yml -e IMAGE=AIX_7100-03_05
```

Author Information
------------------

Author: Girardin Ludovic

Thanks:
-------
This Role is based on work of the excellent [@chmod666](http://www.chmod666.org).

Many thanks to my colleagues for helping me: [@nanori](https://github.com/nanori), [@Thitho007](https://github.com/Thitho007) ... and After Works ;-)
