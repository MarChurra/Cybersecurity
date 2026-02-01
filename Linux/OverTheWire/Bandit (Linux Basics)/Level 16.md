# Level Goal

The credentials for the next level can be retrieved by submitting the password of the current level to a port on localhost in the range 31000 to 32000.
First find out which of these ports have a server listening on them. Then find out which of those speak SSL/TLS and which don’t. 
There is only 1 server that will give the next credentials, the others will simply send back to you whatever you send to it.


## Approach:
This level asks of us to first make a verification of the ports listening on localhost, aswell as which ones require SSL/TLS encryption.
In order to narrow it down, i could use nmap to first check the ports that were listening, and then nc to try these ports for a valid RSA certificate.
After finding the only option available, it was a matter of attempting a connection with Openssl.
Despiste of haivng found the correct port, the server was kicking me out before iI received the credentials I needed. After veryting , this was because of EOF, which finished the connection before the server could responde.
With an extra flag to ignore it, I was able to receive the RSA Private Key that allowed me to connect via ssh to the next level.


## Technologies used:
    -Powershell
    -SSH
    -Openssl
    -SSL/TLS connections
    -nmap 
    -nc
    -Openssl
    -Certificates and Private Keys
