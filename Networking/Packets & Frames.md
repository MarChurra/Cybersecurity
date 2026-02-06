- Packets and frames are small pieces of data that, when forming together, make a larger piece of information or message. However, they are two different things in the OSI model.
- A packet is a piece of data from the Layer 3 Network. It contains information such as an IP header and a payload.
- A frame, however, is used at Layer 2 Data link, which encapsulates the packet and adds additional information such as the MAC address.
- Packets are an efficient way of communicating data across networked devices, because this data is exchanged in small pieces, there is less chance of bottlenecking.
- Packets have different structures that are dependant upon the type of packet that is being sent. Networking is full of standards and protocols that act as a set of rules for how the packet is handled on a device.
- A packet using the Internet Protocol will have a set of headers that contain additional pieces of information to the data that is being sent across a network.

    ### Headers:
    - Time To Live: Sets an expiry timer for the packet to not clog up your network if it never manages to reach a host or escape.
    - Checksum - Provides integrity checking for protocols such as TCP/IP. If any data is changed, this value will be different from what was expected and therefore corrupt.
    - Source Address - The IP address of the device that the packet is being sent from.
    - Destination Address 
