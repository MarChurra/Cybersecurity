## Wireless Communications 

- Infrastructure mode: A wireless router or AP connects wireless clients to a wired distribution system.
- Ad Hoc mode: A wireless router or AP is not present. Two devices connectm wireless in a P2P manner.
- Tethering: A variation of ad hoc, where a smart phone or tablet with cellular data access is used as a personal hotspot, working as an Access Point.

- The BSS (Basic Service Set): The range or extent of the connection of an Access Point. It has an BSSID associated, which is an MAC address.
- The ESS (Extended Service Set): The diagram of the network, with one or more BSA, being connected to a LAN, which is the distribution system.
- CSMA/CA (Carrier Sense Multiple Acess / Collision Avoidance): Listens to the wireless media, to diagonise the traffic between the APs and the endpoints, to prioritize the traffic. The steps are Listen > RTS > CTS > Transmit > ACK
- Wireless Client and AP Association: Discover AP > Authentication between the AP and the endpoint > Associated connection between both.

### Wireless versus Wired LANs
- WLANs use Radio Frequencies instead of cabpes ath the physical and data link layer.
- The IEEE has adopted the 802 LAN/MAN portfolio of computer network architecture standards. The two dominant 802 working groups are 802.3 Ethernet, which defined Ethernet for Wired Lans and 802.11 which defined ethernet for WLANs.
- WLAns connect client sto the network through a wirelress access point or wireless router.
- WLANs connect mobile devices that are often battery powered, as opposed to plugged-in LAN devices. Wireless NICs tend to reduce the battery life of a mobile device.
- WLAN support hosts that contend for access on the RF media (frequency bands). 802.11 prescribes collision-avoidance (CSMA / CA) instead of collision-detection (CSMA/CD) for media access to proactively avoid collisions within the media.
- WLANs usedd a different frame format than wired Ethernet LANs. WLANs require additional information in the Layer 2 header of the frame.
- WLANs raise more privacy issues because rradio frequencies can reach outside the facility.

### 802.11 Frame Structure
- All Layert 2 frames consists of a header, payload and Frame Check Sequence FCS setion. The 802.11 frame contains some more fields:
  - Frame control:  This identifies the type of wireless frame and contains subfields for protocol version, frame type, address type, power management, and security settings.
  - Duration: This is typically used to indicate the remaining duration needed to receive the next frame transmission.
  - Address1 - Receiving Wireless device or AP
  - Address2 - Transmitting wireless device or AP
  - Address3 - Sometimes contains the MAC address of the destination, such as the router interface / default gateway
  - Sequence Control - This contains information to control sequencing and fragmented frames.
  - Address4: Only needed in ad hoc mode
  - Payload: Data for transmission
  - FCS: Layer 2 error control
 
  ### CSMA/CA
  - WLANs are half-duplex, shared media configurations. Half-duplex means that only one client can transmit or receive at any given moment.
  - Shared media means that wireless clients can all transmit and receive on the same radio channel. This creates a problem because a wireless client cannot hear while it is sending, which makes it impossible to detect a collision.
  - To resolve this problem, WLANs use carrier sense multiple access with collision avoidance (CSMA/CA) as the method to determine how and when to send data on the network. A wireless client does the following:
    1. 
