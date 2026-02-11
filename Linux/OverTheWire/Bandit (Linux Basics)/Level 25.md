# Level Goal

Logging in to bandit26 from bandit25 should be fairly easy… The shell for user bandit26 is not /bin/bash, but something else. Find out what it is, how it works and how to break out of it.

    NOTE: if you’re a Windows user and typically use Powershell to ssh into bandit: Powershell is known to cause issues with the intended solution to this level. You should use command prompt instead.

## Approach:

These are two levels combined into one. The idea is that the interface for the level 26 is different, since it is not in bash, as the previous levels.
After inspecting the /etc/password from the level 25, i could see that there was an script running that changed the default shell for an logged user in level 26 to execute **more ~/text.t**
Upon logging in into the level 26, the connection is closed right away, because the program reads text.txt, which is very short, and upon reading it fully it closes the session.

## Solution found
The idea here is narrow by a lot the Shell Window. Because of the **more** command, when the terminal is small, and unable to show all the content, it will ask for input.
With this we can use **v** key to interact with **VIM** a text editor.
Afterwards we can set the default shell to to bash with **:set shell=/bin/bash** and we are back to working again on a bash shell.
To finish, we can then simply read the file to find the password. 

## Technologies used:
    -Powershell
    -SSH
    -Certificates
    -VIM
