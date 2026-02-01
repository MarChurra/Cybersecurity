The password for the next level is stored in /etc/bandit_pass/bandit14 and can only be read by user bandit14. 
For this level, you don’t get the next password, but you get a private SSH key that can be used to log into the next level.
Look at the commands that logged you into previous bandit levels, and find out how to use the key for this level.


One of the challenges that is much more acessible then it seems. There is a private RSA key inside the server which belongs to a user inside the machine. There is no password to the game, the goal is to use that RSA private key to establish an ssh connection to the next game.
After overthinking it and using chmod to give me rw permissions to a copied file of the key, I kept getting blocked when attempting to use the SSH connection, since it was refusing to connect because i was making the connection from within the remote session.
Locally I was able to find success, in a simpler way.

## Technologies used:
    -Powershell
    -SSH
    -chmod
