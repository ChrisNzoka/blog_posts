## Linux File Permissions

File permission is an important concept in computer security. Computer users would only want to give access to certain files and directories to those who need it. This is quite useful, especially on computers with several users like home computers, workplace computers, school library computers, et cetera.

## What You Will Learn
In this guide, you'll learn;

- Linux file permissions 
- How to change permissions, owner and group of a file/folder
- What the commands `chmod`, `sudo`, `su`, `chown`, `chgrp` do
- How to represent each of the three sets of permissions (owner, group, and other) as a single digit
- How to add a user
- How to create a group


## Types of File Permission in Linux

Files and directories on a Linux system are assigned access permissions for the owner of each file, the members of a group of related users, and everybody else. A user can assign permissions to read, write, and execute a file. (i.e., run the file as a program).


- **Read**, allows someone to read the contents of a file or folder.
 
- **Write**, allows someone to write information to a file or folder. 

- **Execute**, allows someone to execute a program. 

## Checking Permissions

For the purpose of this tutorial, create a directory with two files in it using the `mkdir` and `touch` command.

Before you change the permission of a file or folder, first, check the current permissions of the file or folder.

**First**, open the terminal with `ctrl + alt + T`

You should have a shell that looks like this:

![Shell_display.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1647011395744/bW8AvIBvQ.png)

**Heads Up**: The ~$ indicates that the terminal is in the home directory. In case you have a different display, use the `cd`, `cd ~` or `cd ~/` command to change to the home directory.

### Creating Folders

Further, create the folder, `My_cool_folder` with the `mkdir` command:

```
mkdir My_cool_folder
``` 
The `ls` command lists the content of the current working directory. Using the `ls` command, check for My_cool_folder directory.

![Shell_display-2.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1647011407835/WtbTxs4qp.png)
The folders were successfully created!!!

### Creating Files

Now, you can create files within the folder using the `touch` command:
```
touch My_cool_folder/butter My_cool_folder/coffee
```
On entering the command above, the files `butter` and `coffee` are created in `My_cool_folder`.

### Checking File Permissions

Now, take a look at the permissions of the file `butter` in `My_cool_folder`. Then change into `My_cool_folder` directory with the command:

```
cd My_cool_folder
```
Next, to display the ownership and permissions for a file, use `ls` with the -l flag and the name of the file you're interested:

```
ls -l butter
```

![Shell_display-3.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1647011428529/1vtnrvqvA.png)
From the output on the terminal you can see that;

- The file `butter` is owned by user `vagrant`
- The user has the right to read, write, but cannot execute this file
- The file is owned by the group `vagrant`
- Members of the group `vagrant` can also read and write this file
- Everybody else can only read this file.


![file_permissios-2.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1646881681167/V0zN4dlrU.png)

The first thing seen in this column is -rw-rw-r--. There are 10 bits here. The first one is the file type. In this example, dash`-` signifies a file. However, if there is `d` in place of first dash `-`, then it is a directory. 

Further, the next nine bits are the actual permissions. They're grouped in trios or sets of three. The first trio refers to the permission of the owner of the file. The second trio refers to the permission of the group that this file belongs to. The last trio refers to the permission of all other users. 

`r` stands for readable, `w` stands for writeable and `x` stands for executable. 

Like in binary, if a bit is set, it is enabled else it is disabled. For file permissions, if a bit is a dash `-`, it is disabled. If it has something other than a dash, it is enabled. 

![Add a subheading.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1649175236018/dAhdeiO-x.png)

## Changing File Permissions

The `chmod` command is used to modify or change file permissions in Linux. There are two formats used to change file permissions in Linux;

- The Symbolic format and,
- Numeric format.

### Symbolic Format for Changing File Permissions

The symbolic format uses symbols (`+` and `-`) and characters to modify the permissions assigned to a file. 

| Symbol | Meaning |
| --------- | ----------- |
| `u` | denotes the owner | 
| `g` | stands for the group the file belongs to |
| `o` | stands for other users of the computer |


