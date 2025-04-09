Type: [[Linux Up Skill Challenge]] #linux 

```[bash]
# See Linux distro and version
lsb_release -a   
cat /etc/os-release

# System information
uname -a

# System uptime
cat /proc/uptime
uptime # /proc/uptime but readable

# Your username
whoami

# Who is logged in
who

# Who is logged in and what they are doing
w
```

```[bash]
# Hardware Information
lshw # Detailed information

# CPU architecture
lscpu

# Block devices
lsblk

# PCI devices
lspci

# USB devices
lsusb
```

```[bash]
# Memory used
free -h
vmstat

# More interactive
top
htop
```

```[bash]
# Disk Usage
df -h

# Size of your folders
du -h
```

```[bash]
# Network Interfaces
ifconfig   # older
ip addres
ip a

# Network Usage
netstat -i  # Static view
ifstat      # Continuous view

# More info
sudo iftop -i [interface]
```

[[What is swap and swap space?]] 
