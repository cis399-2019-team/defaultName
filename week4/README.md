#Assignment for Week 4

1. URL

		defaultName-1618430243.us-west-2.elb.amazonaws.com/defaultName.html


2. Log messages showing accesses to a web page in your web server document root
  2 
  3     root@ip-10-0-5-201:~# cd /var/log/apache2/
  4 
  5     root@ip-10-0-5-201:/var/log/apache2# ls -lu
  6     total 32
  7     -rw-r----- 1 root adm 12843 Jul 22 18:30 access.log
  8     -rw-r----- 1 root adm  4220 Jul 20 23:15 access.log.1
  9     -rw-r----- 1 root adm   681 Jul 22 06:25 error.log
 10     -rw-r----- 1 root adm   414 Jul 20 23:15 error.log.1
 11     -rw-r----- 1 root adm     0 Jul 20 23:15 other_vhosts_access.log
 12 
 13     root@ip-10-0-5-201:/var/log/apache2# cat access.log
 14     10.0.5.224 - - [23/Jul/2019:00:00:49 +0000] "GET /defaultName.html HTTP/1.1" 200 508 "-" "Mo    zilla/5.0 (Macintosh; Intel Mac OS X 10_14_5) AppleWebKit/605.1.15 (KHTML, like Gecko) Version/1    2.1.1 Safari/605.1.15"
 15     128.223.222.50 - - [23/Jul/2019:00:00:00 +0000] "GET / HTTP/1.1" 200 508 "-" "Mozilla/5.0 (M    acintosh; Intel Mac OS X 10_14_5) AppleWebKit/605.1.15 (KHTML, like Gecko) Version/12.1.1 Safari    /605.1.15"

