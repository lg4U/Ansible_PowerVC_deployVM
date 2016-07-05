Role Name
=========

Ansible_PowerVC_deployVM provide a Playbook Ansible to work with PowerVC and Deploy an AIX VM.

Requirements
------------

This Role use the PowerVC API to provide AIX VM. So you must have set a PowerVC System before using it!

Role Variables
--------------

This Role includes any variables that are in vars/main.yml:

	* **IP_PVC**		:	 PowerVC server IP or Hostname 
	* **URL_PVC**		:	 Url to contact PowerVC server
	* **PVC_USER**		:	 PowerVC User login
	* **PVC_PWD**		:	 PowerVC User password
	* **NETWORK**		:	 Network Name Target available on PowerVC
	* **STOR_CONN_GROUP**	:	 Storage Connectivity Group available on PowerVC
	* **STOR_TEMPLATE**	:	 Storage Template corresponding to Storage Connectivity Group
	* **AGGREGATES**	:	 Host Group available on PowerVC (Be Careful Storage Connectivity Group)
	* **PAUSE_IN_SEC**	:	 Pause before Poll Status (secondes)
	* **nb_retry**		:	 Retries Number to poll Status 
	* **nb_delay**		:	 Delay between Polling (secondes)
	* **nb_timeout**	:	 Timeout waiting Active VM (secondes)

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
