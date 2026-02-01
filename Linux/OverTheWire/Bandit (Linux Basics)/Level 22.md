# Level Goal

A program is running automatically at regular intervals from cron, the time-based job scheduler. Look in /etc/cron.d/ for the configuration and see what command is being executed.

NOTE: Looking at shell scripts written by other people is a very useful skill. The script for this level is intentionally made easy to read. If you are having problems understanding what it does, try executing it to see the debug information it prints.

## Approach:
Much like the preivous challenge, it required to read what the script was doing first. 
IT was running every minute and upon reboot and it outputted the following:

**#!/bin/bash

myname=$(whoami)
mytarget=$(echo I am user $myname | md5sum | cut -d ' ' -f 1)

echo "Copying passwordfile /etc/bandit_pass/$myname to /tmp/$mytarget"

cat /etc/bandit_pass/$myname > /tmp/$mytarget**

The first step was to understand what was happening in this script.
It was first settings two variables, one where it sets it to the name of the user running the script (bandit23) and the other sets a variable with an hash, that is obtaining by piping the result of $myname, into md5sum, and then retrieving only the hash, without trailing whitespaces.
It then echos that it will copy the password file into a new tmp file, with the name of the newly created hash.

## Solution found
Running with Echo the exact same script as above **mytarget=$(echo I am user $myname | md5sum | cut -d ' ' -f 1)** allowed me to easily see what was being printed.
With that, I only had to then use the hash I got to access the temp file with the password.


## Technologies used:
    -Powershell
    -SSH
    -Cron
    -Cronjob
    -Echo
