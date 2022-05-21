## Operating Systems: The Key Knowledge of the Power User

Operating system (OS) is the intermediator between a machine and the user. It is the part of a system  a user interacts with while working on a machine - computer.

In this write up, you're going to understand;
- what an operating system is,
- the components of an operating system,
- their functions, and
- the process of booting up an operating system.

Consider a car driven along the road. The driver, the car user, does not have direct contact with the mechanical setup of the vehicle - wheels, brake pads, engine. Instead, he manoeuvres the car through the interface designed by the manufacturer or the automobile mechanic - steering, gear lever, brake pedal, et cetera.

To drive a car, a driver simply gets in, inserts the key in the ignition, starts the car, shifts the gear and so on. He does not have to go under the hood fiddling with the plugs, crank shaft and brake pads to use the car.

Similarly, to use a computer, the user interacts with the operating system's user space.

![werty.jpg](https://cdn.hashnode.com/res/hashnode/image/upload/v1644236694930/oK56XHWg4.jpeg)

> An operating system is the whole package that manages our computer's resources and lets us interact with it. (source: [Cindy Quash](https://www.coursera.org/professional-certificates/google-it-support))



# The Major Operating Systems

There are several operating systems out there and they all share common characteristics. Once you're able to understand the basic building blocks of one operating system, you can apply that to any operating system and understand how it works.

In this article, we'll focus on the major operating systems used in IT. They include;
- Windows OS
- Mac OS
- Linux OS
- Chrome OS 

![OS.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1644234919128/6CCWNzXRX.png)

Mobile devices are computers in a smaller or embedded form. They make use of operating systems as well like **Android OS**, **iOS**, and **Windows 10 mobile**. 

The operating systems in major mobile devices are sourced from their desktop counterparts. For example, the android OS runs the Linux kernel under the hood. So, it is likely that you've already worked with Linux without knowing it.

It is worthy to note that there are lots of mobile phone operating systems around the world and their number keeps going up. Mastery of any mobile phone OS doesn't guarantee an easy ride with another.


### Windows OS

The Windows OS was developed by Microsoft and used widely in the business and consumer space.  It was first released on November 20, 1985; 36 years ago. Subsequent versions followed till the latest version- Windows 11. It is a closed-source OS with the source code only available through [Shared Source Initiative](https://en.wikipedia.org/wiki/Shared_Source_Initiative). 

Most PC's come with Windows OS as the default operating system. PC means personal computer.

### Linux OS

Linux is an open source operating system, which means its software is free to share, modify, and distribute. They are based on the Linux kernel and are free to download. They can be installed on a Mac or Windows computer. 

![LINUX OS.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1644335959111/h1d-93BTh.png)

Operating systems like Windows or Macintosh on the other hand, are solely developed by their respective companies. 

There are different kinds of linux operating systems termed distributions. Some common Linux distributions are Ubuntu, Debian, Fedora, openSUSE and Red Hat. (Source: [Chris Nzoka-okoye](https://chrisnzoka.hashnode.dev/how-to-install-linux-on-windows-10))

### Mac OS

Mac OS is short for Macintosh Operating System developed by Apple Inc. It is mainly used in the consumer space. Apple computers come with Mac OS preloaded.

![mac os.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1644335760715/ATiw0Ko00.png)

### Chrome OS

Chrome OS is simply the Google chrome browser. With the increase in the development of web applications today, so much can be done through the web browser. Think of emails, chats, creating and sharing documents, editing photos, graphics designing, software development and even remote connection to another computer.

Google Chrome allows for extensions and application installations. Hence, it is reasonable to have an operating system built entirely around the Chrome browser. 

![chrome os2.jpg](https://cdn.hashnode.com/res/hashnode/image/upload/v1644335354460/9NDgCsHW3.jpeg)
> Chrome OS is a Linux-based operating system designed by Google. It is an operating system in which both applications and user data reside in the cloud. (Source: [Wikipedia](https://en.wikipedia.org/wiki/Chrome_OS))

The first Chrome OS laptop, known as a Chromebook, was released in May 2011. Samsung and Acer also shipped their first release in July 2011.


### Key Features of Chrome OS

![chrome-os-parallels-windows.jpg](https://cdn.hashnode.com/res/hashnode/image/upload/v1644335401785/SvuJdTu2S.jpeg)

1. Chrome OS primarily runs web applications but can also run Windows, Android and Linux applications inside containers. 

2. It uses the chrome browser as its user interface but performs kernel functions like process management, memory and input and output in the background. Hence, you don't have to deal with those.

3. Chrome OS machines come pre-installed with the operating system. When you log into a Chrome OS machine, you're also signing into the Chrome browser. 

4. Chrome OS machines are interchangeable because most data is stored in the cloud and not locally on the machine. 

5. Chrome OS is extremely simple to use and very hard for users to meddle with. Since users don't have administrator rights on their Chrome OS machines, they won't be able to alter the system configuration.

6. It has an automatic update mechanism that includes a fail-safe in case anything goes wrong. Simply put, the user does not need to worry about problems or hacks in the system as it is designed to stay up and running. 

7. Finally, the most outstanding feature of Chrome OS is its strong security. It allows the user to browse the web without worrying about malware. Users can also share machines while keeping their data private. It also ensures that data won't be compromised if the machine is stolen. 
There is no need to worry about harmful software that might be out there because Chrome OS defends against these threats.


# Components of an Operating System

There are two main components of an operating system;
- The kernel and
- The user space.


## Kernel space

The Kernel is the background side of the Operating system. It is the unseen part of the operating system performing enormous tasks behind the scene. 
> The kernel is the main core of an operating system which interacts directly with our hardware and manages our systems resources. As users, we don't interact with the kernel directly.  (source: [Coursera](https://www.coursera.org/professional-certificates/google-it-support))

The kernel undertakes four(4) major primary roles in a device; file management, process management, memory management, and I/O management. Below is an indepth explanation on these kernel functions.

![Kernel space.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1644779296536/UFJd-S1mc.png)

### File management

In a physical office file, data is stored in paper form. These files are not all kept on one cabinet, that would be quite messy. Instead, a file system is used to manage and store these files. They are organized in folders or directories to make them easier to find.   

Just like in an office, we use a system to store our files in computers. A computer file is just data that you can store and a file could be anything - a picture, a song, a text file, etcetera. The kernel simply carries out file storage in file management. 

![file management.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1644779658141/7iaBRpjuH.png)

Data are stored in files. A collection of files is known as Folder or Directory. The collection of different directories is known as File System.

Consider a scenario where you have to store a single file. You can easily keep track of the file. Such an easy task. Now, you have hundreds of different kinds of files to store. It is harder to keep track of these files unlike when you had to deal with just one file. This is where the kernel comes to aid. 

The kernel part of the operating system manage files on the computer using three major components;
- File system
- file data and
- metadata

**File systems** are unique and are used for different purposes. Operating system developers also develop file systems with varying features in terms of data storage, speed of operation and resistance towards file corruption.

**NTFS** is the major file system used in Windows OS. Microsoft is developing another file system called [ReFS](https://en.wikipedia.org/wiki/ReFS), this could be a unique feature for Windows 11. 

For Linux, each linux distribution uses a different file system. The standard file system for Linux is **ext4**. It is compatible with older ext file systems.

The default file system for Mac OS is **HFS+**.
  
Since file systems are unique and behave differently, it is not easy to move files across different file systems. You may have to find out more about your OS and the file system.

**File data.** Data are written on the hard disk in the form of data blocks. When a file is saved on the hard disk, it is broken down into many pieces and written to different parts of the disk. Block storage improves faster handling of data because the data isn't stored on one long piece and it can be accessed quicker. It's also better for utilizing storage space. 

**Metadata** is the information about a file. This may include the file type, the size of the file, when it was created,  the last time it was modified, etcetera. You may be able to see the metadata by hovering over the file in some OS like windows.

Lastly, every file is associated with a file extension. For example, beach_song.mp3. Mp3 is a file extension associated with music files. There are many types of file extensions which are used to categorize files.

>A file extension is the appended part of a filename that tells us what type of file it is in certain operating systems. (Source: [Cindy Quash](https://www.coursera.org/professional-certificates/google-it-support))

A working knowledge of file systems and the differences between them is a great skill to have in your  toolbox. It can be useful when you need to do things like recover data from damaged disks. Or explore ways to boot from two different kinds of operating systems, like Windows and Linux, on the same computer.
 

### Process management

> **A process** is simply a running program. For example, the music player playing a song, a web page running on a web browser. 
> 
> **A program** is an application that we can run or execute, such as Google Chrome or Visual studio code editor.

Several processes of the same program can be running at the same time. For example, several windows of your file manager open at the same time or several windows of a web browser running simultaneously. These are all different processes for the same program.

Computers can multitask, hence they can carry out several tasks at once. The **process scheduler** is tasked with switching the execution of different processes on the CPU as fast as the twinkle of an eye. This gives the illusion that things are happening simultaneously.

To run programs, computer resources such as RAM and CPU are dedicated to them. Computer resources are limited. To run multiple programs, the kernel has to manage the computer resources efficiently, allowing all the programs needed to run at the same time.

Thus, we can see that the OS is responsible for managing all the running processes in a system and allocating computer resources towards ensuring the processes run properly.


### Memory management

For a process to run, it requires processor time and memory space. The process will take up space in the computer memory allowing the computer to read and load them quickly. The kernel optimizes memory usage for applications to have enough memory space to run.

The memory is quite small compared to the hard disk drive. Hence, to utilize more memory than we physically have, the kernel use **virtual memory** to better manage memory usage by processes running on the computer.

>Virtual memory is a combination of hard drive space and RAM that acts like memory that our processes can use. (source: [Cindy Quash](https://www.coursera.org/professional-certificates/google-it-support))

To run a program, chunks of data of the program are taken gradually as the process is executed. These data chunks are called pages and are stored in the virtual memory. If we want to read and execute these pages, they have to be sent to physical memory or RAM. 

If the entire program was small enough, it could easily be stored in the RAM to allow the computer process it quickly. For large applications, it would be wasteful loading all the pages to the memory. THe memory cannot contain all at a time. 

Consider a chef making use of a large cookbook. He does not need to read the whole book to make one recipe. Instead, he reads only the pages of the recipe currently in use. 

For recipes he has used recently, he quickly looks through it and continues his cooking process. For recipes used a long time ago or not used for the first time, he will take time to go through it and commit it to memory before applying the steps listed in the recipe.

If the cookbook happens to be small, perhaps it contains only one recipe with a few steps, the chef can easily read through all the pages any time he needs the recipe.

Similarly, when you go to a menu you don't normally use in an application, you will notice the application slows down a little. This is because the computer had to load the page for that menu from virtual memory into RAM. 
Since you don't use all the features of the application at once, the computer does not load all the parts or pages of the application to save memory space.  

The space allocated to virtual memory in the hard drive is termed **swap space**. The kernel handles the process of taking pages of data and swapping them between RAM and virtual memory. 


### I/O Management

I/O management is short for input and output management. It is how the OS kernel manages and interacts with external devices (peripherals) as well as how these external devices interact with each other.

![input-output-devices.png](https://qph.fs.quoracdn.net/main-qimg-0113e94d20c033c06556259f9bd1f932)

The kernel's ability to manage input and output is practical when saving a file to disk, using an external speaker, projecting the computer screen on another screen or use a microphone when video chatting with a friend

> I/O management is anything that can give us input or that we can use for output of data. (source: [Cindy Quash](https://www.coursera.org/professional-certificates/google-it-support))

I/O devices are those devices that perform input and output functions. These include peripherals like monitors, keyboards, mice, hard disk drives, speakers, et cetera. 

The kernel manages these devices when it loads up drivers that are used to interact with them. This is so that the computer, the user as well as other peripherals can recognize and speak to these different types of hardware. 

The kernel manages the transfer of data in and out of the I/O devices. These devices also need to talk to each other. For example; copying a file from a USB drive to the hard drive. 

The kernel handles all the intercommunication between devices and also figures out the most efficient method to carry out the transfer. It tries its best to ensure that data being transferred does not have errors during the process. 

## You and the "user space"

The user space is the part of the operating system the user interacts with like applications (programs), for example text editors, music players, system settings, user interfaces, etcetera. 

There are two ways that you can interact with the OS; with a shell or a graphical user interface (GUI). Note that some shells use graphical user interfaces, but shell users mostly work with the command line interface using text commands. 

A graphical user interface or GUI, is a visual way for a user to interact with a computer. Here, the mouse or touchpad is used to click and drag, to open folders, select programs et cetera. We can see everything we do with it.


> A shell is a program that interprets text commands from the keyboard and sends them to the operating system to execute.

In the early days of operating systems, it was the only user interface available on Unix-like operating systems such as Linux. Nowadays, we have graphical user interfaces (GUIs) in addition to command line interfaces (CLIs) such as the shell.

 

![Screenshot from 2022-02-16 15-50-07.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1645023065972/hkTkznFLv.png)

Instead of right clicking a mouse to create a new file, a text command is used in the shell to perform the same task. 

```$ touch <filename>
``` 

Despite efforts made to develop amazing user interfaces for different operating systems, the shell is still commonly used to run commands, especially by IT specialists, software developers and power users. Power users are above average computer users. 

In Linux, it's essential to actually know commands, not just a GUI. This is because most of the Linux machines you interact with require some tasks to be completed through commands only. 

The common types of shell can be found in Linux and Windows machines. For Linux, **Bash** or **B**ourne **A**gain **SH**ell is used. There are other shell programs available for Linux systems such as **ksh**, **tcsh** and **zsh**. There is also a shell for Windows called Powershell.

You'll learn more about Linux shell; [bash](https://linuxcommand.org/) and windows [powershell](https://ss64.com/ps/) on the linked pages.


# The Boot Process of Operating Systems

Booting an operating system simply means to start up the operating system. Since the operating system runs the machine, turning on the machine usually starts the booting process of the OS as well.

![power-button.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1644760008815/7AWlppZdY.png)

For most operating systems, their boot up process is usually the same and follows the same pattern. Consider the car analogy in the beginning of this work. Different cars start up in the same way. Insert the key, turn on the ignition, et cetera. 

Operating systems start up from nothing and follow a series of steps to arrive at a fully operational system. It is quite important to know the steps so you can diagnose any issue that may arise during the boot process.

The boot process is as below;

![OS boot process.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1644779241019/nNllqsCnC.png)
 
**First**, the computer is turned on. This ushers in the BIOS/UEFI. 
>The BIOS/UEFI is a low-level software that initializes our computer's hardware to make sure everything is good to go. (Source: [Coursera](https://www.coursera.org))

The BIOS/UEFI runs the Power On Self Test (POST). The POST performs a series of diagnostic tests to ensure the computer is in proper working condition. 

Next, a boot device will be selected with respect to the BIOS/UEFI configuration. The BIOS/UEFI is usually configured to select a boot device in the order: Hard drives --> USB drives --> CD drives. These devices will be checked in this order and the computer will search for what is known as a **bootloader**. 

The bootloader is a program that loads the operating system. 

On finding a bootloader on a device in the listed order, the computer will start to execute this program. This will then start to load a larger and more complex program and eventually load our operating system. 

Next, the kernel gets loaded. The kernel controls access to the resources on the computer. It also loads up drivers and more, so that the computer can interact with peripherals. It also gets the hardware to talk to the software. 

Lastly, essential system processes and user space items are launched. These include processes like user log in, spinning up a desktop environment, et cetera. The user space allows us to interact with our system.

# Conclusion

The operating system is the true system manager. It allows the user to have powerful access to the machine to perform difficult tasks with a bit of ease and solve difficult machine problems.

Deep knowledge of operating systems and how to navigate through them is an essential skill in any IT field. As a personal computer user, the knowledge would help you to troubleshoot errors and solve problems on your own without involving an IT support specialist.

There are lots of online guides and courses that will help you learn more and become a powerful computer user. Consider the [Google IT support professional](https://www.coursera.org/professional-certificates/google-it-support) course on Coursera. It teaches core IT skills required of every professional and personal computer user.

To learn and master the linux command line interface and BASH, follow the guides on [Linuxcommand.org](https://linuxcommand.org/)

