# Level Goal

A program is running automatically at regular intervals from cron, the time-based job scheduler. Look in /etc/cron.d/ for the configuration and see what command is being executed.

NOTE: This level requires you to create your own first shell-script. This is a very big step and you should be proud of yourself when you beat this level!

NOTE 2: Keep in mind that your shell script is removed once executed, so you may want to keep a copy around…

## Approach:

The obstacle of this level is the script running in chron, which deletes the contents of the tmp files for the usr bandit24.

myname=$(whoami)

cd /var/spool/$myname
echo "Executing and deleting all scripts in /var/spool/$myname:"
for i in * .*;
do
    if [ "$i" != "." -a "$i" != ".." ];
    then
        echo "Handling $i"
        owner="$(stat --format "%U" ./$i)"
        if [ "${owner}" = "bandit23" ]; then
            timeout -s 9 60 ./$i
        fi
        rm -f ./$i
    fi

In this scenario, we need to create and run our own script that will sucessfully retrieve tht password, before it is cleared.

## Solution found
The approach I found was to create my own script, which essentially copied the contents of the file containing into the password into my own temp file, so I can read it.

**#!/bin/bash
cat /etc/bandit_pass/bandit24 > /tmp/bandit24_pass**

After using **CHMOD** to give me the necessary permissions on the tmp folder and this file, i was then able to add this script into the spool to run the sript with CRON and then use CAT to Read the newly created file with the password.

## Technologies used:
    -Powershell
    -SSH
    -Cron
    -Cronjob
    -CHMOD
    -Bash script
