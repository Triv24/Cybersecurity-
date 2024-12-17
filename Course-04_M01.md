# Introduction to Operating Systems :

## Operating Systems : 
- It's the interface between the computer hardware and the user.
- The operating system is responsible for making the computer run as efficiently as possible while also making it easy to use.
  
> **Hardware :** refers to the physical components of a computer.

- Computers communicate in a language called binary, which consists of 0s and 1s.
- The OS provides an interface to bridge this communication gap between the user and the computer, allowing you to interact with the computer in complex ways.

### Common operating systems :

- The following operating systems are useful to know in the security industry: Windows, macOS®, Linux, ChromeOS, Android, and iOS.

#### Windows and macOS :

- Windows and `macOS` are both common operating systems.
- The Windows operating system was introduced in 1985, and macOS was introduced in 1984.
- Both operating systems are used in personal and enterprise computers. 

- Windows is a closed-source operating system, which means the source code is not shared freely with the public.
- `macOS` is partially open source.
- It has some open-source components, such as `macOS`’s kernel.
- `macOS` also has some closed-source components.

#### Linux :

- Linux is a completely open-source operating system, which means that anyone can access Linux and its source code.
- The open-source nature of Linux allows developers in the Linux community to collaborate.

- Linux is particularly important to the security industry.
- There are some distributions that are specifically designed for security.
- Later in this course, you’ll learn about Linux and its importance to the security industry.

#### ChromeOS :

- ChromeOS launched in 2011.
- It’s partially open source and is derived from `Chromium OS`, which is completely open source.
- ChromeOS is frequently used in the education field.

#### Android and iOS :

- Android and iOS are both mobile operating systems.
- Unlike the other operating systems mentioned, mobile operating systems are typically used in mobile devices, such as phones, tablets, and watches.
- Android was introduced for public use in 2008, and iOS was introduced in 2007.
- Android is open source, and iOS is partially open source.

### Operating systems and vulnerabilities :

- Security issues are inevitable with all operating systems.
- An important part of protecting an operating system is keeping the system and all of its components up to date.

#### Legacy operating systems :

- A legacy operating system is an operating system that is outdated but still being used.
- Some organizations continue to use legacy operating systems because software they rely on is not compatible with newer operating systems.
- This can be more common in industries that use a lot of equipment that requires embedded software—software that’s placed inside components of the equipment.

- Legacy operating systems can be vulnerable to security issues because they’re no longer supported or updated.
- This means that legacy operating systems might be vulnerable to new threats.

 #### Other vulnerabilities :
 
- Even when operating systems are kept up to date, they can still become vulnerable to attack. Below are several resources that include information on operating systems and their vulnerabilities.

