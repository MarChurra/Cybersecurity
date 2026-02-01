# Level Goal

A program is running automatically at regular intervals from cron, the time-based job scheduler. Look in /etc/cron.d/ for the configuration and see what command is being executed.

## Approach:
Viewing the cronjobs, I found one linked to Bandit22. After inspecting it, was able to see that it run every minute, even on reboot, and that it used a script saved in the bin/bash.
After going to the folder mentioned above, I was able to find the script itself. Upon further inspection, it was reading the ocntents of the file where the password for bandit22 is, and outputting it into a tmp file.
After that, it was a question, to use **CAT** to read the password.

## Solution found

## Technologies used:
    -Powershell
    -SSH
    -Cron
    -Cronjob
    -Cat 
