- Transmission Control Protocol consists of four layers and is arguably just a summarised version of the OSI model. These Layeers are:
   - Application
   - Transport
  - Internet
  - Network Interface
- Information is added to each layer of the TCP model as the piece of data or packet traverses it. This process is encapsulation. The reverse is decapsulation.
- One defining feature is that it is connection-based, which means that TCP must establish a connection between both a client and a device acting as a server before data is sent.
- TCP guarantess that any data sent will be received on the other end. This is named the Three-way Handshake.

- TCP Packets contain various section of information known as headers that are added from encapsulation:
  - Source port - Value of the port opened by the sender to send the TCP packet from. Chosen randomly out of the available ports from 0-65535)
  - Destination Port - This value is the port number that an application or service is running on the remote host. Value not chosen at random.
  - Source IP
  - Destination IP
  - Sequence Number - When a connection occurs, the first piece of data transmitted is given a random number.
  - Acknowledgement Number - After a piece of data has been given a sequence number,. the number for the next piece of data will have that number +1.
  - Checksum
  - Data - Where teh data, bytes, of a file that is being transmitted, is stored.
  - Flag - Determines how the packet should be handled by either device during the handshake process.
 
  ### Three-Way Handshake
  - Step 1 - SYN - Initial packet sent by a client during the handshake. This packet is used to initiate a connection and syncronise the twoi devices together.
  - Step 2 - SYN/ACK - This packet is sent by the receiving device (server) to acknowledge the syncronisation attempt from the client-
  - Step 3- ACK - The acknowledgement packet can be used by either the client or server to acknowledge that a series of messages/ packets have been sucessfully received
  - Step 4 - Data - Oncer a connection has been established, data is sent via the DATA message.
  - Step 5 - FIN-  This packet is used to cleanly close the connection after it has been complete
  - # - RST - This packet abruptly ends all communication. Indicates that there was some problemduring the process.
