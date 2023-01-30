# Virtual Box

## centos 7

_Install guest additions_

Intall the kernel development package :
``` bash
yum install kernel-devel
```

Update kernel version and rebooted:
``` bash
yum update kernel kernel-headers
reboot now
```

Install the gcc & bzip2 packages:
``` bash 
yum install gcc
yum install bzip2
```

Add the VirtualBox Guest Additions iso to the machine by clicking Device`\`Insert Guest Additions CD image...

Mount the iso:
``` bash
mkdir /media/iso
mount /dev/sr0 /media/iso
cd /media/iso
./VBoxLinuxAdditions.run
```
