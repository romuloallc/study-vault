Subject: [[Linux]] #linux 

Links:
- [How Do I Find Out Linux Disk Utilization and I/O Usage](https://www.cyberciti.biz/tips/linux-disk-performance-monitoring-howto.html)

Install the sysstat package

```[bash]
iostat
```

```[bash]
iotop
```

How to Interpret the output result?
 - Note the following values
	1. Average service time (svctm)
	2. Percentage of CPU time during which I/O requests were issued (%util)
	3. See if a hard disk reports consistently high reads/writes (r/s and w/s)

- If any of theses are high, you need to take one of the following action:
	- High speed disk and controller for file system (SSD)
	- Tune software or application or kernel or file system for better disk utilization
	- Use RAID array to spread the file system load