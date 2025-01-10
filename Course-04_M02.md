# The Linux Operating System : 

## What will you learn in this module :
1. The architecture of linux
2. Different distributions of linux
3. The shell

## Linux :
- Open-Source OS
- Linux and other programs that come with licensed under the terms of the GNU Public License, which allow you to :
  - use
  - share
  - modify freely

- There are over 600 distributions of linux

- you will use Linux to verify access and authorization in an `identity and access management system`.

## Linux Architecture :

### Components of Linux :
- **User** - person using the system. Linux is multi-user
- **Applications** --  a program that performs a specific task [eg. Nano]
> Nano is a text editor
> Linux applications are commonly distributed through package managers.
> A **package manager** is a tool that helps users install, manage, and remove packages or applications.
> A **package** is a piece of software that can be combined with other packages to form an application.
- **Shell** - it is command line interpreter
- **Filesystem Hierarchy Standard** - organises data. It is a way to organise data so that it can be found when the data is accessed by the system.
- A **directory** is a file that organizes where other files are stored.
- Directories are sometimes called “**folders**,” and they can contain files or other directories. The FHS defines how directories, directory contents, and other storage is organized so the operating system knows where to find specific data. 
- **Kernel** - manages processes and memory.
  - communicates with hardware to execute commands sent by the shell.
  - The kernel uses drivers to enable applications to execute tasks.
  - The Linux kernel helps ensure that the system allocates resources more efficiently and makes the system work faster.
  - The kernel controls all major functions of the hardware, which can help get tasks expedited more efficiently
- **Hardware** - physical components of a computer.[eg. CP, Mouse]
  - Hardware is categorized as either peripheral or internal.
    **1. Peripheral devices**
      - Peripheral devices are hardware components that are attached and controlled by the computer system.
      - They are not core components needed to run the computer system.
      - Peripheral devices can be added or removed freely.
      - Examples of peripheral devices include monitors, printers, the keyboard, and the mouse.
    **2. Internal hardware**
        - Internal hardware are the components required to run the computer.
        - Internal hardware includes a main circuit board and all components attached to it.
        - This main circuit board is also called the **motherboard**.
        - Internal hardware includes the following: 

            1. **The Central Processing Unit (CPU)** is a computer’s main processor, which is used to perform general computing tasks on a computer. The CPU executes the instructions provided by programs, which enables these programs to run. 
            
            2. **Random Access Memory (RAM)** is a hardware component used for short-term memory. It’s where data is stored temporarily as you perform tasks on your computer. For example, if you’re writing a report on your computer, the data needed for this is stored in RAM. After you’ve finished writing the report and closed down that program, this data is deleted from RAM. Information in RAM cannot be accessed once the computer has been turned off. The CPU takes the data from RAM to run programs. 
            
            3. **The hard drive** is a hardware component used for long-term memory. It’s where programs and files are stored for the computer to access later. Information on the hard drive can be accessed even after a computer has been turned off and on again. A computer can have multiple hard drives.

## Linux Distribtions :
- Linux is a very customizable operating system.
- Unlike other operating systems, there are different versions available for you to use.
- These different versions of Linux are called distributions.
- You might also hear them called distros or flavors of Linux.
- It's essential for you to understand the distribution that you're using so you know what tools and apps are available to you.
- For example, Debian is a distro that has different tools than the Ubuntu distribution.
- Different Linux distributions contain different preinstalled programs, user interfaces, and much more.
- Distributions include the Linux kernel, utilities, a package management system, and an installer.

- `Red Hat®` is the parent of CentOS
- `Slackware®` is the parent of SUSE®.
- Both `Ubuntu` and `KALI LINUX™` are derived from Debian.

### KALI LINUX :
- KALI LINUX™ is a trademark of Offensive Security and is Debian derived.
- This open-source distro was made specifically with **penetration testing** and digital forensics in mind.
- There are many tools pre-installed into KALI LINUX™.
- It's important to note that KALI LINUX™ should be used on a virtual machine.
- This prevents damage to your system in the event its tools are used improperly.
- An additional benefit is that using a virtual machine gives you the ability to revert to a previous state.
- KALI LINUX™ has numerous tools that are useful during **penetration testing**.

> **Metasploit** can be used to look for and exploit vulnerabilities on machines.
> **Burp Suite** is another tool that helps to test for weaknesses in web applications.
> **John the Ripper** is a tool used to guess passwords.

- `tcpdump` is a command-line packet analyzer.
- It's used to capture network traffic.
- Another tool commonly used in the security profession is Wireshark.
- It has a graphical user interface that can be used to analyze live and captured network traffic.
- Autopsy is a forensic tool used to analyze hard drives and smartphones.

### Ubuntu :

- Ubuntu is an open-source, user-friendly distribution that is widely used in security and other industries.
- It has both a command-line interface (CLI) and a graphical user interface (GUI).
- Ubuntu is also Debian-derived and includes common applications by default.
- Users can also download many more applications from a package manager, including security-focused tools.
- Because of its wide use, Ubuntu has an especially large number of community resources to support users.
- Ubuntu is also widely used for **cloud computing**.
- As organizations migrate to cloud servers, cybersecurity work may more regularly involve Ubuntu derivatives.

### Parrot :

- Parrot is an open-source distribution that is commonly used for security.
- Similar to KALI LINUX ™, Parrot comes with pre-installed tools related to **penetration testing and digital forensics.**
- Like both KALI LINUX ™ and Ubuntu, it is based on Debian.
- Parrot is also considered to be a user-friendly Linux distribution.
- This is because it has a GUI that many find easy to navigate.
- This is in addition to Parrot’s CLI.

### Red Hat® Enterprise Linux® :

- Red Hat Enterprise Linux is a subscription-based distribution of Linux built for enterprise use.
- Red Hat is not free, which is a major difference from the previously mentioned distributions. -
- Because it’s built and supported for enterprise use, Red Hat also offers a dedicated support team for customers to call about issues.

### AlmaLinux :

- AlmaLinux is a **community-driven** Linux distribution that was created as a stable replacement for CentOS.
- CentOS was an open-source distribution that is closely related to Red Hat, and its final stable release, CentOS 8, was in December 2021.
- CentOS used source code published by Red Hat to provide a similar platform.
- AlmaLinux is designed to be a drop-in replacement for CentOS 8.
- This ensures that applications and configurations that worked on CentOS will continue to function on AlmaLinux. 
