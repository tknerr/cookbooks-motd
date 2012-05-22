Description
===========

Sets the /etc/motd file so you get a nice message like this upon login:

```
*************************************************
* !!! THIS NODE IS MANAGED BY CHEF !!!
* host 'motd-vm' running on ip 192.168.33.10
* last Chef run was at: 2012-05-22 06:50:22 +0000
*************************************************
Last login: Wed May 16 09:16:33 2012 from 10.0.2.2
vagrant@motd-vm:~$
```

Requirements
============

applicable to systems supporting `/etc/motd` only

Attributes
==========

none

Usage
=====

just add `recipe[motd]` to your node's run_list