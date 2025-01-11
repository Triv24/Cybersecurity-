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

### Navigation commands :
**1. `pwd`** - prints the working directory onto the screen.
**2. `ls`** - displays list of files and directories in the current working directory.
> **Note:** If you want to return the contents of a directory that’s not your current working directory, you can add an argument after ls with the absolute/relative file path to the desired directory.
>
> For example, if you’re in the `/home/analyst` directory but want to list the contents of its projects subdirectory, you can enter `ls /home/analyst/projects` or just `ls projects`.

**3. `cd`** - navigate between directories.
> **Pro Tip:** You can use the relative file path and enter `cd ..` to go up one level in the file structure.
>
> For example, if the current directory is `/home/analyst/projects`, entering `cd ..` would change your working directory to /home/analyst. 


### Commands for reading file contents :
**1. `cat`** - displays the content of the file.
   - For example, entering `cat updates.txt` returns everything in the updates.txt file.


**2. `head`** - displays just the beginning of a file (by default 10 lines).
   - Entering `head updates.txt` returns only the first 10 lines of the updates.txt file.

> **Pro Tip:** If you want to change the number of lines returned by head, you can specify the number of lines by including `-n`.
>
> For example, if you only want to display the first five lines of the updates.txt file, enter `head -n 5 updates.txt`.

> **Pro Tip:** To learn what your username is, use the `whoami` command.
>
> The `whoami` command returns the username of the current user.
>
> For example, if your username is `analyst`, entering `whoami` returns `analyst`.

**3. `tail`** - The tail command does the opposite of head. 
   - This command can be used to display just the end of a file, by default 10 lines.
   - Entering `tail updates.txt` returns only the last 10 lines of the updates.txt file.
> **Pro Tip:** You can use tail to read the most recent information in a log file.

**4. `less`** - The less command returns the content of a file one page at a time. 
   - For example, entering `less updates.txt` changes the terminal window to display the contents of updates.txt one page at a time.
   - This allows you to easily move forward and backward through the content. 

   - Once you’ve accessed your content with the less command, you can use several keyboard controls to move through the file:
    - `Space bar`: Move forward one page
    - `b`: Move back one page
    - `Down arrow`: Move forward one line
    - `Up arrow`: Move back one line
    - `q`: Quit and return to the previous terminal window

     
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
> 
> For example, `/home/analyst/logs` can also be represented as `~/logs`.

- You can navigate to specific subdirectories using their absolute or relative file paths.
- The absolute file path is the full file path, which starts from the root.
- For example, `/home/analyst/projects` is an absolute file path.
- The relative file path is the file path that starts from a user's current directory.

> Note: Relative file paths can use a dot (.) to represent the current directory, or two dots (..) to represent the parent of the current directory.
> 
> An example of a relative file path could be ../projects.

