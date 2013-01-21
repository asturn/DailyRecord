系统文件基本结构
==============
```
/bin     basic programs (Programs that are absolutly needed, shell and commands only)
```

```
/boot    initialization files (Required to actually boot your computer)
```

```
/dev     device files (Describe physical stuff like hard disks and partitions)
```

```
/etc     configuration files
```

```
/home    users' home directories
```

```
/lib     basic libraries (Required by the basic programs)
```

```
/media   mount points for removable media
```

```
/mnt     mount points (For system admins who need to temporarily mount a filesystem)
```

```
/opt     third-party programs
```

```
/proc    proc filesystem (Describe processes and status info, not stored on disk)
```

```
/root    system administrator's files
```

```
/sbin    basic administration programs (Like bin, but only usable by administators)
```

```
/srv     service-specific files
```

```
/sys     sys filesystem (Similar to proc, stored in memory based filesytem: tempfs)
```

```
/tmp     temporary files (Files not kept between boots, often in tempfs)
```

```
/usr     most programs (Another bin, etc, lib, sbin, but for less important files)
```

```
/var     varible data (Similar to tmp, but preserved between reboots
```

命令的学习
=========

一个神奇的命令：无论你在哪里，敲入 *不带参数*  的 `cd`,立马回到 `home` 目录

`rmdir` 删除目录 `rm` 删除文件

