# Level Goal

There is a setuid binary in the homedirectory that does the following: it makes a connection to localhost on the port you specify as a commandline argument. 
It then reads a line of text from the connection and compares it to the password in the previous level (bandit20). If the password is correct, it will transmit the password for the next level (bandit21).

NOTE: Try connecting to your own network daemon to see if it works as you think

## Approach:
Much like the previous challenge, there is a setuid binary that runs as an executable program. Unlike the previous challenge, I could run this program right away, without speicfing the user.
This alerted me to the way privilege escalations work in Unix systems, making executables quite dangerous and setuid binaries, since they run right away with all the necessary permissions (it reads the password file inside the home directory, even though it does not belong to the user i am using).
Before running the program, I needed to use **NC (netcat)** to create a new port on the localhost and use echo to specify what that server outputs (the password of the previous challenge).
In this way, I created a daemon that could work alongside the executable to send me the password.

## Solution found

echo 'PASSWORD' | nc -l -p 1234 

./suconnect 1234

## Technologies used:
    -Powershell
    -SSH
    -setuid
    -nc
    -echo
