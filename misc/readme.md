## Command to find Linux Distro

> cal /etc/os-release

or

> lsb_release -a

## Find Linux Kernel Version

> uname -r

For more detailed

> uname -a

## Find the number of CPU Cores and Sockets

> nproc

for detailed info

> lscpu

## Check RAM size

> free -h

or

> cat /proc/meminfo | grep MemTotal

## Monitor Currently Running Processes and their RAM/CPU Usage

> top

or

> htop

if installed(better interface)

## Sort Running Process by RAM or CPU usage

> ps aux --sort=-%cpu | head

> ps aux --sort=-%mem | head

## Check if your system has a GPU

> lspci | grep -i nvidia
> lspci | grep -i vga

for detailed info

> nvidia-smi

## Find the number of disk and their usage

> lsblk

This lists all the disks

> df -h

This shows disk usage

## Find all Connected USB Devices

> lsusb
