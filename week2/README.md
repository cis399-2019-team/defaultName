# Assignment for Week 2: Amazon EC2 Instance Creation

### 1. List the EC2 instance IDs and private IP addresses of all the instances you created

- Austin:
	- i-0b41c232eabc69685
	- 10.0.5.44

- Henzi:
	- i-06e909ea13daeda7f
	- 10.0.5.66


### 2. Describe how you find the public IP address of a given instance using the EC2 console

- In the 'Instances' tab in the AWS, in the IPv4 Public IP column


### 3. Provide the output of a command showing how much disk space one of your instances has

	ubuntu@ip-10-0-5-66:~$ df
	Filesystem     1K-blocks    Used Available Use% Mounted on
	udev              233616       0    233616   0% /dev
	tmpfs              49144     748     48396   2% /run
	/dev/xvda1       8065444 1353944   6695116  17% /
	tmpfs             245712       0    245712   0% /dev/shm
	tmpfs               5120       0      5120   0% /run/lock
	tmpfs             245712       0    245712   0% /sys/fs/cgroup
	/dev/loop0         90624   90624         0 100% /snap/core/7169
	/dev/loop1         18432   18432         0 100% /snap/amazon-ssm-agent/1335
	/dev/loop2         90624   90624         0 100% /snap/core/7270
	tmpfs              49140       0     49140   0% /run/user/1000
   

### 4. Provide the output of a command showing how much memory one of your instances has

	ubuntu@ip-10-0-5-44:~$ free -m
	              total        used        free      shared  buff/cache   available
	Mem:            479         100          49           0         330         366
	Swap:             0           0           0


### 5. Provide a listing showing all the processes running in one of your instances

	ubuntu@ip-10-0-5-44:~$ ps -A
	  PID TTY          TIME CMD
	    1 ?        00:00:02 systemd
	    2 ?        00:00:00 kthreadd
	    4 ?        00:00:00 kworker/0:0H
	    6 ?        00:00:00 mm_percpu_wq
	    7 ?        00:00:00 ksoftirqd/0
	    8 ?        00:00:00 rcu_sched
	    9 ?        00:00:00 rcu_bh
	   10 ?        00:00:00 migration/0
	   11 ?        00:00:00 watchdog/0
	   12 ?        00:00:00 cpuhp/0
	   13 ?        00:00:00 kdevtmpfs
	   14 ?        00:00:00 netns
	   15 ?        00:00:00 rcu_tasks_kthre
	   16 ?        00:00:00 kauditd
	   17 ?        00:00:00 xenbus
	   18 ?        00:00:00 xenwatch
	   19 ?        00:00:00 kworker/0:1
	   20 ?        00:00:00 khungtaskd
	   21 ?        00:00:00 oom_reaper
	   22 ?        00:00:00 writeback
	   23 ?        00:00:00 kcompactd0
	   24 ?        00:00:00 ksmd
	   25 ?        00:00:00 crypto
	   26 ?        00:00:00 kintegrityd
	   27 ?        00:00:00 kblockd
	   28 ?        00:00:00 ata_sff
	   29 ?        00:00:00 md
	   30 ?        00:00:00 edac-poller
	   31 ?        00:00:00 devfreq_wq
	   32 ?        00:00:00 watchdogd
	   35 ?        00:00:00 kswapd0
	   36 ?        00:00:00 kworker/u31:0
	   37 ?        00:00:00 ecryptfs-kthrea
	   79 ?        00:00:00 kthrotld
	   80 ?        00:00:00 nvme-wq
	   81 ?        00:00:00 scsi_eh_0
	   82 ?        00:00:00 scsi_tmf_0
	   83 ?        00:00:00 scsi_eh_1
	   84 ?        00:00:00 scsi_tmf_1
	   89 ?        00:00:00 ipv6_addrconf
	   99 ?        00:00:00 kstrp
	  169 ?        00:00:00 kworker/0:1H
	  277 ?        00:00:00 raid5wq
	  328 ?        00:00:00 jbd2/xvda1-8
	  329 ?        00:00:00 ext4-rsv-conver
	  395 ?        00:00:00 iscsi_eh
	  402 ?        00:00:00 systemd-journal
	  404 ?        00:00:00 ib-comp-wq
	  405 ?        00:00:00 ib_mcast
	  406 ?        00:00:00 ib_nl_sa_wq
	  409 ?        00:00:00 rdma_cm
	  412 ?        00:00:00 kworker/0:2
	  415 ?        00:00:00 lvmetad
	  421 ?        00:00:00 systemd-udevd
	  525 ?        00:00:00 systemd-timesyn
	  623 ?        00:00:00 systemd-network
	  646 ?        00:00:00 systemd-resolve
	  780 ?        00:00:00 networkd-dispat
	  789 ?        00:00:00 accounts-daemon
	  793 ?        00:00:00 rsyslogd
	  795 ?        00:00:00 cron
	  798 ?        00:00:00 systemd-logind
	  799 ?        00:00:00 atd
	  801 ?        00:00:00 lxcfs
	  803 ?        00:00:00 dbus-daemon
	  814 ?        00:00:00 unattended-upgr
	  841 ?        00:00:00 polkitd
	  849 ttyS0    00:00:00 agetty
	  856 tty1     00:00:00 agetty
	  943 ?        00:00:00 sshd
	 1051 ?        00:00:00 loop0
	 1109 ?        00:00:00 snapd
	 1211 ?        00:00:00 loop1
	 1264 ?        00:00:00 amazon-ssm-agen
	 1443 ?        00:00:00 kworker/u30:2
	 1525 ?        00:00:00 sshd
	 1529 ?        00:00:00 systemd
	 1537 ?        00:00:00 (sd-pam)
	 1640 ?        00:00:00 sshd
	 1643 pts/0    00:00:00 bash
	 1662 ?        00:00:00 kworker/u30:1
	 1663 ?        00:00:00 sshd
	 1729 ?        00:00:00 sshd
	 1730 pts/1    00:00:00 bash
	 1754 pts/1    00:00:00 top
	 1765 pts/1    00:00:00 ps
 

### 6. Provide the output of a command showing the network interface configuration of your instance (this should show its private IP address)

	ubuntu@ip-10-0-5-44:~$ ifconfig
	eth0: flags=4163<UP,BROADCAST,RUNNING,MULTICAST>  mtu 9001
	        inet 10.0.5.44  netmask 255.255.255.0  broadcast 10.0.5.255
	        inet6 fe80::813:92ff:fedc:cd62  prefixlen 64  scopeid 0x20<link>
	        ether 0a:13:92:dc:cd:62  txqueuelen 1000  (Ethernet)
	        RX packets 2620  bytes 663736 (663.7 KB)
	        RX errors 0  dropped 0  overruns 0  frame 0
	        TX packets 7068  bytes 1514297 (1.5 MB)
	        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

	lo: flags=73<UP,LOOPBACK,RUNNING>  mtu 65536
	        inet 127.0.0.1  netmask 255.0.0.0
	        inet6 ::1  prefixlen 128  scopeid 0x10<host>
	        loop  txqueuelen 1000  (Local Loopback)
	        RX packets 176  bytes 14432 (14.4 KB)
	        RX errors 0  dropped 0  overruns 0  frame 0
	        TX packets 176  bytes 14432 (14.4 KB)
	        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0


### 7. Provide the output of a command showing the routing table of your instance

	ubuntu@ip-10-0-5-44:~$ route -e
	Kernel IP routing table
	Destination     Gateway         Genmask         Flags   MSS Window  irtt Iface
	default         ip-10-0-5-1.us- 0.0.0.0         UG        0 0          0 eth0
	10.0.5.0        0.0.0.0         255.255.255.0   U         0 0          0 eth0
	ip-10-0-5-1.us- 0.0.0.0         255.255.255.255 UH        0 0          0 eth0


### 8. Provide the output of a command showing all of the open network connections and ports on one of your instances

	ubuntu@ip-10-0-5-44:~$ netstat -at
	Active Internet connections (servers and established)
	Proto Recv-Q Send-Q Local Address           Foreign Address         State
	tcp        0      0 localhost:domain        0.0.0.0:*               LISTEN
	tcp        0      0 0.0.0.0:ssh             0.0.0.0:*               LISTEN
	tcp        0      0 ip-10-0-5-44.us-wes:ssh wlan-nat-outside-:53856 ESTABLISHED
	tcp        0    316 ip-10-0-5-44.us-wes:ssh wlan-nat-outside-:64827 ESTABLISHED
	tcp6       0      0 [::]:ssh                [::]:*                  LISTEN