[Microsoft Security Response Center (MSRC)](https://msrc.microsoft.com/update-guide/vulnerability)
- A list of known vulnerabilities affecting Microsoft products and services

[Apple Security Updates](https://support.apple.com/en-us/100100)
- A list of security updates and information for Apple® operating systems, including macOS and iOS, and other products

[Common Vulnerabilities and Exposures (CVE) Report for Ubuntu](https://ubuntu.com/security/cves)
- A list of known vulnerabilities affecting Ubuntu, which is a specific distribution of Linux

[Google Cloud Security Bulletin](https://cloud.google.com/support/bulletins)
- A list of known vulnerabilities affecting Google Cloud products and services

- Keeping an operating system up to date is one key way to help the system stay secure.
- Because it can be difficult to keep all systems updated at all times, it’s important for security analysts to be knowledgeable about legacy operating systems and the risks they can create.

# Inside the Operating Systems :

- Booting the computer means that a special microchip called a BIOS is activated
- On many computers built after 2007, the chip was replaced by the UEFI.
- Both BIOS and UEFI contain booting instructions that are responsible for loading a special program called the bootloader.
- Then, the bootloader is responsible for starting the operating system. Just like that, your computer is on.

- An application is a program that performs a specific task.
- When you do this, the application sends your request to the operating system.
- From there, the operating system interprets this request and directs it to the appropriate component of the computer's hardware.

## Requests to the operating system :

- Operating systems are a critical component of a computer.
- They make connections between applications and hardware to allow users to perform tasks.

### Booting the computer :

- When you boot, or turn on, your computer, either a BIOS or UEFI microchip is activated.
- The `Basic Input/Output System (BIOS)` is a microchip that contains loading instructions for the computer and is prevalent in older systems.
- The `Unified Extensible Firmware Interface (UEFI)` is a microchip that contains loading instructions for the computer and replaces BIOS on more modern systems.

- The BIOS and UEFI chips both perform the same function for booting the computer.
- BIOS was the standard chip until 2007, when UEFI chips increased in use.
- Now, most new computers include a UEFI chip.
- UEFI provides enhanced security features.

- The BIOS or UEFI microchips contain a variety of loading instructions for the computer to follow.
- For example, one of the loading instructions is to verify the health of the computer’s hardware.

- The last instruction from the BIOS or UEFI activates the bootloader.
- The **bootloader** is a software program that boots the operating system.
- Once the operating system has finished booting, your computer is ready for use.

### Completing a task :

- As previously discussed, operating systems help us use computers more efficiently.
- Once a computer has gone through the booting process, completing a task on a computer is a four-part process.

![image](https://github.com/user-attachments/assets/664b93ea-c94a-46a1-b68a-c649bc91cdeb)

**1. User :**

- The first part of the process is the user.
- The user initiates the process by having something they want to accomplish on the computer.
- Right now, you’re a user!  You’ve initiated the process of accessing this reading.

**2. Application :**

- The application is the software program that users interact with to complete a task.
- For example, if you want to calculate something, you would use the calculator application.
- If you want to write a report, you would use a word processing application. This is the second part of the process.


**3. Operating system :**

- The operating system receives the user’s request from the application.
- It’s the operating system’s job to interpret the request and direct its flow.
- In order to complete the task, the operating system sends it on to applicable components of the hardware. 

**4. Hardware :**

- The hardware is where all the processing is done to complete the tasks initiated by the user.
- For example, when a user wants to calculate a number, the CPU figures out the answer.
- As another example, when a user wants to save a file, another component of the hardware, the hard drive, handles this task. 

After the work is done by the hardware, it sends the output back through the operating system to the application so that it can display the results to the user.

### The OS at work behind the scenes :

- Consider once again how a computer is similar to a car.
- There are processes that someone won’t directly observe when operating a car, but they do feel it move forward when they press the gas pedal.
- It’s the same with a computer.
- Important work happens inside a computer that you don’t experience directly.
- This work involves the operating system.

- You can explore this through another analogy.
- The process of using an operating system is also similar to ordering at a restaurant.
- At a restaurant you place an order and get your food, but you don’t see what’s happening in the kitchen when the cooks prepare the food.

- Ordering food is similar to using an application on a computer.
- When you order your food, you make a specific request like “a small soup, very hot.”
- When you use an application, you also make specific requests like “print three double-sided copies of this document.” 

- You can compare the food you receive to what happens when the hardware sends output.
- You receive the food that you ordered.
- You receive the document that you wanted to print. 

- Finally, the kitchen is like the OS.
- You don’t know what happens in the kitchen, but it’s critical in interpreting the request and ensuring you receive what you ordered.
- Similarly, though the work of the OS is not directly transparent to you, it’s critical in completing your tasks.

### An example: Downloading a file from an internet browser :

- Previously, you explored how operating systems, applications, and hardware work together by examining a task involving a calculation.
- You can expand this understanding by exploring how the OS completes another task, downloading a file from an internet browser: 

1. First, the user decides they want to download a file that they found online, so they click on a download button near the file in the internet browser application.

2. Then, the internet browser communicates this action to the OS.

3. The OS sends the request to download the file to the appropriate hardware for processing.

4. The hardware begins downloading the file, and the OS sends this information to the internet browser application.
  - The internet browser then informs the user when the file has been downloaded.

# Virtualization technology :

- You've explored a lot about operating systems.
- One more aspect to consider is that operating systems can run on virtual machines.
- In this reading, you’ll learn about virtual machines and the general concept of virtualization.
- You’ll explore how virtual machines work and the benefits of using them.

## What is a virtual machine? :

- A virtual machine (VM) is a virtual version of a physical computer.
- Virtual machines are one example of virtualization.
- Virtualization is the process of using software to create virtual representations of various physical machines.
- The term “virtual” refers to machines that don’t exist physically, but operate like they do because their software simulates physical hardware.
- Virtual systems don’t use dedicated physical hardware.
- Instead, they use software-defined versions of the physical hardware.
- This means that a single virtual machine has a virtual CPU, virtual storage, and other virtual hardware.
- Virtual systems are just code.

![image](https://github.com/user-attachments/assets/17145eb1-a2e6-4b6b-97e7-d4c15818205e)

- You can run multiple virtual machines using the physical hardware of a single computer. This involves dividing the resources of the host computer to be shared across all physical and virtual components. For example, Random Access Memory (RAM) is a hardware component used for short-term memory. If a computer has 16GB of RAM, it can host three virtual machines so that the physical computer and virtual machines each have 4GB of RAM. Also, each of these virtual machines would have their own operating system and function similarly to a typical computer.

## Benefits of virtual machines :

- Security professionals commonly use virtualization and virtual machines.
- Virtualization can increase security for many tasks and can also increase efficiency.

### Security :

- One benefit is that virtualization can provide an isolated environment, or a sandbox, on the physical host machine.
- When a computer has multiple virtual machines, these virtual machines are “guests” of the computer.
- Specifically, they are isolated from the host computer and other guest virtual machines.
- This provides a layer of security, because virtual machines can be kept separate from the other systems.
- For example, if an individual virtual machine becomes infected with malware, it can be dealt with more securely because it’s isolated from the other machines.
- A security professional could also intentionally place malware on a virtual machine to examine it in a more secure environment.

> Note: Although using virtual machines is useful when investigating potentially infected machines or running malware in a constrained environment, there are still some risks.
> For example, a malicious program can escape virtualization and access the host machine. This is why you should never completely trust virtualized systems.

### Efficiency :

- Using virtual machines can also be an efficient and convenient way to perform security tasks.
- You can open multiple virtual machines at once and switch easily between them.
- This allows you to streamline security tasks, such as testing and exploring various applications.

- You can compare the efficiency of a virtual machine to a city bus.
- A single city bus has a lot of room and is an efficient way to transport many people simultaneously.
- If city buses didn’t exist, then everyone on the bus would have to drive their own cars.
- This uses more gas, cars, and other resources than riding the city bus. 

- Similar to how many people can ride one bus, many virtual machines can be hosted on the same physical machine.
- That way, separate physical machines aren't needed to perform certain tasks.

## Managing virtual machines :

- Virtual machines can be managed with a software called a hypervisor.
- Hypervisors help users manage multiple virtual machines and connect the virtual and physical hardware.
- Hypervisors also help with allocating the shared resources of the physical host machine to one or more virtual machines.

- One hypervisor that is useful for you to be familiar with is the `Kernel-based Virtual Machine (KVM)`.
- KVM is an open-source hypervisor that is supported by most major Linux distributions.
- It is built into the Linux kernel, which means it can be used to create virtual machines on any machine running a Linux operating system without the need for additional software.

### Other forms of virtualization :

- In addition to virtual machines, there are other forms of virtualization. Some of these virtualization technologies do not use operating systems.
- For example, multiple virtual servers can be created from a single physical server.
- Virtual networks can also be created to more efficiently use the hardware of a physical network.

---

# GUI v/s CLI :

