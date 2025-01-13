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
