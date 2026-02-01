# Level Goal

The password for the next level is stored in a file readme in the homedirectory. 
Unfortunately, someone has modified .bashrc to log you out when you log in with SSH.

## Approach:
A simpler challenge then it seems. My first instinct was to see if I could manipulate the .bashrc first, to enable the remote shell connection once again.
However, after finding out that the same line where I use ssh to connect to the server, can also run code right away, why not simply read the file right away with Cat and retrieve the password?


## Technologies used:
    -Powershell
    -SSH
    -Cat
