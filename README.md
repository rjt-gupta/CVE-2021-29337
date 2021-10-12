# CVE-2021-29337 - Privilege Escalation in MODAPI.sys (MSI Dragon Center) 

## General

- Affected Product: MSI Dragon Center
- Affected Version: 2.0.104.0 
- [CVE MITRE](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2021-29337)

## Description
A vulnerable kernel driver MODAPI.sys in dragon center exposes IOCTL 0x9C406104 which allows low-privileged users to interact directly with physical memory by calling one of several driver routines (MmMapIoSpace) that map physical memory into the virtual address space.

Sending valid input and output buffers via DeviceIoControl allows arbitrary manipulation of the kernel memory in the latest Windows 10 depicting user-mode data being passed to the MmMapIoSpace routine. This vulnerability could possibly allow local privilege escalation to NT AUTHORITY\SYSTEM.

## Inspiration from Legends
- [@DownWithup](https://twitter.com/DownWithUpSec)
- [@h0mbre](https://twitter.com/h0mbre_)