For example, the file `butter` above has the permissions, -rw-rw-r--. Give the owner(user) permission to execute the file. To this, use the `chmod` command.

```
chmod u+x butter
```
You can check the permissions with `ls -l` command. You'll see that the execution permission has been added.

```
ls -l butter
```
![Shell_display-4.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1647000806555/NKPCjWNjM.png)

Similarly, you can re-assign or remove a permission by using the minus `-` symbol. Remove the write `w` permission from the group owners of `butter`:
```
chmod g-w butter
```
Check the permission using `ls -l butter`. You will see that the group does not have the permission to write anymore.

![Shell_display-5.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1647000824914/TUC-6LW2H.png)


### Numeric Format for Changing File Permissions

File permissions can be changed numerically. This method is also known as the [octal notation method](https://linuxcommand.org). It is much faster and simpler. It allows you to modify all permissions at once.

The file permissions contain 10 bits of data out of which 9 can be modified. You can assign binary digits to them and then deduce their decimal equivalents.

| Symbols | Binary Notation | Decimal Notation | Meaning |
| ----------- | ----------- | ------------ | ---------------------------------------------------------------- |
| - --- --- --- | 000 000 000 | 000 | No permission assigned |
| - rwx --- ---	| 111 000 000 | 700 | read, write, & execute assigned to the owner |
| - rwx rwx --- | 111 111 000 | 770 | read, write, & execute assigned to the owner and group |
| - rwx rwx rwx | 111 111 111 | 777	| read, write, & execute assigned to the owner, group and other users |
| - --x --x --x | 001 001 001 | 111 | Execute permission for all |
| - -w- -w- -w- | 010 010 010 | 222 | Write permission for all |
| - -wx -wx -wx | 011 011 011 | 333 | Write & execute for all |
| - r-- r-- r-- | 100 100 100 | 444 | Read for all |
| - r-x r-x r-x | 101 101 101 | 555 | Read & execute for all |
| - rw- rw- rw- | 110 110 110 | 666 | Read & write permissions for all |
| - rwx r-- ---	| 111 100 000 | 740 | Owner can read, write, & execute file; group can only read; other users have no permissions |

To set permissions, these decimal numbers are added for every permission set or trio. Take a look at an example by changing permission the file `coffee` to allow the user read and write the file while group members and other users read only.
```
chmod 644 coffee
```
The first number 6, is the owner's permission. The second number, 4, is the group permissions, and the third number, 4, is the permission for all other users.

![Shell_display-8.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1647017647410/hySXoqNRm.png)

## Changing Folder Permissions

Changing the permissions on a directory follows a similar process to that of a file. Work out an example with the directory `My_cool_folder`.

**First**, move up one directory with `cd ..` command, then view the current permissions of the directory using `ls` with `-ld` flag.

**Heads up:** `ls -ld` allows us to see the permissions of the directory itself and not the content of the directory.
 ```
ls -ld My_cool_folder
```

![Shell_display-9.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1647017727778/ecqArnwIp.png)

The permissions for the directory is `drwxrwxr-x`. It starts with a `d` showing that it is a directory unlike dash`-` for files.

The meaning of the r, w, and x attributes is different for directories.

| Permission Symbols | Meaning |
|              :---:               | :---         |
|               `r`                | Lets a user list the contents of the directory provided the `x` attribute is also set |
|              `w`               | Grants a user access to create, delete or rename files within the directory provided the `x` attribute is also set. |
|              `x`                | Grants a user access to enter the directory using `cd` command |

Let's change the permission of the directory to allow only the owner access to enter (execute) the directory leaving the other permissions the way they are.
```
chmod 764 My_cool_folder
```

![Shell_display-10.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1647017803294/zPSucXcIl.png)

**Head's up:** When using `chmod` on a directory, files within that directory are not affected.

Either way, you can change permissions using the **symbolic** or **numerical** format. Just pick whichever is easier for you. 

If you want to avoid figuring out the number that matches the permission levels, you can use an alternate syntax.

## Adding Multiple Permissions Once

You can also add multiple permissions to a file. Give everyone the permission to execute the file `coffee`. To do this, we use the command below
```
chmod ugo+x coffee
```

![Shell_display-7.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1647002035211/xe3UuAhO1.png)

The alphabet `a` can be used in place of `ugo` to alter a permission for everyone. Let's change the permission so that no user can execute the file `coffee`.
```
chmod a-x coffee
```

![Shell_display-6.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1647003468490/bHxKDpURs.png)


## Changing File Owner and Group

The `chown` or change owner command allows you to change the owner of a file.

For example, the file `coffee` is owned by the user `Vagrant`. Change the owner to `betty` who is also a user of the same machine.
```
sudo chown betty coffee
```
Notice the `sudo` command? It allows you to make changes as an administrator.

![Shell_display-11.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1647158953582/G_wXlqxKj.png)

To change the group a file belongs to, you can use the `chgrp` (change group) command. Let's change the group for the file `coffee` to betty's group.
```
sudo chgrp betty group
```

![Shell_display-12.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1647158965996/PdMzIhRS0.png)

Now, the betty group is the group owner for this file.

You can practice changing the permissions on a few files until you get it down. Permissions are an essential building block to computer security.


## Linux: setUID, setGID, stickybit

What if you want users to be able to do something that requires root privileges, but you do not want to give them root privileges?

Normally, if you need to change a file owned by `root`, you would have to use `sudo`. But we want it to be able to have normal users change the files without giving them root access. 

For this to be possible, the `s` permission is assigned to the file. The `s` stands for set user ID (setUID) when assigned to the owner. It allows other users to run the file with the permissions of the owner of the file. 

To enable the setuid bit, you can do it symbolically or numerically. The symbolic format uses an `s` while the numerical format uses a 4, which you prepend to the rest of the permissions like this;
```
sudo chmod u+s butter
``` 
OR
```
sudo chmod 4744 butter
```

![Shell_display-13.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1647160232047/SqVzEb9Ok.png)

Similar to setUID, you can run a file using group permissions with setGID or set group ID. This allows you to run a file as a member of the file group.

To enable the setGID bit, you can use the symbolic or numeric format. The numerical format uses a 2 unlike that of setUID that uses a 4. Let's see an example;
```
sudo chmod g+s coffee
```
OR
```
sudo chmod 2654 coffee
```

![Shell_display-14.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1647160727926/yRigRWhUJ.png)

Last but not the least, ==the sticky bit==. This bit sticks a file or folder down. It makes it so anyone can write to a file or folder, but they cannot delete anything. Only the owner of root can delete anything. 

For example, take a look at the permissions for `/tmp` directory where a lot of programs write temporary files below;

![Shell_display-15.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1647161177469/S3mAbPKQi.png)

Notice the `t` at the end of the permission bits. This means everyone can add and modify files in the `/tmp` directory, but only root or the owner can delete the directory. 

You can also enable the sticky bit using a numerical or symbolic format. The symbolic bit is a `t` and the numeric bit is a `1`.
```
sudo chmod +t My_cool_folder
``` 
OR 
```
sudo chmod 1755 My_cool_folder
``` 
Any of the above commands would work. Verify.

![Shell_display-16.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1647161996892/KjDzb_R1T.png)

## Wrapping Up

Congrats! You have successfully used `chmod` on both directories and normal files, in multiple formats. You can directly set a file's permissions numerically, or add and remove specific permissions one at a time. 

You have also successfully used `chown` and `chgrp` to change the owner and group of a file respectively. Really great work!

You can learn more about Linux command through the book "[The Linux Command Line](https://linuxcommand.org/tlcl.php)" by William_Shotts.

**Heads up:** At this point, I will grant myself permission to stop writing and do something else. There's no command for this at the moment.