### 9. Provide a listing of all of the software packages installed on one your instances

	ubuntu@ip-10-0-5-44:~$ apt list --installed
	Listing... Done
	accountsservice/bionic,now 0.6.45-1ubuntu1 amd64 [installed,automatic]
	acl/bionic,now 2.2.52-3build1 amd64 [installed,automatic]
	acpid/bionic,now 1:2.0.28-1ubuntu1 amd64 [installed,automatic]
	adduser/bionic,now 3.116ubuntu1 all [installed,automatic]
	apparmor/bionic-updates,bionic-security,now 2.12-4ubuntu5.1 amd64 [installed,automatic]
	apport/bionic-updates,now 2.20.9-0ubuntu7.6 all [installed,automatic]
	apport-symptoms/bionic,now 0.20 all [installed,automatic]
	apt/bionic-updates,now 1.6.11 amd64 [installed,automatic]
	apt-utils/bionic-updates,now 1.6.11 amd64 [installed,automatic]
	at/bionic,now 3.1.20-3.1ubuntu2 amd64 [installed,automatic]
	base-files/bionic-updates,now 10.1ubuntu2.4 amd64 [installed,automatic]
	base-passwd/bionic,now 3.5.44 amd64 [installed,automatic]
	bash/bionic-updates,now 4.4.18-2ubuntu1.1 amd64 [installed]
	bash-completion/bionic,now 1:2.8-1ubuntu1 all [installed,automatic]
	bc/bionic,now 1.07.1-2 amd64 [installed,automatic]
	bcache-tools/bionic,now 1.0.8-2build1 amd64 [installed,automatic]
	bind9-host/bionic-updates,bionic-security,now 1:9.11.3+dfsg-1ubuntu1.8 amd64 [installed,automatic]
	bsdmainutils/bionic,now 11.1.2ubuntu1 amd64 [installed,automatic]
	bsdutils/bionic-updates,now 1:2.31.1-0.4ubuntu3.3 amd64 [installed,automatic]
	btrfs-progs/bionic,now 4.15.1-1build1 amd64 [installed,automatic]
	btrfs-tools/bionic,now 4.15.1-1build1 amd64 [installed,automatic]
	busybox-initramfs/bionic-updates,bionic-security,now 1:1.27.2-2ubuntu3.2 amd64 [installed,automatic]
	busybox-static/bionic-updates,bionic-security,now 1:1.27.2-2ubuntu3.2 amd64 [installed,automatic]
	byobu/bionic,now 5.125-0ubuntu1 all [installed,automatic]
	bzip2/bionic-updates,bionic-security,now 1.0.6-8.1ubuntu0.1 amd64 [installed,automatic]
	ca-certificates/bionic,bionic-updates,now 20180409 all [installed,automatic]
	cloud-guest-utils/bionic,now 0.30-0ubuntu5 all [installed,automatic]
	cloud-init/bionic-updates,now 19.1-1-gbaa47854-0ubuntu1~18.04.1 all [installed]
	cloud-initramfs-copymods/bionic-updates,now 0.40ubuntu1.1 all [installed,automatic]
	cloud-initramfs-dyn-netconf/bionic-updates,now 0.40ubuntu1.1 all [installed,automatic]
	command-not-found/bionic-updates,now 18.04.5 all [installed,automatic]
	command-not-found-data/bionic-updates,now 18.04.5 amd64 [installed,automatic]
	console-setup/bionic-updates,now 1.178ubuntu2.9 all [installed,automatic]
	console-setup-linux/bionic-updates,now 1.178ubuntu2.9 all [installed,automatic]
	coreutils/bionic,now 8.28-1ubuntu1 amd64 [installed,automatic]
	cpio/bionic,now 2.12+dfsg-6 amd64 [installed,automatic]
	cron/bionic,now 3.0pl1-128.1ubuntu1 amd64 [installed,automatic]
	cryptsetup/bionic-updates,now 2:2.0.2-1ubuntu1.1 amd64 [installed,automatic]
	cryptsetup-bin/bionic-updates,now 2:2.0.2-1ubuntu1.1 amd64 [installed,automatic]
	curl/bionic-updates,bionic-security,now 7.58.0-2ubuntu3.7 amd64 [installed,automatic]
	dash/bionic,now 0.5.8-2.10 amd64 [installed]
	dbus/bionic-updates,bionic-security,now 1.12.2-1ubuntu1.1 amd64 [installed,automatic]
	debconf/bionic-updates,now 1.5.66ubuntu1 all [installed,automatic]
	debconf-i18n/bionic-updates,now 1.5.66ubuntu1 all [installed,automatic]
	debianutils/bionic,now 4.8.4 amd64 [installed,automatic]
	diffutils/bionic,now 1:3.6-1 amd64 [installed]
	dirmngr/bionic-updates,bionic-security,now 2.2.4-1ubuntu1.2 amd64 [installed,automatic]
	distro-info-data/bionic-updates,bionic-security,now 0.37ubuntu0.5 all [installed,automatic]
	dmeventd/bionic,now 2:1.02.145-4.1ubuntu3 amd64 [installed,automatic]
	dmidecode/bionic,now 3.1-1 amd64 [installed,automatic]
	dmsetup/bionic,now 2:1.02.145-4.1ubuntu3 amd64 [installed,automatic]
	dns-root-data/bionic,now 2018013001 all [installed,automatic]
	dnsmasq-base/bionic,now 2.79-1 amd64 [installed,automatic]
	dnsutils/bionic-updates,bionic-security,now 1:9.11.3+dfsg-1ubuntu1.8 amd64 [installed,automatic]
	dosfstools/bionic,now 4.1-1 amd64 [installed,automatic]
	dpkg/bionic-updates,now 1.19.0.5ubuntu2.1 amd64 [installed,automatic]
	e2fsprogs/bionic-updates,now 1.44.1-1ubuntu1.1 amd64 [installed,automatic]
	eatmydata/bionic,now 105-6 all [installed]
	ebtables/bionic-updates,now 2.0.10.4-3.5ubuntu2.18.04.3 amd64 [installed,automatic]
	ed/bionic,now 1.10-2.1 amd64 [installed,automatic]
	eject/bionic,now 2.1.5+deb1+cvs20081104-13.2 amd64 [installed,automatic]
	ethtool/bionic,now 1:4.15-0ubuntu1 amd64 [installed,automatic]
	fdisk/bionic-updates,now 2.31.1-0.4ubuntu3.3 amd64 [installed,automatic]
	file/bionic-updates,bionic-security,now 1:5.32-2ubuntu0.2 amd64 [installed,automatic]
	findutils/bionic,now 4.6.0+git+20170828-2 amd64 [installed]
	fonts-ubuntu-console/bionic,now 0.83-2 all [installed,automatic]
	friendly-recovery/bionic-updates,now 0.2.38ubuntu1 all [installed,automatic]
	ftp/bionic,now 0.17-34 amd64 [installed,automatic]
	fuse/bionic,now 2.9.7-1ubuntu1 amd64 [installed,automatic]
	gawk/bionic,now 1:4.1.4+dfsg-1build1 amd64 [installed,automatic]
	gcc-8-base/bionic-updates,bionic-security,now 8.3.0-6ubuntu1~18.04.1 amd64 [installed,automatic]
	gdisk/bionic,now 1.0.3-1 amd64 [installed,automatic]
	geoip-database/bionic,now 20180315-1 all [installed,automatic]
	gettext-base/bionic-updates,bionic-security,now 0.19.8.1-6ubuntu0.3 amd64 [installed,automatic]
	gir1.2-glib-2.0/bionic,now 1.56.1-1 amd64 [installed,automatic]
	git/bionic-updates,bionic-security,now 1:2.17.1-1ubuntu0.4 amd64 [installed,automatic]
	git-man/bionic-updates,bionic-security,now 1:2.17.1-1ubuntu0.4 all [installed,automatic]
	gnupg/bionic-updates,bionic-security,now 2.2.4-1ubuntu1.2 amd64 [installed,automatic]
	gnupg-l10n/bionic-updates,bionic-security,now 2.2.4-1ubuntu1.2 all [installed,automatic]
	gnupg-utils/bionic-updates,bionic-security,now 2.2.4-1ubuntu1.2 amd64 [installed,automatic]
	gpg/bionic-updates,bionic-security,now 2.2.4-1ubuntu1.2 amd64 [installed,automatic]
	gpg-agent/bionic-updates,bionic-security,now 2.2.4-1ubuntu1.2 amd64 [installed,automatic]
	gpg-wks-client/bionic-updates,bionic-security,now 2.2.4-1ubuntu1.2 amd64 [installed,automatic]
	gpg-wks-server/bionic-updates,bionic-security,now 2.2.4-1ubuntu1.2 amd64 [installed,automatic]
	gpgconf/bionic-updates,bionic-security,now 2.2.4-1ubuntu1.2 amd64 [installed,automatic]
	gpgsm/bionic-updates,bionic-security,now 2.2.4-1ubuntu1.2 amd64 [installed,automatic]
	gpgv/bionic-updates,bionic-security,now 2.2.4-1ubuntu1.2 amd64 [installed,automatic]
	grep/bionic,now 3.1-2 amd64 [installed]
	groff-base/bionic,now 1.22.3-10 amd64 [installed,automatic]
	grub-common/bionic-updates,now 2.02-2ubuntu8.13 amd64 [installed,automatic]
	grub-gfxpayload-lists/bionic,now 0.7 amd64 [installed,automatic]
	grub-legacy-ec2/bionic,now 1:1 all [installed,automatic]
	grub-pc/bionic-updates,now 2.02-2ubuntu8.13 amd64 [installed,automatic]
	grub-pc-bin/bionic-updates,now 2.02-2ubuntu8.13 amd64 [installed,automatic]
	grub2-common/bionic-updates,now 2.02-2ubuntu8.13 amd64 [installed,automatic]
	gzip/bionic,now 1.6-5ubuntu1 amd64 [installed]
	hdparm/bionic,now 9.54+ds-1 amd64 [installed,automatic]
	hibagent/bionic,now 1.0.1-0ubuntu1 all [installed]
	hostname/bionic,now 3.20 amd64 [installed]
	htop/bionic,now 2.1.0-3 amd64 [installed,automatic]
	info/bionic,now 6.5.0.dfsg.1-2 amd64 [installed,automatic]
	init/bionic,now 1.51 amd64 [installed]
	init-system-helpers/bionic,now 1.51 all [installed,automatic]
	initramfs-tools/bionic-updates,now 0.130ubuntu3.8 all [installed,automatic]
	initramfs-tools-bin/bionic-updates,now 0.130ubuntu3.8 amd64 [installed,automatic]
	initramfs-tools-core/bionic-updates,now 0.130ubuntu3.8 all [installed,automatic]
	install-info/bionic,now 6.5.0.dfsg.1-2 amd64 [installed,automatic]
	iproute2/bionic,now 4.15.0-2ubuntu1 amd64 [installed,automatic]
	iptables/bionic,now 1.6.1-2ubuntu2 amd64 [installed,automatic]
	iputils-ping/bionic,now 3:20161105-1ubuntu2 amd64 [installed,automatic]
	iputils-tracepath/bionic,now 3:20161105-1ubuntu2 amd64 [installed,automatic]
	irqbalance/bionic-updates,now 1.3.0-0.1ubuntu0.18.04.1 amd64 [installed,automatic]
	isc-dhcp-client/bionic-updates,bionic-security,now 4.3.5-3ubuntu7.1 amd64 [installed,automatic]
	isc-dhcp-common/bionic-updates,bionic-security,now 4.3.5-3ubuntu7.1 amd64 [installed,automatic]
	iso-codes/bionic,now 3.79-1 all [installed,automatic]
	kbd/bionic,now 2.0.4-2ubuntu1 amd64 [installed,automatic]
	keyboard-configuration/bionic-updates,now 1.178ubuntu2.9 all [installed,automatic]
	klibc-utils/bionic,now 2.0.4-9ubuntu2 amd64 [installed,automatic]
	kmod/bionic-updates,now 24-1ubuntu3.2 amd64 [installed,automatic]
	krb5-locales/bionic-updates,bionic-security,now 1.16-2ubuntu0.1 all [installed,automatic]
	landscape-common/bionic-updates,now 18.01-0ubuntu3.3 amd64 [installed,automatic]
	language-selector-common/bionic-updates,now 0.188.2 all [installed,automatic]
	less/bionic,now 487-0.1 amd64 [installed,automatic]
	libaccountsservice0/bionic,now 0.6.45-1ubuntu1 amd64 [installed,automatic]
	libacl1/bionic,now 2.2.52-3build1 amd64 [installed,automatic]
	libapparmor1/bionic-updates,bionic-security,now 2.12-4ubuntu5.1 amd64 [installed,automatic]
	libapt-inst2.0/bionic-updates,now 1.6.11 amd64 [installed,automatic]
	libapt-pkg5.0/bionic-updates,now 1.6.11 amd64 [installed,automatic]
	libargon2-0/bionic,now 0~20161029-1.1 amd64 [installed,automatic]
	libasn1-8-heimdal/bionic,now 7.5.0+dfsg-1 amd64 [installed,automatic]
	libassuan0/bionic,now 2.5.1-2 amd64 [installed,automatic]
	libatm1/bionic,now 1:2.5.1-2build1 amd64 [installed,automatic]
	libattr1/bionic,now 1:2.4.47-2build1 amd64 [installed,automatic]
	libaudit-common/bionic,now 1:2.8.2-1ubuntu1 all [installed,automatic]
	libaudit1/bionic,now 1:2.8.2-1ubuntu1 amd64 [installed,automatic]
	libbind9-160/bionic-updates,bionic-security,now 1:9.11.3+dfsg-1ubuntu1.8 amd64 [installed,automatic]
	libblkid1/bionic-updates,now 2.31.1-0.4ubuntu3.3 amd64 [installed,automatic]
	libbsd0/bionic,now 0.8.7-1 amd64 [installed,automatic]
	libbz2-1.0/bionic-updates,bionic-security,now 1.0.6-8.1ubuntu0.1 amd64 [installed,automatic]
	libc-bin/bionic,now 2.27-3ubuntu1 amd64 [installed,automatic]
	libc6/bionic,now 2.27-3ubuntu1 amd64 [installed,automatic]
	libcap-ng0/bionic,now 0.7.7-3.1 amd64 [installed,automatic]
	libcap2/bionic,now 1:2.25-1.2 amd64 [installed,automatic]
	libcap2-bin/bionic,now 1:2.25-1.2 amd64 [installed,automatic]
	libcom-err2/bionic-updates,now 1.44.1-1ubuntu1.1 amd64 [installed,automatic]
	libcryptsetup12/bionic-updates,now 2:2.0.2-1ubuntu1.1 amd64 [installed,automatic]
	libcurl3-gnutls/bionic-updates,bionic-security,now 7.58.0-2ubuntu3.7 amd64 [installed,automatic]
	libcurl4/bionic-updates,bionic-security,now 7.58.0-2ubuntu3.7 amd64 [installed,automatic]
	libdb5.3/bionic-updates,bionic-security,now 5.3.28-13.1ubuntu1.1 amd64 [installed,automatic]
	libdbus-1-3/bionic-updates,bionic-security,now 1.12.2-1ubuntu1.1 amd64 [installed,automatic]
	libdebconfclient0/bionic,now 0.213ubuntu1 amd64 [installed,automatic]
	libdevmapper-event1.02.1/bionic,now 2:1.02.145-4.1ubuntu3 amd64 [installed,automatic]
	libdevmapper1.02.1/bionic,now 2:1.02.145-4.1ubuntu3 amd64 [installed,automatic]
	libdns-export1100/bionic-updates,bionic-security,now 1:9.11.3+dfsg-1ubuntu1.8 amd64 [installed,automatic]
	libdns1100/bionic-updates,bionic-security,now 1:9.11.3+dfsg-1ubuntu1.8 amd64 [installed,automatic]
	libdrm-common/bionic-updates,now 2.4.95-1~18.04.1 all [installed,automatic]
	libdrm2/bionic-updates,now 2.4.95-1~18.04.1 amd64 [installed,automatic]
	libdumbnet1/bionic,now 1.12-7build1 amd64 [installed,automatic]
	libeatmydata1/bionic,now 105-6 amd64 [installed]
	libedit2/bionic,now 3.1-20170329-1 amd64 [installed,automatic]
	libelf1/bionic-updates,bionic-security,now 0.170-0.4ubuntu0.1 amd64 [installed,automatic]
	liberror-perl/bionic,now 0.17025-1 all [installed,automatic]
	libestr0/bionic,now 0.1.10-2.1 amd64 [installed,automatic]
	libevent-2.1-6/bionic,now 2.1.8-stable-4build1 amd64 [installed,automatic]
	libexpat1/bionic-updates,bionic-security,now 2.2.5-3ubuntu0.1 amd64 [installed,automatic]
	libext2fs2/bionic-updates,now 1.44.1-1ubuntu1.1 amd64 [installed,automatic]
	libfastjson4/bionic,now 0.99.8-2 amd64 [installed,automatic]
	libfdisk1/bionic-updates,now 2.31.1-0.4ubuntu3.3 amd64 [installed,automatic]
	libffi6/bionic,now 3.2.1-8 amd64 [installed,automatic]
	libfreetype6/bionic,now 2.8.1-2ubuntu2 amd64 [installed,automatic]
	libfribidi0/bionic,now 0.19.7-2 amd64 [installed,automatic]
	libfuse2/bionic,now 2.9.7-1ubuntu1 amd64 [installed,automatic]
	libgcc1/bionic-updates,bionic-security,now 1:8.3.0-6ubuntu1~18.04.1 amd64 [installed,automatic]
	libgcrypt20/bionic-updates,bionic-security,now 1.8.1-4ubuntu1.1 amd64 [installed,automatic]
	libgdbm-compat4/bionic,now 1.14.1-6 amd64 [installed,automatic]
	libgdbm5/bionic,now 1.14.1-6 amd64 [installed,automatic]
	libgeoip1/bionic,now 1.6.12-1 amd64 [installed,automatic]
	libgirepository-1.0-1/bionic,now 1.56.1-1 amd64 [installed,automatic]
	libglib2.0-0/bionic-updates,bionic-security,now 2.56.4-0ubuntu0.18.04.3 amd64 [installed,automatic]
	libglib2.0-data/bionic-updates,bionic-security,now 2.56.4-0ubuntu0.18.04.3 all [installed,automatic]
	libgmp10/bionic,now 2:6.1.2+dfsg-2 amd64 [installed,automatic]
	libgnutls30/bionic-updates,bionic-security,now 3.5.18-1ubuntu1.1 amd64 [installed,automatic]
	libgpg-error0/bionic,now 1.27-6 amd64 [installed,automatic]
	libgpm2/bionic,now 1.20.7-5 amd64 [installed,automatic]
	libgssapi-krb5-2/bionic-updates,bionic-security,now 1.16-2ubuntu0.1 amd64 [installed,automatic]
	libgssapi3-heimdal/bionic,now 7.5.0+dfsg-1 amd64 [installed,automatic]
	libhcrypto4-heimdal/bionic,now 7.5.0+dfsg-1 amd64 [installed,automatic]
	libheimbase1-heimdal/bionic,now 7.5.0+dfsg-1 amd64 [installed,automatic]
	libheimntlm0-heimdal/bionic,now 7.5.0+dfsg-1 amd64 [installed,automatic]
	libhogweed4/bionic,now 3.4-1 amd64 [installed,automatic]
	libhx509-5-heimdal/bionic,now 7.5.0+dfsg-1 amd64 [installed,automatic]
	libicu60/bionic,now 60.2-3ubuntu3 amd64 [installed,automatic]
	libidn11/bionic-updates,now 1.33-2.1ubuntu1.2 amd64 [installed,automatic]
	libidn2-0/bionic,now 2.0.4-1.1build2 amd64 [installed,automatic]
	libip4tc0/bionic,now 1.6.1-2ubuntu2 amd64 [installed,automatic]
	libip6tc0/bionic,now 1.6.1-2ubuntu2 amd64 [installed,automatic]
	libiptc0/bionic,now 1.6.1-2ubuntu2 amd64 [installed,automatic]
	libirs160/bionic-updates,bionic-security,now 1:9.11.3+dfsg-1ubuntu1.8 amd64 [installed,automatic]
	libisc-export169/bionic-updates,bionic-security,now 1:9.11.3+dfsg-1ubuntu1.8 amd64 [installed,automatic]
	libisc169/bionic-updates,bionic-security,now 1:9.11.3+dfsg-1ubuntu1.8 amd64 [installed,automatic]
	libisccc160/bionic-updates,bionic-security,now 1:9.11.3+dfsg-1ubuntu1.8 amd64 [installed,automatic]
	libisccfg160/bionic-updates,bionic-security,now 1:9.11.3+dfsg-1ubuntu1.8 amd64 [installed,automatic]
	libisns0/bionic,now 0.97-2build1 amd64 [installed,automatic]
	libjson-c3/bionic,now 0.12.1-1.3 amd64 [installed,automatic]
	libk5crypto3/bionic-updates,bionic-security,now 1.16-2ubuntu0.1 amd64 [installed,automatic]
	libkeyutils1/bionic,now 1.5.9-9.2ubuntu2 amd64 [installed,automatic]
	libklibc/bionic,now 2.0.4-9ubuntu2 amd64 [installed,automatic]
	libkmod2/bionic-updates,now 24-1ubuntu3.2 amd64 [installed,automatic]
	libkrb5-26-heimdal/bionic,now 7.5.0+dfsg-1 amd64 [installed,automatic]
	libkrb5-3/bionic-updates,bionic-security,now 1.16-2ubuntu0.1 amd64 [installed,automatic]
	libkrb5support0/bionic-updates,bionic-security,now 1.16-2ubuntu0.1 amd64 [installed,automatic]
	libksba8/bionic,now 1.3.5-2 amd64 [installed,automatic]
	libldap-2.4-2/bionic-updates,now 2.4.45+dfsg-1ubuntu1.2 amd64 [installed,automatic]
	libldap-common/bionic-updates,now 2.4.45+dfsg-1ubuntu1.2 all [installed,automatic]
	liblocale-gettext-perl/bionic,now 1.07-3build2 amd64 [installed,automatic]
	liblvm2app2.2/bionic,now 2.02.176-4.1ubuntu3 amd64 [installed,automatic]
	liblvm2cmd2.02/bionic,now 2.02.176-4.1ubuntu3 amd64 [installed,automatic]
	liblwres160/bionic-updates,bionic-security,now 1:9.11.3+dfsg-1ubuntu1.8 amd64 [installed,automatic]
	liblxc-common/bionic-updates,now 3.0.3-0ubuntu1~18.04.1 amd64 [installed,automatic]
	liblxc1/bionic-updates,now 3.0.3-0ubuntu1~18.04.1 amd64 [installed,automatic]
	liblz4-1/bionic,now 0.0~r131-2ubuntu3 amd64 [installed,automatic]
	liblzma5/bionic,now 5.2.2-1.3 amd64 [installed,automatic]
	liblzo2-2/bionic,now 2.08-1.2 amd64 [installed,automatic]
	libmagic-mgc/bionic-updates,bionic-security,now 1:5.32-2ubuntu0.2 amd64 [installed,automatic]
	libmagic1/bionic-updates,bionic-security,now 1:5.32-2ubuntu0.2 amd64 [installed,automatic]
	libmnl0/bionic,now 1.0.4-2 amd64 [installed,automatic]
	libmount1/bionic-updates,now 2.31.1-0.4ubuntu3.3 amd64 [installed,automatic]
	libmpdec2/bionic,now 2.4.2-1ubuntu1 amd64 [installed,automatic]
	libmpfr6/bionic,now 4.0.1-1 amd64 [installed,automatic]
	libmspack0/bionic-updates,bionic-security,now 0.6-3ubuntu0.2 amd64 [installed,automatic]
	libncurses5/bionic-updates,now 6.1-1ubuntu1.18.04 amd64 [installed,automatic]
	libncursesw5/bionic-updates,now 6.1-1ubuntu1.18.04 amd64 [installed,automatic]
	libnetfilter-conntrack3/bionic,now 1.0.6-2 amd64 [installed,automatic]
	libnettle6/bionic,now 3.4-1 amd64 [installed,automatic]
	libnewt0.52/bionic,now 0.52.20-1ubuntu1 amd64 [installed,automatic]
	libnfnetlink0/bionic,now 1.0.1-3 amd64 [installed,automatic]
	libnghttp2-14/bionic,now 1.30.0-1ubuntu1 amd64 [installed,automatic]
	libnih1/bionic,now 1.0.3-6ubuntu2 amd64 [installed,automatic]
	libnpth0/bionic,now 1.5-3 amd64 [installed,automatic]
	libnss-systemd/bionic-updates,now 237-3ubuntu10.23 amd64 [installed,automatic]
	libntfs-3g88/bionic-updates,bionic-security,now 1:2017.3.23-2ubuntu0.18.04.2 amd64 [installed,automatic]
	libnuma1/bionic-updates,now 2.0.11-2.1ubuntu0.1 amd64 [installed,automatic]
	libp11-kit0/bionic,now 0.23.9-2 amd64 [installed,automatic]
	libpam-cap/bionic,now 1:2.25-1.2 amd64 [installed,automatic]
	libpam-modules/bionic-updates,now 1.1.8-3.6ubuntu2.18.04.1 amd64 [installed,automatic]
	libpam-modules-bin/bionic-updates,now 1.1.8-3.6ubuntu2.18.04.1 amd64 [installed,automatic]
	libpam-runtime/bionic-updates,now 1.1.8-3.6ubuntu2.18.04.1 all [installed,automatic]
	libpam-systemd/bionic-updates,now 237-3ubuntu10.23 amd64 [installed,automatic]
	libpam0g/bionic-updates,now 1.1.8-3.6ubuntu2.18.04.1 amd64 [installed,automatic]
	libparted2/bionic-updates,now 3.2-20ubuntu0.2 amd64 [installed,automatic]
	libpcap0.8/bionic,now 1.8.1-6ubuntu1 amd64 [installed,automatic]
	libpci3/bionic-updates,now 1:3.5.2-1ubuntu1.1 amd64 [installed,automatic]
	libpcre3/bionic,now 2:8.39-9 amd64 [installed,automatic]
	libperl5.26/bionic-updates,bionic-security,now 5.26.1-6ubuntu0.3 amd64 [installed,automatic]
	libpipeline1/bionic,now 1.5.0-1 amd64 [installed,automatic]
	libplymouth4/bionic-updates,now 0.9.3-1ubuntu7.18.04.2 amd64 [installed,automatic]
	libpng16-16/bionic-updates,bionic-security,now 1.6.34-1ubuntu0.18.04.2 amd64 [installed,automatic]
	libpolkit-agent-1-0/bionic-updates,bionic-security,now 0.105-20ubuntu0.18.04.5 amd64 [installed,automatic]
	libpolkit-backend-1-0/bionic-updates,bionic-security,now 0.105-20ubuntu0.18.04.5 amd64 [installed,automatic]
	libpolkit-gobject-1-0/bionic-updates,bionic-security,now 0.105-20ubuntu0.18.04.5 amd64 [installed,automatic]
	libpopt0/bionic,now 1.16-11 amd64 [installed,automatic]
	libprocps6/bionic-updates,bionic-security,now 2:3.3.12-3ubuntu1.1 amd64 [installed,automatic]
	libpsl5/bionic,now 0.19.1-5build1 amd64 [installed,automatic]
	libpython3-stdlib/bionic-updates,now 3.6.7-1~18.04 amd64 [installed,automatic]
	libpython3.6/bionic-updates,now 3.6.8-1~18.04.1 amd64 [installed,automatic]
	libpython3.6-minimal/bionic-updates,now 3.6.8-1~18.04.1 amd64 [installed,automatic]
	libpython3.6-stdlib/bionic-updates,now 3.6.8-1~18.04.1 amd64 [installed,automatic]
	libreadline5/bionic,now 5.2+dfsg-3build1 amd64 [installed,automatic]
	libreadline7/bionic,now 7.0-3 amd64 [installed,automatic]
	libroken18-heimdal/bionic,now 7.5.0+dfsg-1 amd64 [installed,automatic]
	librtmp1/bionic,now 2.4+20151223.gitfa8646d.1-1 amd64 [installed,automatic]
	libsasl2-2/bionic,now 2.1.27~101-g0780600+dfsg-3ubuntu2 amd64 [installed,automatic]
	libsasl2-modules/bionic,now 2.1.27~101-g0780600+dfsg-3ubuntu2 amd64 [installed,automatic]
	libsasl2-modules-db/bionic,now 2.1.27~101-g0780600+dfsg-3ubuntu2 amd64 [installed,automatic]
	libseccomp2/bionic-updates,bionic-security,now 2.4.1-0ubuntu0.18.04.2 amd64 [installed,automatic]
	libselinux1/bionic,now 2.7-2build2 amd64 [installed,automatic]
	libsemanage-common/bionic,now 2.7-2build2 all [installed,automatic]
	libsemanage1/bionic,now 2.7-2build2 amd64 [installed,automatic]
	libsepol1/bionic,now 2.7-1 amd64 [installed,automatic]
	libsigsegv2/bionic,now 2.12-1 amd64 [installed,automatic]
	libslang2/bionic,now 2.3.1a-3ubuntu1 amd64 [installed,automatic]
	libsmartcols1/bionic-updates,now 2.31.1-0.4ubuntu3.3 amd64 [installed,automatic]
	libsqlite3-0/bionic-updates,bionic-security,now 3.22.0-1ubuntu0.1 amd64 [installed,automatic]
	libss2/bionic-updates,now 1.44.1-1ubuntu1.1 amd64 [installed,automatic]
	libssl1.0.0/bionic-updates,bionic-security,now 1.0.2n-1ubuntu5.3 amd64 [installed,automatic]
	libssl1.1/bionic-updates,now 1.1.1-1ubuntu2.1~18.04.3 amd64 [installed,automatic]
	libstdc++6/bionic-updates,bionic-security,now 8.3.0-6ubuntu1~18.04.1 amd64 [installed,automatic]
	libsystemd0/bionic-updates,now 237-3ubuntu10.23 amd64 [installed,automatic]
	libtasn1-6/bionic,now 4.13-2 amd64 [installed,automatic]
	libtext-charwidth-perl/bionic,now 0.04-7.1 amd64 [installed,automatic]
	libtext-iconv-perl/bionic,now 1.7-5build6 amd64 [installed,automatic]
	libtext-wrapi18n-perl/bionic,now 0.06-7.1 all [installed,automatic]
	libtinfo5/bionic-updates,now 6.1-1ubuntu1.18.04 amd64 [installed,automatic]
	libudev1/bionic-updates,now 237-3ubuntu10.23 amd64 [installed,automatic]
	libunistring2/bionic-updates,now 0.9.9-0ubuntu2 amd64 [installed,automatic]
	libunwind8/bionic,now 1.2.1-8 amd64 [installed,automatic]
	libusb-1.0-0/bionic,now 2:1.0.21-2 amd64 [installed,automatic]
	libutempter0/bionic,now 1.1.6-3 amd64 [installed,automatic]
	libuuid1/bionic-updates,now 2.31.1-0.4ubuntu3.3 amd64 [installed,automatic]
	libuv1/bionic,now 1.18.0-3 amd64 [installed,automatic]
	libwind0-heimdal/bionic,now 7.5.0+dfsg-1 amd64 [installed,automatic]
	libwrap0/bionic,now 7.6.q-27 amd64 [installed]
	libx11-6/bionic-updates,now 2:1.6.4-3ubuntu0.2 amd64 [installed,automatic]
	libx11-data/bionic-updates,now 2:1.6.4-3ubuntu0.2 all [installed,automatic]
	libxau6/bionic,now 1:1.0.8-1 amd64 [installed,automatic]
	libxcb1/bionic-updates,now 1.13-2~ubuntu18.04 amd64 [installed,automatic]
	libxdmcp6/bionic,now 1:1.1.2-3 amd64 [installed,automatic]
	libxext6/bionic,now 2:1.3.3-1 amd64 [installed,automatic]
	libxml2/bionic-updates,bionic-security,now 2.9.4+dfsg1-6.1ubuntu1.2 amd64 [installed,automatic]
	libxmlsec1/bionic,now 1.2.25-1build1 amd64 [installed,automatic]
	libxmlsec1-openssl/bionic,now 1.2.25-1build1 amd64 [installed,automatic]
	libxmuu1/bionic,now 2:1.1.2-2 amd64 [installed,automatic]
	libxslt1.1/bionic-updates,bionic-security,now 1.1.29-5ubuntu0.1 amd64 [installed,automatic]
	libxtables12/bionic,now 1.6.1-2ubuntu2 amd64 [installed,automatic]
	libyaml-0-2/bionic,now 0.1.7-2ubuntu3 amd64 [installed,automatic]
	libzstd1/bionic,now 1.3.3+dfsg-2ubuntu1 amd64 [installed,automatic]
	linux-aws/now 4.15.0.1043.42 amd64 [installed,local]
	linux-aws-headers-4.15.0-1043/now 4.15.0-1043.45 all [installed,local]
	linux-base/bionic,now 4.5ubuntu1 all [installed,automatic]
	linux-headers-4.15.0-1043-aws/now 4.15.0-1043.45 amd64 [installed,local]
	linux-headers-aws/now 4.15.0.1043.42 amd64 [installed,local]
	linux-image-4.15.0-1043-aws/now 4.15.0-1043.45 amd64 [installed,local]
	linux-image-aws/now 4.15.0.1043.42 amd64 [installed,local]
	linux-modules-4.15.0-1043-aws/now 4.15.0-1043.45 amd64 [installed,local]
	locales/bionic,now 2.27-3ubuntu1 all [installed,automatic]
	login/bionic-updates,now 1:4.5-1ubuntu2 amd64 [installed]
	logrotate/bionic,now 3.11.0-0.1ubuntu1 amd64 [installed,automatic]
	lsb-base/bionic,now 9.20170808ubuntu1 all [installed,automatic]
	lsb-release/bionic,now 9.20170808ubuntu1 all [installed,automatic]
	lshw/bionic-updates,now 02.18-0.1ubuntu6.18.04.1 amd64 [installed,automatic]
	lsof/bionic,now 4.89+dfsg-0.1 amd64 [installed,automatic]
	ltrace/bionic,now 0.7.3-6ubuntu1 amd64 [installed,automatic]
	lvm2/bionic,now 2.02.176-4.1ubuntu3 amd64 [installed,automatic]
	lxcfs/bionic-updates,now 3.0.3-0ubuntu1~18.04.1 amd64 [installed,automatic]
	lxd/bionic-updates,now 3.0.3-0ubuntu1~18.04.1 amd64 [installed,automatic]
	lxd-client/bionic-updates,now 3.0.3-0ubuntu1~18.04.1 amd64 [installed,automatic]
	man-db/bionic-updates,now 2.8.3-2ubuntu0.1 amd64 [installed,automatic]
	manpages/bionic,now 4.15-1 all [installed,automatic]
	mawk/bionic,now 1.3.3-17ubuntu3 amd64 [installed,automatic]
	mdadm/bionic-updates,now 4.1~rc1-3~ubuntu18.04.2 amd64 [installed,automatic]
	mime-support/bionic,now 3.60ubuntu1 all [installed,automatic]
	mlocate/bionic,now 0.26-2ubuntu3.1 amd64 [installed,automatic]
	mount/bionic-updates,now 2.31.1-0.4ubuntu3.3 amd64 [installed,automatic]
	mtr-tiny/bionic,now 0.92-1 amd64 [installed,automatic]
	multiarch-support/bionic,now 2.27-3ubuntu1 amd64 [installed,automatic]
	nano/bionic,now 2.9.3-2 amd64 [installed,automatic]
	ncurses-base/bionic-updates,now 6.1-1ubuntu1.18.04 all [installed]
	ncurses-bin/bionic-updates,now 6.1-1ubuntu1.18.04 amd64 [installed]
	ncurses-term/bionic-updates,now 6.1-1ubuntu1.18.04 all [installed]
	net-tools/bionic,now 1.60+git20161116.90da8a0-1ubuntu1 amd64 [installed,automatic]
	netbase/bionic,now 5.4 all [installed,automatic]
	netcat-openbsd/bionic-updates,now 1.187-1ubuntu0.1 amd64 [installed,automatic]
	netplan.io/bionic-updates,now 0.97-0ubuntu1~18.04.1 amd64 [installed,automatic]
	networkd-dispatcher/bionic-updates,now 1.7-0ubuntu3.3 all [installed,automatic]
	nplan/bionic-updates,now 0.97-0ubuntu1~18.04.1 all [installed,automatic]
	ntfs-3g/bionic-updates,bionic-security,now 1:2017.3.23-2ubuntu0.18.04.2 amd64 [installed,automatic]
	open-iscsi/bionic-updates,now 2.0.874-5ubuntu2.7 amd64 [installed,automatic]
	open-vm-tools/bionic-updates,now 2:10.3.10-1~ubuntu0.18.04.1 amd64 [installed,automatic]
	openssh-client/bionic-updates,bionic-security,now 1:7.6p1-4ubuntu0.3 amd64 [installed,automatic]
	openssh-server/bionic-updates,bionic-security,now 1:7.6p1-4ubuntu0.3 amd64 [installed]
	openssh-sftp-server/bionic-updates,bionic-security,now 1:7.6p1-4ubuntu0.3 amd64 [installed]
	openssl/bionic-updates,now 1.1.1-1ubuntu2.1~18.04.3 amd64 [installed,automatic]
	os-prober/bionic,now 1.74ubuntu1 amd64 [installed,automatic]
	overlayroot/bionic-updates,now 0.40ubuntu1.1 all [installed,automatic]
	parted/bionic-updates,now 3.2-20ubuntu0.2 amd64 [installed,automatic]
	passwd/bionic-updates,now 1:4.5-1ubuntu2 amd64 [installed,automatic]
	pastebinit/bionic,now 1.5-2 all [installed,automatic]
	patch/bionic,now 2.7.6-2ubuntu1 amd64 [installed,automatic]
	pciutils/bionic-updates,now 1:3.5.2-1ubuntu1.1 amd64 [installed,automatic]
	perl/bionic-updates,bionic-security,now 5.26.1-6ubuntu0.3 amd64 [installed,automatic]
	perl-base/bionic-updates,bionic-security,now 5.26.1-6ubuntu0.3 amd64 [installed,automatic]
	perl-modules-5.26/bionic-updates,bionic-security,now 5.26.1-6ubuntu0.3 all [installed,automatic]
	pinentry-curses/bionic,now 1.1.0-1 amd64 [installed,automatic]
	plymouth/bionic-updates,now 0.9.3-1ubuntu7.18.04.2 amd64 [installed,automatic]
	plymouth-theme-ubuntu-text/bionic-updates,now 0.9.3-1ubuntu7.18.04.2 amd64 [installed,automatic]
	policykit-1/bionic-updates,bionic-security,now 0.105-20ubuntu0.18.04.5 amd64 [installed,automatic]
	pollinate/bionic-updates,now 4.33-0ubuntu1~18.04.1 all [installed,automatic]
	popularity-contest/bionic,now 1.66ubuntu1 all [installed,automatic]
	powermgmt-base/bionic,now 1.33 all [installed,automatic]
	procps/bionic-updates,bionic-security,now 2:3.3.12-3ubuntu1.1 amd64 [installed,automatic]
	psmisc/bionic-updates,now 23.1-1ubuntu0.1 amd64 [installed,automatic]
	publicsuffix/bionic,now 20180223.1310-1 all [installed,automatic]
	python-apt-common/bionic-updates,now 1.6.4 all [installed,automatic]
	python3/bionic-updates,now 3.6.7-1~18.04 amd64 [installed,automatic]
	python3-apport/bionic-updates,now 2.20.9-0ubuntu7.6 all [installed,automatic]
	python3-apt/bionic-updates,now 1.6.4 amd64 [installed,automatic]
	python3-asn1crypto/bionic,now 0.24.0-1 all [installed,automatic]
	python3-attr/bionic,now 17.4.0-2 all [installed,automatic]
	python3-automat/bionic,now 0.6.0-1 all [installed,automatic]
	python3-blinker/bionic,now 1.4+dfsg1-0.1 all [installed]
	python3-certifi/bionic,now 2018.1.18-2 all [installed,automatic]
	python3-cffi-backend/bionic,now 1.11.5-1 amd64 [installed,automatic]
	python3-chardet/bionic,now 3.0.4-1 all [installed,automatic]
	python3-click/bionic,now 6.7-3 all [installed,automatic]
	python3-colorama/bionic,now 0.3.7-1 all [installed,automatic]
	python3-commandnotfound/bionic-updates,now 18.04.5 all [installed,automatic]
	python3-configobj/bionic,now 5.0.6-2 all [installed,automatic]
	python3-constantly/bionic,now 15.1.0-1 all [installed,automatic]
	python3-cryptography/bionic-updates,now 2.1.4-1ubuntu1.3 amd64 [installed,automatic]
	python3-dbus/bionic,now 1.2.6-1 amd64 [installed,automatic]
	python3-debconf/bionic-updates,now 1.5.66ubuntu1 all [installed,automatic]
	python3-debian/bionic,now 0.1.32 all [installed,automatic]
	python3-distro-info/bionic-updates,now 0.18ubuntu0.18.04.1 all [installed,automatic]
	python3-distupgrade/bionic-updates,now 1:18.04.33 all [installed,automatic]
	python3-gdbm/bionic-updates,now 3.6.8-1~18.04 amd64 [installed,automatic]
	python3-gi/bionic-updates,now 3.26.1-2ubuntu1 amd64 [installed,automatic]
	python3-httplib2/bionic-updates,now 0.9.2+dfsg-1ubuntu0.1 all [installed,automatic]
	python3-hyperlink/bionic,now 17.3.1-2 all [installed,automatic]
	python3-idna/bionic,now 2.6-1 all [installed,automatic]
	python3-incremental/bionic,now 16.10.1-3 all [installed,automatic]
	python3-jinja2/bionic-updates,bionic-security,now 2.10-1ubuntu0.18.04.1 all [installed]
	python3-json-pointer/bionic,now 1.10-1 all [installed]
	python3-jsonpatch/bionic,now 1.19+really1.16-1fakesync1 all [installed]
	python3-jsonschema/bionic,now 2.6.0-2 all [installed]
	python3-jwt/bionic,now 1.5.3+ds1-1 all [installed]
	python3-markupsafe/bionic,now 1.0-1build1 amd64 [installed]
	python3-minimal/bionic-updates,now 3.6.7-1~18.04 amd64 [installed,automatic]
	python3-netifaces/bionic,now 0.10.4-0.1build4 amd64 [installed,automatic]
	python3-newt/bionic,now 0.52.20-1ubuntu1 amd64 [installed,automatic]
	python3-oauthlib/bionic,now 2.0.6-1 all [installed]
	python3-openssl/bionic,now 17.5.0-1ubuntu1 all [installed,automatic]
	python3-pam/bionic,now 0.4.2-13.2ubuntu4 amd64 [installed,automatic]
	python3-pkg-resources/bionic,now 39.0.1-2 all [installed,automatic]
	python3-problem-report/bionic-updates,now 2.20.9-0ubuntu7.6 all [installed,automatic]
	python3-pyasn1/bionic,now 0.4.2-3 all [installed,automatic]
	python3-pyasn1-modules/bionic,now 0.2.1-0.2 all [installed,automatic]
	python3-requests/bionic-updates,bionic-security,now 2.18.4-2ubuntu0.1 all [installed,automatic]
	python3-requests-unixsocket/bionic,now 0.1.5-3 all [installed,automatic]
	python3-serial/bionic,now 3.4-2 all [installed,automatic]
	python3-service-identity/bionic,now 16.0.0-2 all [installed,automatic]
	python3-six/bionic,now 1.11.0-2 all [installed,automatic]
	python3-software-properties/bionic-updates,now 0.96.24.32.9 all [installed,automatic]
	python3-systemd/bionic,now 234-1build1 amd64 [installed,automatic]
	python3-twisted/bionic,now 17.9.0-2 all [installed,automatic]
	python3-twisted-bin/bionic,now 17.9.0-2 amd64 [installed,automatic]
	python3-update-manager/bionic-updates,now 1:18.04.11.10 all [installed,automatic]
	python3-urllib3/bionic-updates,bionic-security,now 1.22-1ubuntu0.18.04.1 all [installed,automatic]
	python3-yaml/bionic,now 3.12-1build2 amd64 [installed,automatic]
	python3-zope.interface/bionic,now 4.3.2-1build2 amd64 [installed,automatic]
	python3.6/bionic-updates,now 3.6.8-1~18.04.1 amd64 [installed,automatic]
	python3.6-minimal/bionic-updates,now 3.6.8-1~18.04.1 amd64 [installed,automatic]
	readline-common/bionic,now 7.0-3 all [installed,automatic]
	rsync/bionic,now 3.1.2-2.1ubuntu1 amd64 [installed,automatic]
	rsyslog/bionic,now 8.32.0-1ubuntu4 amd64 [installed,automatic]
	run-one/bionic,now 1.17-0ubuntu1 all [installed,automatic]
	screen/bionic-updates,now 4.6.2-1ubuntu1 amd64 [installed,automatic]
	sed/bionic,now 4.4-2 amd64 [installed,automatic]
	sensible-utils/bionic,now 0.0.12 all [installed,automatic]
	shared-mime-info/bionic,now 1.9-2 amd64 [installed,automatic]
	snapd/bionic-updates,now 2.39.2+18.04 amd64 [installed,automatic]
	software-properties-common/bionic-updates,now 0.96.24.32.9 all [installed,automatic]
	sosreport/bionic-updates,now 3.6-1ubuntu0.18.04.2 amd64 [installed,automatic]
	squashfs-tools/bionic-updates,now 1:4.3-6ubuntu0.18.04.1 amd64 [installed,automatic]
	ssh-import-id/bionic-updates,now 5.7-0ubuntu1.1 all [installed]
	strace/bionic,now 4.21-1ubuntu1 amd64 [installed,automatic]
	sudo/bionic,now 1.8.21p2-3ubuntu1 amd64 [installed,automatic]
	systemd/bionic-updates,now 237-3ubuntu10.23 amd64 [installed,automatic]
	systemd-sysv/bionic-updates,now 237-3ubuntu10.23 amd64 [installed,automatic]
	sysvinit-utils/bionic,now 2.88dsf-59.10ubuntu1 amd64 [installed]
	tar/bionic-updates,now 1.29b-2ubuntu0.1 amd64 [installed,automatic]
	tcpdump/bionic,now 4.9.2-3 amd64 [installed,automatic]
	telnet/bionic,now 0.17-41 amd64 [installed,automatic]
	time/bionic,now 1.7-25.1build1 amd64 [installed,automatic]
	tmux/bionic-updates,now 2.6-3ubuntu0.1 amd64 [installed,automatic]
	tzdata/bionic-updates,bionic-security,now 2019a-0ubuntu0.18.04 all [installed,automatic]
	ubuntu-advantage-tools/bionic,now 17 all [installed,automatic]
	ubuntu-keyring/bionic-updates,now 2018.09.18.1~18.04.0 all [installed,automatic]
	ubuntu-minimal/bionic-updates,now 1.417.1 amd64 [installed]
	ubuntu-release-upgrader-core/bionic-updates,now 1:18.04.33 all [installed,automatic]
	ubuntu-server/bionic-updates,now 1.417.1 amd64 [installed]
	ubuntu-standard/bionic-updates,now 1.417.1 amd64 [installed]
	ucf/bionic,now 3.0038 all [installed,automatic]
	udev/bionic-updates,now 237-3ubuntu10.23 amd64 [installed,automatic]
	ufw/bionic-updates,now 0.36-0ubuntu0.18.04.1 all [installed,automatic]
	uidmap/bionic-updates,now 1:4.5-1ubuntu2 amd64 [installed,automatic]
	unattended-upgrades/bionic-updates,now 1.1ubuntu1.18.04.11 all [installed,automatic]
	update-manager-core/bionic-updates,now 1:18.04.11.10 all [installed,automatic]
	update-notifier-common/bionic-updates,now 3.192.1.7 all [installed,automatic]
	ureadahead/bionic-updates,now 0.100.0-21 amd64 [installed,automatic]
	usbutils/bionic,now 1:007-4build1 amd64 [installed,automatic]
	util-linux/bionic-updates,now 2.31.1-0.4ubuntu3.3 amd64 [installed,automatic]
	uuid-runtime/bionic-updates,now 2.31.1-0.4ubuntu3.3 amd64 [installed,automatic]
	vim/bionic-updates,bionic-security,now 2:8.0.1453-1ubuntu1.1 amd64 [installed,automatic]
	vim-common/bionic-updates,bionic-security,now 2:8.0.1453-1ubuntu1.1 all [installed,automatic]
	vim-runtime/bionic-updates,bionic-security,now 2:8.0.1453-1ubuntu1.1 all [installed,automatic]
	vim-tiny/bionic-updates,bionic-security,now 2:8.0.1453-1ubuntu1.1 amd64 [installed,automatic]
	wget/bionic-updates,bionic-security,now 1.19.4-1ubuntu2.2 amd64 [installed,automatic]
	whiptail/bionic,now 0.52.20-1ubuntu1 amd64 [installed,automatic]
	xauth/bionic,now 1:1.0.10-1 amd64 [installed,automatic]
	xdelta3/bionic,now 3.0.11-dfsg-1ubuntu1 amd64 [installed,automatic]
	xdg-user-dirs/bionic,now 0.17-1ubuntu1 amd64 [installed,automatic]
	xfsprogs/bionic,now 4.9.0+nmu1ubuntu2 amd64 [installed,automatic]
	xkb-data/bionic,now 2.23.1-1ubuntu1 all [installed,automatic]
	xxd/bionic-updates,bionic-security,now 2:8.0.1453-1ubuntu1.1 amd64 [installed,automatic]
	xz-utils/bionic,now 5.2.2-1.3 amd64 [installed,automatic]
	zerofree/bionic,now 1.0.4-1 amd64 [installed,automatic]
	zlib1g/bionic,now 1:1.2.11.dfsg-0ubuntu2 amd64 [installed,automatic]


