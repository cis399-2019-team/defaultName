# Assignment for Week 4

### 1. URLs

- Henzi:

	ec2-54-190-27-30.us-west-2.compute.amazonaws.com
		
- Austin:

	ec2-34-223-5-208.us-west-2.compute.amazonaws.com


### 2. Log messages showing accesses to your web page in your web server document root

	root@ip-10-0-5-201:~# cd /var/log/apache2/

	root@ip-10-0-5-201:/var/log/apache2# ls -lu
	total 32
	-rw-r----- 1 root adm 12843 Jul 22 18:30 access.log
	-rw-r----- 1 root adm  4220 Jul 20 23:15 access.log.1
	-rw-r----- 1 root adm   681 Jul 22 06:25 error.log
	-rw-r----- 1 root adm   414 Jul 20 23:15 error.log.1
	-rw-r----- 1 root adm     0 Jul 20 23:15 other_vhosts_access.log

	root@ip-10-0-5-201:/var/log/apache2# cat access.log
	10.0.5.224 - - [23/Jul/2019:00:00:49 +0000] "GET /defaultName.html HTTP/1.1" 200 508 "-" "Mo    zilla/5.0 (Macintosh; Intel Mac OS X 10_14_5) AppleWebKit/605.1.15 (KHTML, like Gecko) Version/1    2.1.1 Safari/605.1.15"
	128.223.222.50 - - [23/Jul/2019:00:00:00 +0000] "GET / HTTP/1.1" 200 508 "-" "Mozilla/5.0 (M    acintosh; Intel Mac OS X 10_14_5) AppleWebKit/605.1.15 (KHTML, like Gecko) Version/12.1.1 Safari    /605.1.15"


### 3. Domain name associated with load balancer

- defaultName-1618430243.us-west-2.elb.amazonaws.com


### 4. Describe the results of testing your load balancer when you shut down one, then both, back-end instances, and when you restore them.

- [x] With *both* instances serving
	- The load balancer provides access to our webpage

- [x] With *one* instance shut down
	- The load balancer still provides access to our webpage

- [x] With *both* instances shut down
	- The load balancer fails to provide access to our webpage resulting in a blank page


### 5. Provide excerpts from web server logs from each of your web server instances showing load balancer health checks and accesses to your web content.

- Henzi:

		128.223.222.50 - - [23/Jul/2019:00:04:38 +0000] "GET / HTTP/1.1" 200 508 "-" "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_14_5) AppleWebKit/605.1.15 (KHTML, like Gecko) Version/12.1.1 Safari/605.1.15"
		10.0.5.91 - - [23/Jul/2019:00:04:40 +0000] "GET / HTTP/1.1" 200 518 "-" "ELB-HealthChecker/1.0"
		10.0.5.224 - - [23/Jul/2019:00:04:40 +0000] "GET / HTTP/1.1" 200 518 "-" "ELB-HealthChecker/1.0"
		10.0.5.91 - - [23/Jul/2019:00:05:10 +0000] "GET / HTTP/1.1" 200 518 "-" "ELB-HealthChecker/1.0"
		10.0.5.224 - - [23/Jul/2019:00:05:10 +0000] "GET / HTTP/1.1" 200 518 "-" "ELB-HealthChecker/1.0"
		10.0.5.224 - - [23/Jul/2019:00:05:12 +0000] "-" 408 0 "-" "-"
		10.0.5.91 - - [23/Jul/2019:00:05:22 +0000] "-" 408 0 "-" "-"

- Austin:

		10.0.5.80 - - [22/Jul/2019:20:19:22 +0000] "GET /index.html HTTP/1.1" 200 11229 "-" "ELB-HealthChecker/1.0"
		10.0.5.82 - - [22/Jul/2019:20:19:22 +0000] "GET /index.html HTTP/1.1" 200 11229 "-" "ELB-HealthChecker/1.0"
		10.0.5.80 - - [22/Jul/2019:20:19:45 +0000] "-" 408 0 "-" "-"
		10.0.5.82 - - [22/Jul/2019:20:19:45 +0000] "-" 408 0 "-" "-"
		10.0.5.80 - - [22/Jul/2019:20:19:52 +0000] "GET /index.html HTTP/1.1" 200 11229 "-" "ELB-HealthChecker/1.0"
		10.0.5.82 - - [22/Jul/2019:20:19:52 +0000] "GET /index.html HTTP/1.1" 200 11229 "-" "ELB-HealthChecker/1.0"
		10.0.5.80 - - [22/Jul/2019:20:20:22 +0000] "GET /index.html HTTP/1.1" 200 11229 "-" "ELB-HealthChecker/1.0"
		10.0.5.82 - - [22/Jul/2019:20:20:22 +0000] "GET /index.html HTTP/1.1" 200 11229 "-" "ELB-HealthChecker/1.0"
		10.0.5.80 - - [22/Jul/2019:20:20:36 +0000] "-" 408 0 "-" "-"
		10.0.5.82 - - [22/Jul/2019:20:20:36 +0000] "-" 408 0 "-" "-"


### 6. Puppet code you use to replicate content between your web server instances

Partial puppet code is from `/etc/puppet/code/modules/apache2/manifests/init.pp`

	file { "/var/www/html":
		ensure	=> directory,
		recurse	=> true,
		mode	=> '444',
		owner	=> 'root',
		group	=> 'root',
		source	=> "puppet:///modules/apache2/html",
		require	=> Package["apache2"],
	}

Additional files in subdirectory `/etc/puppet/code/modules/apache2/files` to ensure synchronization to `/var/www/html` as stated in above code.

	root@ip-10-0-5-201:/etc/puppet# cd code/modules/apache2/files/

	root@ip-10-0-5-201:/etc/puppet/code/modules/apache2/files# ls -lu
	total 12
	-rw-r--r-- 1 root root 7224 Jul 22 18:19 apache2.conf
	drwxr-xr-x 2 root root 4096 Jul 23 02:09 html

