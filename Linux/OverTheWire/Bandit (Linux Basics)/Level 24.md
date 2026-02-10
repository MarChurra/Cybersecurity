# Level Goal

A daemon is listening on port 30002 and will give you the password for bandit25 if given the password for bandit24 and a secret numeric 4-digit pincode. There is no way to retrieve the pincode except by going through all of the 10000 combinations, called brute-forcing.
You do not need to create new connections each time

## Approach:

The daemon is constantly listening for the correct passcode, in order to echo the password for the next level.
Brute forcing 10000 combinations manually would be time consuming, and as such, a script would make it more convenient to solve.

## Solution found
This solution worked, however it seemed to quite longer then expected, since it manually tried a nc connection to check for the pincode everytime the script ran. There could be a better solution, a faster one, however i wasn´t able to test one.

#!/bin/bash

for i in $(seq -w 0000 9999)
do
    echo "UoMYTrfrBFHyQXmg6gzctqAwOmw1IohZ $i"
done | nc localhost 30002 > result.txt


This will run a seq from 0 to 9999, making it 10000 attempts. It will echo the password from the previous level alongisde the index for the current sequence.

It will then use that result and funnel it into the netcat connection and output the resulting echo in a new file.

## Technologies used:
    -Powershell
    -SSH
    -CHMOD
    -Bash script
    -Netcat
