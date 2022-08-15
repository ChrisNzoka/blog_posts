## Linux Commands for Checking How much space Is left on a Disk

In this guide, we will learn Linux commands for checking how much space left on the disk. Apart from checking the amount of free space on the disk, the information on how much space files occupy is helpful in disk management.

Also, we'll explore how to combine these commands with other Linux commands to modify the resulting output. These commands work perfectly in Bash and Zsh.

## 1.0. *df* Command
This command displays the amount of space left on the disk. It gives concise information on disk usage for all the file systems and the partitions mounted on the disk. The letter *df* is an acronym for disk free.

```
$ df
Filesystem  1K-blocks      Used    Available  Use%       Mounted on
udev        3980068           0      3980068    0%             /dev
tmpfs       803640         2176       801464    1%             /run
/dev/sda5   479151816  35869768    418872704    8%                /
tmpfs       4018184      201584      3816600    6%         /dev/shm
tmpfs       5120              4         5116    1%        /run/lock
tmpfs       4018184           0      4018184    0%   /sys/fs/cgroup
/dev/loop0  114304       114304            0  100% /snap/core/12941
```

Also, there are several options available for this command. These options help to modify the command output. Alternatively, an option is also known as a flag or a switch. Let's look at the commonly used options.

### 1.1. Human-Readable Format

We can display file sizes with the df command output in a human-readable format using the *-h* flag. It instructs the command to output sizes to the nearest Kilobytes (K), Megabytes (M), Gigabytes (G), et cetera. To illustrate, let's run the command *df -h*.

```
$ df -h
Filesystem  Size  Used  Avail  Use%       Mounted on
udev        3.8G     0   3.8G    0%             /dev
tmpfs       785M  2.2M   783M    1%             /run
/dev/sda5   457G   35G   400G    8%                /
tmpfs       3.9G  230M   3.7G    6%         /dev/shm
tmpfs       5.0M  4.0K   5.0M    1%        /run/lock
tmpfs       3.9G     0   3.9G    0%   /sys/fs/cgroup
/dev/loop0  112M  112M      0  100% /snap/core/12941
```
### 1.2. Total Free Space
When we run *df*, the command shows free disk spaces per filesystem. Manually calculating the sum of free disk spaces can lead to error and waste time. Hence, the *--total* switch appends the summary of free disk space to the output. For instance, "*df --total*" would yield a result as illustrated below.
```
$ df --total
Filesystem  1K-blocks      Used   Available  Use%       Mounted on
udev          3980068         0     3980068    0%             /dev
tmpfs          803640      2176      801464    1%             /run
/dev/sda5   479151816  35869768   418872704    8%                /
tmpfs         4018184    201584     3816600    6%         /dev/shm
tmpfs            5120         4        5116    1%        /run/lock
tmpfs         4018184         0     4018184    0%   /sys/fs/cgroup
/dev/loop0     114304    114304           0  100% /snap/core/12941
total       492091316  36187836   431494136    9% -
```
### 1.3. More Field Display

By default, *df* displays six fields;

- Filesystem
- Size
- Used
- Avail
- Use%
- Mounted on

However, ⁣*df* can display additional fields of information. The option *--o *tells the command to include all omitted fields in the output. 

```
$ df --o
Filesystem  Type   Inodes  IUsed   IFree  IUse%  1K-blocks    Used    Avail  Use%  File Mounted on
udev    devtmpfs   995017    661  994356   1%    3980068         0   3980068   0%   -   /dev
tmpfs      tmpfs  1004546   1294  1003252  1%     803640      2188    801452   1%   -   /run
/dev/sda5   ext4 30498816 360670 30138146  2%  479151816  35878052 418864420   8%   -   /
tmpfs      tmpfs  1004546    331  1004215  1%    4018184    234508   3783676   6%   -   /dev/shm
tmpfs      tmpfs  1004546      6  1004540  1%       5120         4      5116   1%   -   /run/lock
tmpfs      tmpfs  1004546     19  1004527  1%    4018184         0   4018184   0%   -   /sys/fs/cgroup
```
### 1.4. Combining Options
Having seen how the options work individually, next, we can combine them in a single command line to obtain the desired output. For instance, let's append the total free space to the result in a human-readable format.
```
$ df -h --total
Filesystem Size Used Avail Use% Mounted on
udev       3.8G    0  3.8G   0% /dev
tmpfs      785M 2.2M  783M   1% /run
/dev/sda5  457G  35G  400G   8% /
tmpfs      3.9G 230M  3.7G   6% /dev/shm
tmpfs      5.0M 4.0K  5.0M   1% /run/lock
tmpfs      3.9G    0  3.9G   0% /sys/fs/cgroup
/dev/loop0 112M 112M     0 100% /snap/core/12941
total      497G  36G  413G   9% -
```
## 2. *du* Command

