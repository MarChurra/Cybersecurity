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
    - This layer plays a vital part in trasmitting data across a network.
    - When data is sent between devices, it follows one of two different protocols that are decided based upon several factors:
      - TCP
      - UDP
    - TCP: 
        - The transmission Control Protocol, is designed with reliability and guarantee in mind. It reserves a constant connection between the two devices for the amount of time it takes for the data to be sent and received.
        - It checks for errors by design. This is how it guarantees that data sent from the small chunks in the session layer 5 has then been received and reassembled in the same order.
        - While it guarnatees the accuracy of data, it requires a reliable connection. If one small chunk is not received, the entire chunk of data cannot be used.
        - It can syncronize two devices to prevent each other from being flooded with data, but a slow connection can bottleneck another device, as the connection will be reserved on the receiving computer the whole time.
        - It performs a lot more processes for realibility, but is much slower than UDP.
        - It is used for situations such as file sharing, internet browsing or emails. 
        - Files are broken down into smaller pieces of data **packets**. The server divides the packets and the host or computer re-constructs them.
    - UDP:
        - User Datagram Protocol is not early as advanced as TCP. It does not have error checking and realibility. Any data that gets sent via UDP is sent to the computer whether it gets there or not.
        - There is no syncronisation between the two devices or guarantee.
        - Is much faster than TCP, but does not care if data is properly received.
        - It leaves the application layer to decide if there is any control over how quickly packets are sent. It is flexibile to software developers.
        - It does not reserve a continuous connection, making it unstable for worse connections, which can impact the user experience.
        - Usefull in situations where there are small pieces of data being sent. Such as video streaming and protocols such as ARP and DHCP 

  ### Layer 5 - Session
    - Once data has been translated or formatted from the presentation layer, the session layer will begin to create and maintain the connection to other computer for which the data is destined. When a connection is estabilished, a session is created.
    - This layer is also responsible for closing the connection if it hasn´t been used in a while or if it is lost. A session can also contain checkpoints, where if the data is lost, only the newest pieces of data are required to be sent, saving bandwidth.
    - Sesions are unique, meaning that data cannot travel over different sessions.

  ### Layer 6 - Presentation
    - This is the layer in which standardisation starts to take place. Because software developers can develop any software such as an email client differently, the data stills needs to be handled in the same way, no matter the software.
    - This layer acts a translator for data to and from the application layer. The receiving computer will also udnersatnd data sent to a computer in one format destined for in another format. 
    - Security features, such as encryption with HTTPS occur at this layer.

 ### Layer 7 -Application   
     - The layer in which protocols nd rules are in place to determine how the user should interact with data.
     - Applications provide a GUI for users to interact with Data.
