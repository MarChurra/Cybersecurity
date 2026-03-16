- & - Append it to a command to run the cmd in the background
- CTRL + Z - suspends the process and puts it in the background
- FG - brings a process back to the foreground

- pwd - Show me the current location (Printing Working Directory)
- ls - Shows subfolders of the current directory
- ls -l - Lists the content of the subfolder in further detail
- ls -al - Lists the content of the subfolders wioth detals and hidden files (Hidden files start with a dot and are hidden by default by Linux)
- cd - Change Directory
- cd .. - Go back one level
- find - Locates files with find <start> -name <filename>
- ~ - Home directory
- cat - Reads the file
- whoami - Logged in user
- uname -a - Kernel Version
- df -h - Check Disk usage or available space (h flag is for human readable).
  - /dev/root is the main disk of the system.
  - Linux stores configuration and information files in the /etc directory 
- grep - Searches for contents inside a file
- | - funnels output as an input for another command
- pyhton3 -m http.server - opens a web server
- curl or wget - download application via HTTP
- scp - Secure copy with SSH
- CP - copy
- RM - Remove
- MV - MOVE / Rename
- echo - echoes input
- nano - edits file
- touch - creates new file
- MKDIR - Creates new directory
- SU - Change User
- SSH - Establish SSH connection
- ps - Running Processes. Use AUX flag to see all processes running in the machine, including other users.
- TOP - Gives statistics about the processes running on your system. Refreshes every 10 seconds
- kill - Kills processes
- SIGTERM - Kill the process, but allow it to do some cleanup task beforehand
- SIGKILL - Kills the process, doest do any cleanup
- SIGSTOP - Stop/suspend a process
- systemctl - Allows to interact with systemd process/daemon
  - Start
  - Stop
  - Enable
  - Disable
  - Status
-APT - Install software - A part of the package management software also named apt
dplg - Package installer

## Processess
- namespaces are used by the OS to split up the resources available on the computer to processes, such as CPU, RAM and priority.
- Only those that are in the same namespace will be able to see each other.
- A process with an ID of 0 is a process that is started when the system boots.
- This process is the system's init on Ubuntu, such as systemd, which is used to provide a way of managing a user's processes and sits in between the operating system and the user.
- Any program or piece of software that we want to start will start as what's known as a child process of systemd.
- This means that it is controlled by systemd, but will run as its own process (although sharing the resources from systemd) to make it easier for us to identify and the likes.
- Some applications can be started on the boot of the system that we own.

## Backgrounding and Foregrounding in Linux
- Processes can run in two states: In the background and in the foreground
- For example, commands that you run in your terminal such as "echo" or things of that sort will run in the foreground of your terminal as it is the only command provided that hasn't been told to run in the background.

## CRON 
- Can be edited via crontab, a special file with formatting that is recognised by cron.
- Requires:
  - MIN . Minute
  - HOUR
  - DOM - Day of the month
  - Mon - MOnth
  - DOW - Day of the week
  - CMD - Command

## Package Management
- When software is submitted, it is submitted to an "apt" repository.
- If approved, their programs and tools will be released.
- You can one via add-apt-repository
- APT contains a suite of tools that allows us to manage the packages and sources of our software, and to install or remove software at the same time.
- When adding software, the integrity of what we download is guaranteed by the use of what is called GPG Gnu Privacy Guard keys. These are a safety check from the developers. If the keys do not match up to what your system.
- If the keys do not match up to what your system trusts and whaat the developers used, then the software will not be downloaded.
- 
- 
