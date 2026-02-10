- The User Datagram Protocol  is another protocol used to communicate data between devices.
- Unlike its brother TCP, UDP is stateless and does not require constant connection between the two devices for data to be sent.
- The Three-Way handshake does not occur, nor is there any sync between devices
- It is much fater than TCP, since it does not care about the quality of the data that is received.
- UDP leaves the application to decide if there is any control over how quickly packets are sent.
- No safeguards for data integrity

** Headers of a UDP Packet:
  - Time To Live TTL - Sets an expiry timer for the packet, so it does not clog up the network, if it never manages to reach a host or escape.
  - Source Address
  - Destination Address
  - Source Port - The port opened by the sender to send the UDP Packet from
  - Destination Port
  - Data

** Ports
- Ports are essential for data to be exchanged.
- These ports enforce what can park and where, rejecting incompatible data transfers.
- Networking devices also use ports to enforce strict rules when communcating with one another.
- When a connection is estabilished between devices, any data sent or received by a device will be sne tthrough these ports.
- Ports are a numerical value between 0 and 65535
- There is a standard for applications. Web browser data is sent over by port 80, for example.
- Any port within 0 and 1024 is known as a **common port**

- FTP - Port Number 21
- SSH - Port 22
- HTTP - Port 80
- HTTPS - Port 443
- SMB - 445
- RDP - 3389
