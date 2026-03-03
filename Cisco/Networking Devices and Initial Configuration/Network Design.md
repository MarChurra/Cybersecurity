## Reliable Networks
### Network Architecture
- The term network architecture refers to the technologies that support the intrastructure and the programmed services and rules, or protocols, that move data across the network.
- There are four basic characteristics that networks architects must address to meet end user expectations:
  - Fault Tolerance
  - Scalability
  - Quality of Service QoS
  - Security
 
### Fault Tolerance
- A fault tolerant network is one that limits the number of affected devices during a failure. It is built to allow quick recovery when such a failure occurs.
- These networks depend on multiple paths between the source and destination of a message.
- If one path fails, the messages are instantly sent over a different link. This is known as **redundancy**
- Implementing a packet-switched network is one way that reliable networks porvide redundancy.
- Packet swtcihing splits traffic into patckets that are routed over a shared network.
- A single message is broken into message blocks, called packets. Each packet has the necessary addressing information of the source and destination of the message.
- The routers within the network switch the packets based on the condition of the network at the moment.
- This means that all the packets in a single message could take very different pathjs to the same destination.

### Scalability
- A scalable network explands quickly to support new users and applications. It does this without degrading the performance of services that are being accessed by existing users.

### Quality of Service
- An increasing requirement of networks today.
- Congestion occurs when the demand for bandiwth exceeds the amount available.
- Network bandwidth is measured in the number of bits that can be transmitted in a single seconds, or bits per second **bps**.
- When simultaneous communications are attempted across the network, the demand for network bandwidth can exeed its avaialbility, creating network congestion.
- When the volume of traffic is greater than what can be transported across the network, devices will hold the packets in memory until resource sbecome available to transmit them.
- With QoS policy in place, a router can manage the flow of data and voice traffic, giving priority to voice communications if the network experiences congestion.
- The focus of QoS is to prioritize time-sensitive traffic.

### Netowrk Security
- Network adminstrators must address the two types of network security concerns: network infrastructure security and information security.
- Securing the network infrastructure includes physically securing devices that provide network connectivity and preventing unauthorized access to the management software that resides on them.
- Network administrators must also protect the information contained within the packets being transmitted over the network, and the information stored on network attached devices. There are three primary requirements to achieve the goals of network security.
  - Confidentiality
  - Integrity
  - Availability

## Hierachical Network Design
### Layers of a Network
- IP traffic is managed based on the characetristics and devices associated with each of the three layers of the hierachical network design model: Access, Distribution and Core.
  - Access Layer:
    - Provides a connection point for end user devices to the network and allows multiple hosts to connect to other hosts through a network device, such as a swtich, or a wireless access point.
    - All devices within a single access layer will have the same network portion of the IP address
    - If a message is destined for a local host, based on the network portion of the IP address, the message remains local. If it is destined for a different network, it is passed up to the distribution layer.
    - Switches provide the connection to the distribution layer devices, usually a Layer 3 device such as a router of Layer 3 Swtich.
 - Distribution Layer
   - Provides a connection point for separete networks and controls the flow of information between the networks. It typically contains more powerfull switches, than the acess layer, as well as routers for routing between networks.
   - Distribution layer devices control the type and amount of traffic that flows from the access layer to the core layer.
- Core Layer
   - A high-speed backbone layer with redundant connections. It is responsible for trasporting large amounts of data between multiple end networks.
   - Core layer devices typically include very powerfull, high-speed switches and routers.
   - The main goal of this layer is to transport data quickly.
