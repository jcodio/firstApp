Sar - system activity reporter
sar - part of the sysstat package
sar - collect, report, or save system activity information 
sadc - system activity data collector
sadc  is a backend for sar 

sa1 - every 10 minutes ( generate sa report - binary file)
sa2 - summarize collected data each day ( generates sar report - text file)

/var/log/sa

Ubuntu 
	/etc/default/sysstat - enable to true

centos/Rockey 
	/etc/sysconfig/sysstat

Cron Jobs 
	/etc/cron.d/sysstat

Fedora 
	/etc/systemd/system/sysstat.service.wants/sysstat-collect.timer
	/etc/systemd/system/sysstat.service.wants/sysstat-summary.timer

sar --help 

sar -V version 
sar (sar -u)  CPU
sar -q LOAD AVERAGE 
sar -r MEMORY
sar -A -s -e
sar -q -f FILE
sar -w CONTEXT SWITCHES
sar -n DEV NETWORK
sar -b I/O
sar -B paging
sar -d disk
sar -H huge pages
sar -v Reports status of inode, file and other kernel tables
sar -W Report swapping statistics
    -P (speccify processor)


sar -u -1 (command to go back one day)
sar -r --human (gives the percentage of memory used in human form)
sar -r --human -s 23:00   -- memory usage starting from a particular time.... 
sar -r --human -s 23:00 -e 23:45  - command gives me a range 

