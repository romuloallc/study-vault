Subject: [[Linux]] #linux 

---
Ver o que está ocupando espaço na pasta
```bash
du -hsx * | sort -rh | head -20
```

Disk-free
```[bash]
df -h  # Show Disk space in human-readable format 
df -a  # Shows the file system's complete disk usage even if the Available field is 0 
df -T  # Show type of the disk
df -i  # shows used and free inodes(?)
```

Disk-usage
```[bash]
du -sch * | sort -h
```
