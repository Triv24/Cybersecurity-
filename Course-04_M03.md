# Linux Commands in the Bash Shell :

## What you'll  learn :
- The command line
- Navigating and Managing the File System
- Authenticating and Authorizing Users
- Accessing Resources

### Security Analysts :
- Work with server logs
- Navigate, Manage, Analyze files remotely
- Verify and COnfigure users and group access
- Give authorization and set file permissions

## Core commands for navigation and reading files :

**1. `pwd`** - prints the working directory onto the screen.
**2. `ls`** - displays list of files and directories in the current working directory.
**3. `cd`** - navigate between directories.
**4. `cat`** - displays the content of the file.
**5. `head`** - displays just the beginning of a file (by default 10 lines).

## Filesystem Hierarchy Standard (FHS)
- Previously, you learned that the Filesystem Hierarchy Standard (FHS) is the component of Linux that organizes data.
- The FHS is important because it defines how directories, directory contents, and other storage is organized in the operating system.

- This diagram illustrates the hierarchy of relationships under the FHS:
 ![image](https://github.com/user-attachments/assets/e26569f3-c63a-46d4-9b75-0d9150b33584)

> A **file path** is the location of a file or directory.
>
> In the file path, the different levels of the hierarchy are separated by a forward slash `/`.

### Root directory :
- The root directory is the highest-level directory in Linux,
- and it’s always represented with a forward slash `/`.
- All subdirectories branch off the root directory.
- Subdirectories can continue branching out to as many levels as necessary.

### Standard FHS directories :
Directly below the root directory, you’ll find standard FHS directories. In the diagram, home, bin, and etc are standard FHS directories. Here are a few examples of what standard directories contain:

**1. `/home`:** Each user in the system gets their own home directory.

**2. `/bin`:** This directory stands for “binary” and contains binary files and other executables.
   - Executables are files that contain a series of commands a computer needs to follow to run programs and perform other functions.

**3. `/etc`:** This directory stores the system’s configuration files.

**4. `/tmp`:** This directory stores many temporary files. 
  - The /tmp directory is commonly used by attackers because anyone in the system can modify data in these files.

**5. `/mnt`:** This directory stands for “mount” and stores media, such as USB drives and hard drives.

> Pro Tip: You can use the `man hier` command to learn more about the FHS and its standard directories.

### User-specific subdirectories :
- Under home are subdirectories for specific users.
- In the diagram, these users are analyst and analyst2.
- Each user has their own personal subdirectories, such as projects, logs, or reports.

> Note: When the path leads to a subdirectory below the user’s home directory, the user’s home directory can be represented as the tilde (~).
> For example, `/home/analyst/logs` can also be represented as `~/logs`.

- You can navigate to specific subdirectories using their absolute or relative file paths.
- The absolute file path is the full file path, which starts from the root.
- For example, `/home/analyst/projects` is an absolute file path.
- The relative file path is the file path that starts from a user's current directory.

> Note: Relative file paths can use a dot (.) to represent the current directory, or two dots (..) to represent the parent of the current directory.
> An example of a relative file path could be ../projects.
