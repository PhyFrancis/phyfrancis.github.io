# Design Patterns in Linux kernel

## Consistency model for shared resource
1. Spin lock.
1. Read/Write lock.
1. Read copy write.

## Virtual Filesystem (VFS) design
Separating filesystem interface and filesystem implementation. So all filesystems have the same interface, making it easier to develop apps.

New filesystem can be supported dynamically, by registering its implementation into a virtual-table-like data structure in kernel.

## I/O scheduler for block devices
Reading block devices is slow because the device (e.g. a hdd disk) needs mechanically move its read head. The scheduler reduces the overhead by batching together the read requests that are reading adjacent regions.

## Linux filesystem
Main advantage of ext3 over ext2 is that the former supports
[journaling](https://en.wikipedia.org/wiki/Journaling_file_system), which can
guarantee atomiticity at system call level.
