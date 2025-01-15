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

> Note: Relative file paths can use a dot `.` to represent the current directory, or two dots `..` to represent the parent of the current directory.
> 
> An example of a relative file path could be ../projects.

## Find what you Need with Linux :

**1. `grep` :** searches a specified file and returns all lines in the file containing a specified string.
   - [example] : `grep "os" updates.txt` : 1st arguements is the string to be searched, 2nd arguement is the file through which we have to search.


**Piping : `|`**
- Sends the standard output of one command as standard input to another command for further processing.

- When used with grep, the pipe can help you find directories and files containing a specific word in their names.
   - For example, `ls /home/analyst/reports | grep users` returns the file and directory names in the reports directory that contain users.
   - Before the pipe, ls indicates to list the names of the files and directories in reports.
   - Then, it sends this output to the command after the pipe.
   - In this case, grep users returns all of the file or directory names containing users from the input it received.

> **Note:** Piping is a general form of redirection in Linux and can be used for multiple tasks other than filtering.
>
> You can think of piping as a general tool that you can use whenever you want the output of one command to become the input of another command.

**2. `find :`** searches for directories and files that meet specified criteria. 
   - There’s a wide range of criteria that can be specified with find.
   - For example, you can search for files and directories that :
        - Contain a specific string in the name
        - Are a certain file size
        - Were last modified within a certain time frame
   - When using find, the first argument after find indicates where to start searching.
   - For example, entering find /home/analyst/projects searches for everything starting at the projects directory.
   - After this first argument, you need to indicate your criteria for the search.
   - If you don’t include a specific search criteria with your second argument, your search will likely return a lot of directories and files.
   - Specifying criteria involves options. Options modify the behavior of a command and commonly begin with a hyphen (-). 

**a) `-name` and `-iname` :**
   - One key criteria analysts might use with find is to find file or directory names that contain a specific string.
   - The specific string you’re searching for must be entered in quotes after the -name or -iname options.
   - The difference between these two options is that -name is case-sensitive, and -iname is not. 

   - For example, you might want to find all files in the projects directory that contain the word “log” in the file name.
   - To do this, you’d enter find /home/analyst/projects -name `"*log*"`.
   - You could also enter find /home/analyst/projects -iname `"*log*"`.
         
   - In these examples, the output would be all files in the projects directory that contain log surrounded by zero or more characters.
   - The `"*log*"` portion of the command is the search criteria that indicates to search for the string “log”.
   - When `-name` is the option, files with names that include Log or LOG, for example, wouldn’t be returned because this option is case-sensitive.
   - However, they would be returned when `-iname` is the option.
         
> **Note:** An asterisk `*` is used as a wildcard to represent zero or more unknown characters.


**b) `-mtime` :**
   - Security analysts might also use find to find files or directories last modified within a certain time frame. 
   - The `-mtime` option can be used for this search. 
   - For example, entering `find /home/analyst/projects -mtime -3` returns all files and directories in the projects directory that have been modified within the past three days. 

   - The `-mtime` option search is based on days, so entering `-mtime +1` indicates all files or directories last modified more than one day ago, and entering `-mtime -1` indicates all files or directories last modified less than one day ago. 
         
> **Note:** The option `-mmin` can be used instead of `-mtime` if you want to base the search on minutes rather than days.
      
### Create and Modify directories :

#### Commands :

1. `mkdir` : Creates a new directory.
   - you can either provide the new directory as the absolute file path, which starts from the root, or as a relative file path, which starts from your current directory.

2. `rmdir` : Removes, or deletes a directory.
> Note: The rmdir command cannot delete directories with files or subdirectories inside.

3. `touch` : Creates a new file.
4. `rm` : Removes or deletes a file.
5. `mv` : Moves a file or directory to a new location.
6. `cp` : Copies a file/directory to a new location.

### nano text editor :
- nano is a **command-line file editor** that is available by default in many Linux distributions.
- Many beginners find it easy to use, and it’s widely used in the security profession.
- You can perform multiple basic tasks in nano, such as creating new files and modifying file contents. 

- To open an existing file in nano from the directory that contains it, enter nano followed by the file name.
- For example, entering `nano permissions.txt` from the /home/analyst/reports directory opens a new nano editing window with the permissions.txt file open for editing.
- You can also provide the absolute file path to the file if you’re not in the directory that contains it.

- You can also create a new file in nano by entering nano followed by a new file name.
- For example, entering nano `authorized_users.txt` from the `/home/analyst/reports` directory creates the `authorized_users.txt` file within that directory and opens it in a new nano editing window.

