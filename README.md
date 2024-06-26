# Beginner Guide To Command Line Interface :rocket:
The blinking cursor in the terminal window – is it a portal to digital mastery or a gateway to frustration? Don't let the unknown intimidate you! This guide unveils the secrets of the Linux CLI, transforming you from a bewildered beginner to a confident user.
Our Learning Curve :mountain:
1. ### Bread and butter commands :bread:
- #### Most common Commmands
-  man 
-   cd ( Understand flags - dot ., double dot .., tilda~, dash -)
-   mkdir
-   mv
-   cp with recursive flag
-   ls with different flags
-   pwd
-   rm
-   touch
-   cat
-   sudo
-   apt
-   nano
- #### Permission Related Commands :house:
-   chmod - Super important
-   chown - Super important
- #### Files Related Commands  :up:
-   less
-   more
-   tail
-   grep
-   find - Super Important
-   sort
-   wc
2. ### Some More Useful Commands :thumbsup:
-   ps
-   top
-   df
-   uname
-   free
-   lspci
-   kill (with flags)
-   ping
-   ifconfig
-   Pipe operator |
:train: Let's get started!

-   **`man`:** Your personal guru! This command displays the manual page (reference guide) for any other command. Stuck on something?  `man <command name>` will shed light.
-   **`cd` (change directory):** Your trusty map – use this command to navigate between folders in your system.
    -   `cd ..`: Move up one directory level (like going back on a folder path).
    -   `cd ~`: Shortcut to go to your home directory.
    -   `cd -`: Jumps back to the previous directory you were in (handy for quick back-and-forth).
-   **`mkdir` (make directory):** Need to create a new folder? This command is your champion, allowing you to organize your files with ease. For example,  `mkdir new_folder` creates a new folder named "new_folder."
-   **`mv` (move):** This command relocates files and folders to a new location. Use it with caution, as misplaced files can be tricky to recover. `mvmyfile.txt documents/`
This command moves the file named "myfile.txt" to the "documents" directory.
-   **`cp` (copy):** Need a duplicate?  cp -r *source destination.* Copies the entire contents of the "source" directory (including subfolders and files) to the "destination" directory. 
  cp *filename* *destination*. copies the file to the destination file ex: `cp mytext.txt ./Documents`
    
-   **`ls`:** Lists files and folders in the current directory.
    
    -   **`ls -l`:** Shows detailed information about files (permissions, owner, size).
    -   **`ls -h`:** Displays file sizes in a human-readable format (Gigabytes, Megabytes).
    -   **`ls -a`:** Includes all the hidden files in the current directory.
-   **`pwd`:** Prints the full path of your current working directory.
    
-   **`rm filename`:** Permanently deletes the file named "filename". Use with caution!
- **`rm -r`:**  `-r` flag is used to recursively delete a folder. 
    
-   **`touch newfile.txt`:** Creates a new empty file named "newfile.txt".
    
-   **`cat filename`:** Displays the contents of the file named "filename" on your screen.
    
-   **`sudo apt update`:** Updates the list of available software packages (requires administrator privileges).
    
-   **`nano filename.txt`:** Opens the file named "filename.txt" in the nano text editor for modification.

Let's get to a bit more advanced commands: The Permission related commands
-  **`chmod (Change Mode)`:**

_This super important command controls file permissions in Linux._ It determines who (user, group, or others) can access a file and how they can interact with it (read, write, execute).

_Example:_* Let's say you have a file named "secret_document.txt" that you only want yourself (the owner) to be able to read and write. You can use `chmod` to achieve this:

```
chmod 600 secret_document.txt

```

Here's how the permission code breaks down:

-   First digit: Permissions for the owner **(user)** - In this case, 6 (read & write)
-   Second digit: Permissions for the **(group)** - In this case, 0 (no access)
-   Third digit: Permissions for **(others)** - In this case, 0 (no access)
![enter image description here](https://cdn.thegeekdiary.com/wp-content/uploads/2017/11/Files-permissions-and-ownership-basics-in-Linux.png)
-    **-D :** It's a Directory.
-    **- :** It's a file.
-    **User:** The owner of the file.
-   **Group:** A group of users associated with the file.
-   **Others:** All users on the system who are not the owner or in the group.

Each category can have three permission levels:

-   **Read "r":** Allows viewing the file's contents.
-   **Write "w":** Allows modifying the file's content.
-   **Execute "x":** Allows executing the file (if it's a program).
- To add or remove any of the above permission from the user (u), group (g),other (o) or all (a) +,-or = command can be used: Ex `chmod u-x` command revokes the execute permission from the user.
**Files Related Commands** 
**1. less**

-   **Purpose:** View text files one screen at a time, ideal for long files.
-   **Example:**
    
 
    ```
    less /etc/passwd  # View the contents of the /etc/passwd file
    
    ```
    
    **2. more**

-   **Purpose:** Similar to `less`, but with fewer features. Useful for quickly scrolling through files.
-   **Example:**
    
  
    
    ```
    more /etc/issue  # View the system's welcome message
    
    ```
    **3. tail**

-   **Purpose:** View the last few lines of a file, helpful for monitoring logs or output.
-   **Example:**
    

    
    ```
    tail /var/log/syslog  # View the last 10 lines of the system log
    tail -f /var/log/syslog  # Follow the system log in real-time (use Ctrl+C to stop)
    
    ```
    **Some Useful Commands :**
    **1. ps**

-   **Purpose:** Display information about running processes.
-   **Example:**
    

    
    ```
    ps aux  # Show all processes (user, PID, %CPU, %MEM, command)
    ps -ef  # Show all processes in a detailed format
    
    ```
    

**2. top**

-   **Purpose:** Provide a dynamic real-time view of running processes.
-   **Example:**
    
    
    
    ```
    top  # Start the top process monitor
    
    ```
    
    **3. df**

-   **Purpose:** Display information about disk usage.
-   **Example:**
    

    
    ```
    df /home  # Show disk usage for the /home partition
    df -h  # Show disk usage in human-readable format (e.g., GB, MB)
    
    ```

    **4. uname**

-   **Purpose:** Print information about the system's kernel and operating system.
-   **Example:**
    

    
    ```
    uname -a  # Display all available information (kernel version, hostname, etc.)
    
    ```
    
    
    **5. lspci**

-   **Purpose:** List Peripheral Component Interconnect (PCI) devices.
-   **Example:**
    

    
    ```
    lspci -v  # Display detailed information about PCI devices
    
    ```
    
   
    **6. ping**

-   **Purpose:** Test network connectivity by sending ICMP (ping) packets to a host.
-   **Example:**
    

    
    ```
    ping google.com  # Send ping packets to google.com
    
    ```
    
   **7. ifconfig**

-   **Purpose:** Display information about network interfaces (e.g., IP addresses).
-   **Example:**
    

    
    ```
    ifconfig  # Show details of all network interfaces
    
    ```
    
8. **Pipe Operator (|)**

-   **Purpose:** Combine the output of one command as input for another.
-   **Example:**

    
    ```
    ps aux | grep ssh  # Filter processes related to SSH using grep
    df / | sort -n  # Sort disk usage information numerically by used space
    
    ```
There you have it! You're no longer a complete CLI novice. Now you can impress your friends (or at least pretend to) with your newfound command-line prowess. Remember, the power is literally at your fingertips (or should we say keystrokes?). Keep practicing, and you'll be a CLI master in no time!

