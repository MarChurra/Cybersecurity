# Level Goal

The password for the next level is stored in a file readme in the homedirectory. Unfortunately, someone has modified .bashrc to log you out when you log in with SSH.

## Approach:
Trying to read the file directly does not work, since, after checking the file premissions, the fle is owned by the user bandit20 nad not our bandit19 (despiste of us being in the same user group).

The setuid is a specal file permission that will allow us to execute a program with the permission / credential of another user.

This way, CAT will work properly.

## Solution found

./bandit20-do cat /etc/bandit_pass/bandit20

## Technologies used:
    -Powershell
    -SSH
    -setuid