- Since there isn't an auto-saving feature in nano, it’s important to save your work before exiting.
- To save a file in nano, use the keyboard shortcut `Ctrl + O`.
- You’ll be prompted to confirm the file name before saving.
- To exit out of nano, use the keyboard shortcut `Ctrl + X`.

> **Note:** Vim and Emacs are also popular command-line text editors.

### Standard output redirection :

- There’s an additional way you can write to files.
- Previously, you learned about standard input and standard output.
- Standard input is information received by the OS via the command line, and standard output is information returned by the OS through the shell.

- You’ve also learned about piping.
- Piping sends the standard output of one command as standard input to another command for further processing.
- It uses the pipe character (|). 

- In addition to the pipe `|`, you can also use the right angle bracket `>` and double right angle bracket `>>` operators to redirect standard output.

- When used with echo, the `>` and `>>` operators can be used to send the output of echo to a specified file rather than the screen.
- The difference between the two is that > overwrites your existing file, and `>>` adds your content to the end of the existing file instead of overwriting it.
- The `>` operator should be used carefully, because it’s not easy to recover overwritten files.

- When you’re inside the directory containing the permissions.txt file, entering `echo "last updated date" >> permissions.txt` adds the string “last updated date” to the file contents. Entering `echo "time" > permissions.txt` after this command overwrites the entire file contents of permissions.txt with the string “time”.

## File permissions and Ownership :
- Permissions are the type of access granted for a file or directory.
- Permissions are related to authorization.
- Authorization is the concept of granting access to specific resources in a system.
- Authorization allows you to limit access to specified files or directories.
- A good rule to follow is that data access is on a need-to-know basis.
- You can imagine the security risk it would impose if anyone could access or modify anything they wanted to on a system.

- There are three types of permissions in Linux that an authorized user can have :
   1. **Read** : On a file, read permissions means contents on the file can be read.
      - On a directory, this permission means you can read all files in that directory.
   2. **Write** : Write permissions on a file allow modifications of contents of the file.
      - On a directory, write permissions indicate that new files can be created in that directory.    3. **Execute** : Execute permissions on files mean that the file can be executed if it's an executable file.
      - Execute permissions on directories allow users to enter into a directory and access its files.
     
- Permissions are granted by 3 different types of Owners :
  1. **User** -- Owner of the file
      - When you create a file, you become the owner of the file.
      - But the ownership can be changed.
  2. **Group** -- Every user is a part of a certain group.
      - A group consists of several users, and this is one way to manage a multi-user environment.
  3. **Other** -- Other can be considered all other users on the system.
 
- In Linux, file permissions are represented with a 10-character string. For a directory with full permissions for the user group, this string would be: drwxrwxrwx.

