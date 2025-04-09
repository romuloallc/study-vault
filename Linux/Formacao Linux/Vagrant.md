Subject: [[Linux]] #linux 

---
Vagrant init
```[bash]
# Create a Vagrant directory with the Rocky Linux 9 box
vagrant init rockylinux/9
```

Uncomment the line, so the VM can use Bridge Adapter
```[bash]
config.vm.network "public_network"
```

Vagrant up
```[bash]
# In Vagrant Directory to start VM 
vagrant up
```