This command estimates disk space occupied by a specified file or directory. However, if there is no specified file or directory, the command's action defaults to the current directory. The letters *du* stands for disk usage. It is one of the Linux commands for disk management.

It is equally important to note that the function of *du* is recursive for folders. Thus, the effect spans all the content down to the longest path in such a folder.

### 2.1. Specifying a File or Folder

The basic syntax for the *du* command is *du [OPTION]... [FILE]...* To demonstrate the use of *du*, we will work with the boot folder in the root directory.

We will require administrative rights to gain access to this folder. Therefore, we will attach *sudo* in the command *du -h*. The *sudo* command will grant us superuser access to restricted files and folders.

```
$ sudo du /boot/
4       /boot/efi
2344    /boot/grub/fonts
2516    /boot/grub/i386-pc
7224    /boot/grub
174724  /boot/
```
### 1.2. Human-Readable Format

Previously, we saw how to get data sizes in human-readable format for *df* with the *-h* flag. In the same way, we can get the output for *du* in comfortable size units using the *-h* option.

```
$ sudo du -h /boot/
4.0K /boot/efi
2.3M /boot/grub/fonts
2.5M /boot/grub/i386-pc
7.1M /boot/grub
171M /boot/
```
### 2.3. All Files

By default, du prints the space occupied by directories only. We can employ the *-a* switch to account for all files within the specified directory.

```
$ sudo du -a /boot/
```
### 2.4. Total Occupied Space

The command *du* displays the size of the specified folder last after those of its content. This value is the size of the folder and the amount of disk space it occupies. However, there are two options to get the total amount of space taken by a specified file or folder. They include *-c* and *-h* flags.

*-s* displays the summary of the space used. We will combine *-s* and *-h* to get the output in a readable unit.

```
$ sudo du -sh /boot/
171M  /boot/
```

*-c* appends the total amount of space used to the default output of *du*. From this output, we will see that the "total" size is the same as the space occupied by the directory. To get an easily readable result, we will need to use *-h*.

```
$ sudo du -ch /boot/
4.0K    /boot/efi
2.3M   /boot/grub/fonts
2.5M   /boot/grub/i386-pc
7.1M   /boot/grub
171M  /boot/
171M  total
```
### 2.5. Modifying Output Through Other Commands

So far, we have seen how to use *du* to determine how much space a file or directory occupies on a disk. Furthermore, we will combine this command with other Linux commands to tailor it to our desired output.

We can combine *du* by piping the output into other commands to obtain a different result. For example, let's sort the resultant output according to size. We will use the sort command with the *-n* flag. By default, the sort command compares only the first digits numerically. *-n* ensures the command compares according to string numerical values.

Alternatively, we can guarantee a general numeric comparison with the *-g* switch.

```
$ sudo du -a /boot/ | sort -g
4      /boot/efi
2344   /boot/grub/fonts
2516   /boot/grub/i386-pc
7224   /boot/grub
174724 /boot/
```

Next, we can check for larger files by piping the outcome through the *tail* command. This command prints the last ten lines of each file to standard output. In addition, it also reads from standard input and the outcome of instructions passed to it.

```
$ sudo du -a /boot/ | sort -g | tail
2344   /boot/grub/fonts
2516   /boot/grub/i386-pc
5824   /boot/System.map-5.13.0-35-generic
5824   /boot/System.map-5.13.0-39-generic
7224   /boot/grub
9936   /boot/vmlinuz-5.13.0-35-generic
9936   /boot/vmlinuz-5.13.0-39-generic
67452  /boot/initrd.img-5.13.0-35-generic
67468  /boot/initrd.img-5.13.0-39-generic
174724 /boot/
```

In the same way, the *head* command can give a similar result. It prints the first ten lines read from standard input to standard output. However, we will append *-r* to the sort command to reverse the comparison. We will obtain a result with a similar result sorted in reverse order.

```
$ sudo du -a /boot/ | sort -gr | head
174724 /boot/
67468  /boot/initrd.img-5.13.0-39-generic
67452  /boot/initrd.img-5.13.0-35-generic
9936   /boot/vmlinuz-5.13.0-39-generic
9936   /boot/vmlinuz-5.13.0-35-generic
7224   /boot/grub
5824   /boot/System.map-5.13.0-39-generic
5824   /boot/System.map-5.13.0-35-generic
2516   /boot/grub/i386-pc
2344   /boot/grub/fonts
```
4. Conclusion

To wrap up, we saw handy Linux commands to check for available space on a disk. Also, we practised how to use them alongside options employed to modify their output. Using the pipe symbol, we were able to work with other Linux commands to obtain desired results.