![image](https://github.com/user-attachments/assets/fbcf335c-2e8c-4435-a24c-e0aa80a0364c)
- Here in the above 10-char string -- `d` denotes that it is a directory.
- if there was a `-` instead, it denotes a regular file.

![image](https://github.com/user-attachments/assets/bba5fd38-e31f-45aa-94ae-cfb8e80b592d)
- the first block of rwx defines the permissions for users. [(r - read),(w - write),(x - execute)]
- if any permission is not granted, then that char contains a `-` instead.

![image](https://github.com/user-attachments/assets/ebc20176-3828-492d-be95-725f8d766e58)
- Second block of rwx defines the permissions for a group
  
![image](https://github.com/user-attachments/assets/1707efc6-cf87-4b76-bfa9-a8b794ece496)
- third block of rwx indicates the permissions for the owner type - Other.

> Ensuring files and directories are set with their appropriate access permissions is critical to protecting sensitive files and maintaining the overall security of a system.

> **World-writable files** can pose significant security risks.
>
> World-writable files are those which contain write permissions for all types of owners.

### Options :
![image](https://github.com/user-attachments/assets/b82db3c4-6e18-486f-ab03-0c9f7960a4e4)

- the options for a command can be a single letter or a full-word.

![image](https://github.com/user-attachments/assets/1f1e52d9-2ae7-45d0-a4c5-b59b9accdff3)![image](https://github.com/user-attachments/assets/9dba1e6e-2e3d-4d28-807c-1b92b2350e9c)![image](https://github.com/user-attachments/assets/ac4c64a7-9d9c-4b4f-a246-01643a389e6a)
![image](https://github.com/user-attachments/assets/a70de782-648f-45ff-9094-0a47c96290cd)

### Changing file permissions:

#### **Using `chmod`** : 
- `chmod` : Changes permissions to files and directories.
   - `chmod` stands for 'change mode'.
- The `chmod` command requires two arguments.
- The first argument indicates how to change permissions
- the second argument indicates the file or directory that you want to change permissions for. 
- For example, the following command would add all permissions to login_sessions.txt:
   - `chmod u+rwx,g+rwx,o+rwx login_sessions.txt`
- If you wanted to take all the permissions away, you could use
   - `chmod u-rwx,g-rwx,o-rwx login_sessions.txt`

- Another way to assign these permissions is to use the equals sign `=` in this first argument.
- Using `=` with chmod sets, or assigns, the permissions exactly as specified.
- For example, the following command would set read permissions for login_sessions.txt for user, group, and other:
   - `chmod u=r,g=r,o=r login_sessions.txt`

- This command overwrites existing permissions.
- For instance, if the user previously had write permissions, these write permissions are removed after you specify only read permissions with `=`. 

   - ![image](https://github.com/user-attachments/assets/a2f3f098-b72c-410f-822c-e371070f1b1d)
   - ![image](https://github.com/user-attachments/assets/ec75cc1e-9c43-4014-a2f7-3764268ff64c)

#### The principle of least privilege in action :
- As a security analyst, you may encounter a situation like this one:
- There’s a file called `bonuses.txt` within a compensation directory.
- The owner of this file is a member of the Human Resources department with a username of hrrep1.
- It has been decided that hrrep1 needs access to this file.
- But, since this file contains confidential information, no one else in the hr group needs access.

- You run `ls -l` to check the permissions of files in the compensation directory and discover that the permissions for `bonuses.txt` are `-rw-rw----`.
- The group owner type has read and write permissions that do not align with the principle of least privilege.  

- To remedy the situation, you input `chmod g-rw bonuses.txt`.
- Now, only the user who needs to access this file to carry out their job responsibilities can access this file.

## Add and Delete Users :

### Root Users (Super user) :
- A root user is the user with elevated privileges to modify the system.
- Individuals who need to perform specific tasks can be temporarily added as root users.
- Root users can create, modify, delete and run any program.
- Only root users or accounts with root privileges can add new users.
  ![image](https://github.com/user-attachments/assets/e60ca3ff-df19-4846-a511-4faff5779c67)


- Problems logging in as a root user :
   - Security risks
   - Irreversible mistakes
   - Accountability
 
### `sudo` :
- Temporarily grants elevated permissions to specific users.
- stands for -- super-user-do

### Commands :

**1. `useradd` :**
- Adds a user to the system.
- ![image](https://github.com/user-attachments/assets/fb442544-bcdb-4932-8d08-df109e8aeda6)

**2. `userdel` :**
- delete a user from the system
- ![image](https://github.com/user-attachments/assets/113b7fdf-7b80-4e38-8dbb-d6636184513a)

### Responsible use of sudo :
- Previously, you explored authorization, authentication, and Linux commands with `sudo`, `useradd`, and `userdel`.
- The `sudo` command is important for security analysts because it allows users to have elevated permissions without risking the system by running commands as the root user.
- You’ll continue exploring authorization, authentication, and Linux commands in this reading and learn two more commands that can be used with sudo: `usermod` and `chown`.

### Responsible use of sudo :
- To manage authorization and authentication, you need to be a root user, or a user with elevated privileges to modify the system.
- The root user can also be called the “super user.”
- You become a root user by logging in as the root user.
- However, running commands as the root user is not recommended in Linux because it can create security risks if malicious actors compromise that account.
- It’s also easy to make irreversible mistakes, and the system can’t track who ran a command.
- For these reasons, rather than logging in as the root user, it’s recommended you use sudo in Linux when you need elevated privileges.

- The `sudo` command temporarily grants elevated permissions to specific users.
- The name of this command comes from `super user do`.
- Users must be given access in a configuration file to use sudo. This file is called the **sudoers file.**
- Although using sudo is preferable to logging in as the root user, it's important to be aware that users with the elevated permissions to use sudo might be more at risk in the event of an attack.

- You can compare this to a hotel with a master key.
- The master key can be used to access any room in the hotel.
- There are some workers at the hotel who need this key to perform their work.
- For example, to clean all the rooms, the janitor would scan their ID badge and then use this master key.
- However, if someone outside the hotel’s network gained access to the janitor’s ID badge and master key, they could access any room in the hotel.
- In this example, the janitor with the master key represents a user using sudo for elevated privileges.
- Because of the dangers of sudo, only users who really need to use it should have these permissions.

- Additionally, even if you need access to sudo, you should be careful about using it with only the commands you need and nothing more.
- Running commands with sudo allows users to bypass the typical security controls that are in place to prevent elevated access to an attacker.

> **Note :** Be aware of sudo if copying commands from an online source. It’s important you don’t use sudo accidentally. 
