- The OSI **Open System Interconnection Model** is an essential model used in networking. This critical model provides a framework dictating how all networked devices wil send, receive and interpret data.
- One of the main benefits of this model is that devices can have different functions and designs on a network while communicating with other devices.
- It consits of seven layer, each with different set of responsibilities.
- Encapsulation is also the process of adding pieces of information, as it passes through the several layers.

## Layers
  ### Layer 1 - Physical 
    - The physical components of the hardware used in networking and the lowest layer.
    - Devices use electrical signals to transfer data between each other in a binary numbering system (1 and 0)
    
  ### Layer 2 - Data Link
    - Focuses on the physical adressing of the transmission. It receives a packet from the network layer (including the IP for the remote PC) and adds in the physical MAC of the receiving endpoint.
    - PResents the data in a format suitable for transmission

  ### Layer 3 - Network
    - Where the routing & re-assembly of data takes place (from smaller to larger chunks)
    - Routing determines the most optimal path in which these cunks of data should be sent
    - Some Protocols at this layer determine exactly the optimal path for data to take. These protocols include **OSPF Open Shortest Path First** and **RIP Routing Information Protocol** 
    - It takes into account which path is the nshortest, what path is the most reliable, and which has the faster physical connection.
    - At this layer everything is dealt with via IP addresses. Devices such as routers capable of delivering packets using IP addresses are known as Layer 3 devices.

  ### Layer 4 - Transport 
