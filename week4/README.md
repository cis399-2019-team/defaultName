#Assignment for Week 4

1. URL

		defaultName-1618430243.us-west-2.elb.amazonaws.com/defaultName.html


2. Log messages showing accesses to our web page in our web server document root

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


3. Domain name associated with load balancer

		Henzi:
			ec2-54-190-27-30.us-west-2.compute.amazonaws.com
		
		Austin:
			ec2-34-223-5-208.us-west-2.compute.amazonaws.com