### 10. Provide transcripts showing the output of the commands you use to update your package database and upgrade packages on each of your instances

	ubuntu@ip-10-0-5-66:~$ sudo apt-get update
	Hit:1 http://us-west-2.ec2.archive.ubuntu.com/ubuntu bionic InRelease
	Get:2 http://us-west-2.ec2.archive.ubuntu.com/ubuntu bionic-updates InRelease [88.7 kB]
	Get:3 http://us-west-2.ec2.archive.ubuntu.com/ubuntu bionic-backports InRelease [74.6 kB]
	Get:4 http://security.ubuntu.com/ubuntu bionic-security InRelease [88.7 kB]
	Get:5 http://us-west-2.ec2.archive.ubuntu.com/ubuntu bionic-updates/main amd64 Packages [682 kB]
	Get:6 http://us-west-2.ec2.archive.ubuntu.com/ubuntu bionic-updates/main Translation-en [251 kB]   
	Get:7 http://us-west-2.ec2.archive.ubuntu.com/ubuntu bionic-updates/universe amd64 Packages [970 kB]
	Get:8 http://us-west-2.ec2.archive.ubuntu.com/ubuntu bionic-updates/universe Translation-en [293 kB]
	Get:9 http://us-west-2.ec2.archive.ubuntu.com/ubuntu bionic-updates/multiverse amd64 Packages [6640 B]
	Get:10 http://security.ubuntu.com/ubuntu bionic-security/multiverse amd64 Packages [4008 B]
	Fetched 2458 kB in 1s (2594 kB/s)                         
	Reading package lists... Done

	ubuntu@ip-10-0-5-66:~$ sudo apt-get upgrade
	Reading package lists... Done
	Building dependency tree       
	Reading state information... Done
	Calculating upgrade... Done
	The following packages will be upgraded:
	  bash dmeventd dmsetup friendly-recovery libdevmapper-event1.02.1 libdevmapper1.02.1
	  libdrm-common libdrm2 liblvm2app2.2 liblvm2cmd2.02 libnss-systemd libpam-systemd libsystemd0
	  libudev1 lvm2 python3-distupgrade systemd systemd-sysv ubuntu-release-upgrader-core udev
	20 upgraded, 0 newly installed, 0 to remove and 0 not upgraded.
	Need to get 7464 kB of archives.
	After this operation, 1024 B of additional disk space will be used.
	Do you want to continue? [Y/n] y
	Get:1 http://us-west-2.ec2.archive.ubuntu.com/ubuntu bionic-updates/main amd64 bash amd64 4.4.18-2ubuntu1.2 [614 kB]
	Get:2 http://us-west-2.ec2.archive.ubuntu.com/ubuntu bionic-updates/main amd64 libnss-systemd amd64 237-3ubuntu10.24 [105 kB]
	Get:3 http://us-west-2.ec2.archive.ubuntu.com/ubuntu bionic-updates/main amd64 libsystemd0 amd64 237-3ubuntu10.24 [204 kB]
	Get:4 http://us-west-2.ec2.archive.ubuntu.com/ubuntu bionic-updates/main amd64 libpam-systemd amd64 237-3ubuntu10.24 [108 kB]
	Get:5 http://us-west-2.ec2.archive.ubuntu.com/ubuntu bionic-updates/main amd64 systemd amd64 237-3ubuntu10.24 [2903 kB]
	Get:6 http://us-west-2.ec2.archive.ubuntu.com/ubuntu bionic-updates/main amd64 udev amd64 237-3ubuntu10.24 [1101 kB]
	Get:7 http://us-west-2.ec2.archive.ubuntu.com/ubuntu bionic-updates/main amd64 libudev1 amd64 237-3ubuntu10.24 [53.6 kB]
	Get:8 http://us-west-2.ec2.archive.ubuntu.com/ubuntu bionic-updates/main amd64 systemd-sysv amd64 237-3ubuntu10.24 [11.4 kB]
	Get:9 http://us-west-2.ec2.archive.ubuntu.com/ubuntu bionic-updates/main amd64 libdevmapper1.02.1 amd64 2:1.02.145-4.1ubuntu3.18.04.1 [127 kB]
	Get:10 http://us-west-2.ec2.archive.ubuntu.com/ubuntu bionic-updates/main amd64 dmsetup amd64 2:1.02.145-4.1ubuntu3.18.04.1 [74.4 kB]
	Get:11 http://us-west-2.ec2.archive.ubuntu.com/ubuntu bionic-updates/main amd64 friendly-recovery all 0.2.38ubuntu1.1 [8888 B]
	Get:12 http://us-west-2.ec2.archive.ubuntu.com/ubuntu bionic-updates/main amd64 libdrm-common all 2.4.97-1ubuntu1~18.04.1 [5216 B]
	Get:13 http://us-west-2.ec2.archive.ubuntu.com/ubuntu bionic-updates/main amd64 libdrm2 amd64 2.4.97-1ubuntu1~18.04.1 [31.3 kB]
	Get:14 http://us-west-2.ec2.archive.ubuntu.com/ubuntu bionic-updates/main amd64 ubuntu-release-upgrader-core all 1:18.04.34 [25.2 kB]
	Get:15 http://us-west-2.ec2.archive.ubuntu.com/ubuntu bionic-updates/main amd64 python3-distupgrade all 1:18.04.34 [107 kB]
	Get:16 http://us-west-2.ec2.archive.ubuntu.com/ubuntu bionic-updates/main amd64 libdevmapper-event1.02.1 amd64 2:1.02.145-4.1ubuntu3.18.04.1 [10.9 kB]
	Get:17 http://us-west-2.ec2.archive.ubuntu.com/ubuntu bionic-updates/main amd64 liblvm2cmd2.02 amd64 2.02.176-4.1ubuntu3.18.04.1 [585 kB]
	Get:18 http://us-west-2.ec2.archive.ubuntu.com/ubuntu bionic-updates/main amd64 dmeventd amd64 2:1.02.145-4.1ubuntu3.18.04.1 [30.4 kB]
	Get:19 http://us-west-2.ec2.archive.ubuntu.com/ubuntu bionic-updates/main amd64 liblvm2app2.2 amd64 2.02.176-4.1ubuntu3.18.04.1 [432 kB]
	Get:20 http://us-west-2.ec2.archive.ubuntu.com/ubuntu bionic-updates/main amd64 lvm2 amd64 2.02.176-4.1ubuntu3.18.04.1 [928 kB]
	Fetched 7464 kB in 0s (49.8 MB/s)
	(Reading database ... 56621 files and directories currently installed.)
	Preparing to unpack .../bash_4.4.18-2ubuntu1.2_amd64.deb ...
	Unpacking bash (4.4.18-2ubuntu1.2) over (4.4.18-2ubuntu1.1) ...
	Setting up bash (4.4.18-2ubuntu1.2) ...
	update-alternatives: using /usr/share/man/man7/bash-builtins.7.gz to provide /usr/share/man/man7/builtins.7.gz (builtins.7.gz) in auto mode
	(Reading database ... 56621 files and directories currently installed.)
	Preparing to unpack .../libnss-systemd_237-3ubuntu10.24_amd64.deb ...
	Unpacking libnss-systemd:amd64 (237-3ubuntu10.24) over (237-3ubuntu10.23) ...
	Preparing to unpack .../libsystemd0_237-3ubuntu10.24_amd64.deb ...
	Unpacking libsystemd0:amd64 (237-3ubuntu10.24) over (237-3ubuntu10.23) ...
	Setting up libsystemd0:amd64 (237-3ubuntu10.24) ...
	(Reading database ... 56621 files and directories currently installed.)
	Preparing to unpack .../libpam-systemd_237-3ubuntu10.24_amd64.deb ...
	Unpacking libpam-systemd:amd64 (237-3ubuntu10.24) over (237-3ubuntu10.23) ...
	Preparing to unpack .../systemd_237-3ubuntu10.24_amd64.deb ...
	Unpacking systemd (237-3ubuntu10.24) over (237-3ubuntu10.23) ...
	Preparing to unpack .../udev_237-3ubuntu10.24_amd64.deb ...
	Unpacking udev (237-3ubuntu10.24) over (237-3ubuntu10.23) ...
	Preparing to unpack .../libudev1_237-3ubuntu10.24_amd64.deb ...
	Unpacking libudev1:amd64 (237-3ubuntu10.24) over (237-3ubuntu10.23) ...
	Setting up libudev1:amd64 (237-3ubuntu10.24) ...
	Setting up systemd (237-3ubuntu10.24) ...
	(Reading database ... 56621 files and directories currently installed.)
	Preparing to unpack .../00-systemd-sysv_237-3ubuntu10.24_amd64.deb ...
	Unpacking systemd-sysv (237-3ubuntu10.24) over (237-3ubuntu10.23) ...
	Preparing to unpack .../01-libdevmapper1.02.1_2%3a1.02.145-4.1ubuntu3.18.04.1_amd64.deb ...
	Unpacking libdevmapper1.02.1:amd64 (2:1.02.145-4.1ubuntu3.18.04.1) over (2:1.02.145-4.1ubuntu3) ...
	Preparing to unpack .../02-dmsetup_2%3a1.02.145-4.1ubuntu3.18.04.1_amd64.deb ...
	Unpacking dmsetup (2:1.02.145-4.1ubuntu3.18.04.1) over (2:1.02.145-4.1ubuntu3) ...
	Preparing to unpack .../03-friendly-recovery_0.2.38ubuntu1.1_all.deb ...
	Unpacking friendly-recovery (0.2.38ubuntu1.1) over (0.2.38ubuntu1) ...
	Preparing to unpack .../04-libdrm-common_2.4.97-1ubuntu1~18.04.1_all.deb ...
	Unpacking libdrm-common (2.4.97-1ubuntu1~18.04.1) over (2.4.95-1~18.04.1) ...
	Preparing to unpack .../05-libdrm2_2.4.97-1ubuntu1~18.04.1_amd64.deb ...
	Unpacking libdrm2:amd64 (2.4.97-1ubuntu1~18.04.1) over (2.4.95-1~18.04.1) ...
	Preparing to unpack .../06-ubuntu-release-upgrader-core_1%3a18.04.34_all.deb ...
	Unpacking ubuntu-release-upgrader-core (1:18.04.34) over (1:18.04.33) ...
	Preparing to unpack .../07-python3-distupgrade_1%3a18.04.34_all.deb ...
	Unpacking python3-distupgrade (1:18.04.34) over (1:18.04.33) ...
	Preparing to unpack .../08-libdevmapper-event1.02.1_2%3a1.02.145-4.1ubuntu3.18.04.1_amd64.deb ...
	Unpacking libdevmapper-event1.02.1:amd64 (2:1.02.145-4.1ubuntu3.18.04.1) over (2:1.02.145-4.1ubuntu3) ...
	Preparing to unpack .../09-liblvm2cmd2.02_2.02.176-4.1ubuntu3.18.04.1_amd64.deb ...
	Unpacking liblvm2cmd2.02:amd64 (2.02.176-4.1ubuntu3.18.04.1) over (2.02.176-4.1ubuntu3) ...
	Preparing to unpack .../10-dmeventd_2%3a1.02.145-4.1ubuntu3.18.04.1_amd64.deb ...
	Unpacking dmeventd (2:1.02.145-4.1ubuntu3.18.04.1) over (2:1.02.145-4.1ubuntu3) ...
	Preparing to unpack .../11-liblvm2app2.2_2.02.176-4.1ubuntu3.18.04.1_amd64.deb ...
	Unpacking liblvm2app2.2:amd64 (2.02.176-4.1ubuntu3.18.04.1) over (2.02.176-4.1ubuntu3) ...
	Preparing to unpack .../12-lvm2_2.02.176-4.1ubuntu3.18.04.1_amd64.deb ...
	Unpacking lvm2 (2.02.176-4.1ubuntu3.18.04.1) over (2.02.176-4.1ubuntu3) ...
	Setting up libnss-systemd:amd64 (237-3ubuntu10.24) ...
	Processing triggers for ureadahead (0.100.0-21) ...
	Processing triggers for install-info (6.5.0.dfsg.1-2) ...
	Setting up systemd-sysv (237-3ubuntu10.24) ...
	Setting up libdevmapper1.02.1:amd64 (2:1.02.145-4.1ubuntu3.18.04.1) ...
	Setting up libdrm-common (2.4.97-1ubuntu1~18.04.1) ...
	Setting up libdevmapper-event1.02.1:amd64 (2:1.02.145-4.1ubuntu3.18.04.1) ...
	Processing triggers for libc-bin (2.27-3ubuntu1) ...
	Setting up udev (237-3ubuntu10.24) ...
	update-initramfs: deferring update (trigger activated)
	Processing triggers for systemd (237-3ubuntu10.24) ...
	Setting up dmsetup (2:1.02.145-4.1ubuntu3.18.04.1) ...
	update-initramfs: deferring update (trigger activated)
	Setting up liblvm2app2.2:amd64 (2.02.176-4.1ubuntu3.18.04.1) ...
	Processing triggers for man-db (2.8.3-2ubuntu0.1) ...
	Setting up friendly-recovery (0.2.38ubuntu1.1) ...
	Sourcing file `/etc/default/grub'
	Sourcing file `/etc/default/grub.d/50-cloudimg-settings.cfg'
	Generating grub configuration file ...
	Found linux image: /boot/vmlinuz-4.15.0-1043-aws
	Found initrd image: /boot/initrd.img-4.15.0-1043-aws
	done
	Processing triggers for dbus (1.12.2-1ubuntu1.1) ...
	Setting up python3-distupgrade (1:18.04.34) ...
	Setting up libpam-systemd:amd64 (237-3ubuntu10.24) ...
	Setting up ubuntu-release-upgrader-core (1:18.04.34) ...
	Setting up libdrm2:amd64 (2.4.97-1ubuntu1~18.04.1) ...
	Setting up liblvm2cmd2.02:amd64 (2.02.176-4.1ubuntu3.18.04.1) ...
	Setting up dmeventd (2:1.02.145-4.1ubuntu3.18.04.1) ...
	dm-event.service is a disabled or a static unit not running, not starting it.
	Setting up lvm2 (2.02.176-4.1ubuntu3.18.04.1) ...
	update-initramfs: deferring update (trigger activated)
	Processing triggers for initramfs-tools (0.130ubuntu3.8) ...
	update-initramfs: Generating /boot/initrd.img-4.15.0-1043-aws
	Processing triggers for libc-bin (2.27-3ubuntu1) ...

