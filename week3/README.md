# Assignment for Week 3

### 1. Remove the `sshd` package

	root@ip-10-0-5-201:/etc/puppet# apt remove openssh-server
	Reading package lists... Done
	Building dependency tree       
	Reading state information... Done
	The following packages will be REMOVED:
  	openssh-server
	0 upgraded, 0 newly installed, 1 to remove and 0 not upgraded.
	After this operation, 898 kB disk space will be freed.
	Do you want to continue? [Y/n] y
	(Reading database ... 59933 files and directories currently installed.)
	Removing openssh-server (1:7.6p1-4ubuntu0.3) ...
	Processing triggers for man-db (2.8.3-2ubuntu0.1) ...

	root@ip-10-0-5-201:/etc/puppet# puppet apply -t /etc/puppet/manifests/site.pp
	Notice: Compiled catalog for ip-10-0-5-201.us-west-2.compute.internal in environment production in 0.41 seconds
	Info: Applying configuration version '1563247871'
	Notice: /Stage[main]/Sshd/Package[openssh-server]/ensure: created
	Notice: Applied catalog in 3.84 seconds


### 2. Stop `sshd`

	root@ip-10-0-5-201:/etc/puppet# systemctl stop sshd

	root@ip-10-0-5-201:/etc/puppet# puppet apply -t /etc/puppet/manifests/site.pp 
	Notice: Compiled catalog for ip-10-0-5-201.us-west-2.compute.internal in environment production in 0.38 seconds
	Info: Applying configuration version '1563248122'
	Notice: /Stage[main]/Sshd/Service[ssh]/ensure: ensure changed 'stopped' to 'running'
	Info: /Stage[main]/Sshd/Service[ssh]: Unscheduling refresh on Service[ssh]
	Notice: Applied catalog in 0.32 seconds


### 3. Modify or delete `/etc/ssh/sshd_config`

- [x] Deleted `/etc/ssh/sshd_config`

		root@ip-10-0-5-201:/etc/ssh# ls -lu
		total 584
		-rw-r--r-- 1 root root 553122 Jul 15 23:12 moduli
		-rw------- 1 root root    668 Jul 15 22:56 ssh_host_dsa_key
		-rw-r--r-- 1 root root    608 Jul 15 22:56 ssh_host_dsa_key.pub
		-rw------- 1 root root    227 Jul 15 22:56 ssh_host_ecdsa_key
		-rw-r--r-- 1 root root    180 Jul 15 22:56 ssh_host_ecdsa_key.pub
		-rw------- 1 root root    411 Jul 15 22:56 ssh_host_ed25519_key
		-rw-r--r-- 1 root root    100 Jul 15 22:56 ssh_host_ed25519_key.pub
		-rw------- 1 root root   1675 Jul 15 22:56 ssh_host_rsa_key
		-rw-r--r-- 1 root root    400 Jul 15 22:56 ssh_host_rsa_key.pub
		-rw-r--r-- 1 root root    338 Jun 27 16:27 ssh_import_id
		-r--r--r-- 1 root root   3262 Jul 16 03:21 sshd_config

		root@ip-10-0-5-201:/etc/ssh# rm sshd_config 

		root@ip-10-0-5-201:/etc/ssh# ls -lu
		total 580
		-rw-r--r-- 1 root root 553122 Jul 15 23:12 moduli
		-rw------- 1 root root    668 Jul 15 22:56 ssh_host_dsa_key
		-rw-r--r-- 1 root root    608 Jul 15 22:56 ssh_host_dsa_key.pub
		-rw------- 1 root root    227 Jul 15 22:56 ssh_host_ecdsa_key
		-rw-r--r-- 1 root root    180 Jul 15 22:56 ssh_host_ecdsa_key.pub
		-rw------- 1 root root    411 Jul 15 22:56 ssh_host_ed25519_key
		-rw-r--r-- 1 root root    100 Jul 15 22:56 ssh_host_ed25519_key.pub
		-rw------- 1 root root   1675 Jul 15 22:56 ssh_host_rsa_key
		-rw-r--r-- 1 root root    400 Jul 15 22:56 ssh_host_rsa_key.pub
		-rw-r--r-- 1 root root    338 Jun 27 16:27 ssh_import_id

		root@ip-10-0-5-201:/etc/ssh# puppet apply -t /etc/puppet/manifests/site.pp 
		Notice: Compiled catalog for ip-10-0-5-201.us-west-2.compute.internal in environment production in 0.39 seconds
		Info: Applying configuration version '1563248430'
		Notice: /Stage[main]/Sshd/File[/etc/ssh/sshd_config]/ensure: defined content as '{md5}203e9b92fe3623aeba277ee44297f7dd'
		Info: /Stage[main]/Sshd/File[/etc/ssh/sshd_config]: Scheduling refresh of Service[ssh]
		Info: /Stage[main]/Sshd/File[/etc/ssh/sshd_config]: Scheduling refresh of Service[ssh]
		Notice: /Stage[main]/Sshd/Service[ssh]: Triggered 'refresh' from 2 events
		Notice: Applied catalog in 0.16 seconds

		root@ip-10-0-5-201:/etc/ssh# ls -lu
		total 584
		-rw-r--r-- 1 root root 553122 Jul 15 23:12 moduli
		-rw------- 1 root root    668 Jul 15 22:56 ssh_host_dsa_key
		-rw-r--r-- 1 root root    608 Jul 15 22:56 ssh_host_dsa_key.pub
		-rw------- 1 root root    227 Jul 15 22:56 ssh_host_ecdsa_key
		-rw-r--r-- 1 root root    180 Jul 15 22:56 ssh_host_ecdsa_key.pub
		-rw------- 1 root root    411 Jul 15 22:56 ssh_host_ed25519_key
		-rw-r--r-- 1 root root    100 Jul 15 22:56 ssh_host_ed25519_key.pub
		-rw------- 1 root root   1675 Jul 15 22:56 ssh_host_rsa_key
		-rw-r--r-- 1 root root    400 Jul 15 22:56 ssh_host_rsa_key.pub
		-rw-r--r-- 1 root root    338 Jun 27 16:27 ssh_import_id
		-r--r--r-- 1 root root   3262 Jul 16 03:40 sshd_config


### 4. Modify or delete `.ssh/authorized_keys` in an instance's user account

- [x] Deleted `.ssh/authorized_keys` 

		root@ip-10-0-5-201:~# cd .ssh/

		root@ip-10-0-5-201:~/.ssh# ls -lu
		total 4
		-rw------- 1 ubuntu ubuntu 964 Jul 16 03:25 authorized_keys

		root@ip-10-0-5-201:~/.ssh# rm authorized_keys 

		root@ip-10-0-5-201:~/.ssh# ls -lu
		total 0

		root@ip-10-0-5-201:~/.ssh# puppet apply -t /etc/puppet/manifests/site.pp 
		Notice: Compiled catalog for ip-10-0-5-201.us-west-2.compute.internal in environment production in 0.39 seconds
		Info: Applying configuration version '1563248623'
		Notice: /Stage[main]/Sshd/Ssh_authorized_key[henzik_key]/ensure: created
		Notice: /Stage[main]/Sshd/Ssh_authorized_key[arobiso2-key-pair]/ensure: created
		Notice: Applied catalog in 0.10 seconds

		root@ip-10-0-5-201:~/.ssh# ls -lu
		total 4
		-rw------- 1 ubuntu ubuntu 964 Jul 16 03:43 authorized_keys

