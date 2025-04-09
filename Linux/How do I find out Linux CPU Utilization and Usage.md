Subject: [[Linux]] #linux 

Links:
- [How Do I Find Out Linux CPU Utilization and Usage](https://www.cyberciti.biz/tips/how-do-i-find-out-linux-cpu-utilization.html)

When the CPU is occupied by it's process, it is unavailable for processing other requests
 - New process needs to wait unitl the CPU is free

Identify the CPU utilization, usage and which process is eating the CPU(s)

```[bash]
top
htop
```

There are more tools to investigate the CPU utilization with the package **sysstat**
```[bash]
# Show the utilization of each CPU individually
mpstat
mpstat -P ALL
```

```[bash]
# Show system's average CPU utilization since the last reboot
# Show input/output statistics for devices and partitions
iostat

# Output of the command every 5 seconds
iostat -xtc 5 3