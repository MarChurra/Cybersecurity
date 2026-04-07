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
    1. Listens to the channel to see if it is idle, which means that is senses no other traffic is currently on the channel. The channel is also called the carrier.
    2. Sends a ready to send (RTS) message to the AP to request dedicated access to the network.
    3. Receives a clear to send (CTS) message from the AP granting access to send.
    4. If the wireless client does not receive a CTS message, it waits a random amount of time before restarting the process.
    5. After it receives the CTS, it transmits the data.
    6. All transmissions are acknowledged. If a wireless client does not receive an acknowledgment, it assumes a collision occurred and restarts the process.
   
  ### Wireless Client and AP Association
  - For wireless devices to communicate over a network, they must first associate with an AP or wireless router. An important part of the 802.11 process is discovering a WLAN and subsequently connecting to it. Wireless devices complete the following three stage process, as shown in the figure:
    1. Discover a Wireless AP
    2. Authenticate with AP
    3. Associate with AP
 - To have a sucessfull association, a wireless client and an AP must agree on specific parameters. Parameters must then be configured on the AP and subsequently on the client to enable the negotation of a sucessfull association.
 - SSID: The SSID name appears in the list of available wireless networks on a client. In larger organizations that use multiple VLANs to segment traffic, each SSID is mapped to one VLAN. Depending on the network configuration, several APs on a network can share a common SSID.
 - Password
 - Network Mode: This refers to the 802.11a/b/g/n/ac/ad WLAN standards. APs and wireless routers can operate in a Mixed mode meaning that they can simultaneously support clients connecting via multiple standards.
 - Security mode: This refers to the security parameter settings, such as WEP, WPA, or WPA2. Always enable the highest security level supported.
 - Channel Settings: This refers to the frequency bands used to transmit wireless data. Wireless routers and APs can scan the radio frequency channels and automatically select an appropriate channel setting. The channel can also be set manually if there is interference with another AP or wireless device.

### Passive and Active Discover Mode
- Passive Mode: In passive mode, the AP openly advertises its service by periodically sending broadcast beacon frames containing the SSID, supported standards, and security settings. The primary purpose of the beacon is to allow wireless clients to learn which networks and APs are available in a given area. This allows the wireless clients to choose which network and AP to use.
- Active Mode: In active mode, wireless clients must know the name of the SSID. The wireless client initiates the process by broadcasting a probe request frame on multiple channels. The probe request includes the SSID name and standards supported. APs configured with the SSID will send a probe response that includes the SSID, supported standards, and security settings. Active mode may be required if an AP or wireless router is configured to not broadcast beacon frames.
       
### Wireless Devices -AP, LWAP and WLC
- A common wireless data implementation is enabling devices to connect wirelessly via a LAN. In general, a wireless LAN requires wireless access points and clients that have wireless NICs
-  Home and small business wireless routers integrate the functions of a router, switch, and access point into one device
-  Note that in small networks, the wireless router may be the only AP because only a small area requires wireless coverage. In larger networks, there can be many APs.
-  All of the control and management functions of the APs on a network can be centralized into a Wireless LAN Controller (WLC).
-  When using a WLC, the APs no longer act autonomously, but instead act as lightweight APs (LWAPs)
-  LWAPs only forward data between the wireless LAN and the WLC.
-  All management functions, such as defining SSIDs and authentication are conducted on the centralized WLC rather than on each individual AP. A major benefit of centralizing the AP management functions in the WLC is simplified configuration and monitoring of numerous access points

## WLAN Threats

### Wireless Security Overview
- A WLAN is open to anyone within range of an AP and the appropriate credentials to associate to it. With a wireless NIC and knowledge of cracking techniques, an attacker may not have to physically enter the workplace to gain access to a WLAN.
- Attacks can be generated by outsiders, disgruntled employees, and even unintentionally by employees. Wireless networks are specifically susceptible to several threats, including:
  - Interception of data: Wireless data should be encrypted to prevent it from being read by eavesdroppers.
  - Wireless Intruders: Unauthorized users attempting to access network resources can be deterred through effective authentication techniques.
  - DoS attacks:  Access to WLAN services can be compromised either accidentally or maliciously. Various solutions exist depending on the source of the DoS attack.
  - Rogue APs: Unauthorized APs installed by a well-intentioned user or for malicious purposes can be detected using management software.
 
### DoS Attacks
- Wireless DoS attacks can be the result of:
  - Improperly configured devices: Configuration errors can disable the WLAN. For instance, an administrator could accidently alter a configuration and disable the network, or an intruder with administrator privileges could intentionally disable a WLAN.
  - A malicious user intentionally interfering with the wireless communication: Their goal is to disable the wireless network completely or to the point where no legitimate device can access the medium.
  - Accidental Interference: WLANs are prone to interference from other wireless devices including microwave ovens, cordless phones, baby monitors, and more, as shown in the figure. The 2.4 GHz band is more prone to interference than the 5 GHz band.
- To minimize the risk of a DoS attack due to improperly configured devices and malicious attacks, harden all devices, keep passwords secure, create backups, and ensure that all configuration changes are incorporated off-hours.
- Monitor the WLAN for any accidental interference problems and address them as they appear. Because the 2.4 GHz band is used by other devices types, the 5 GHz should be used in areas prone to interference.

### Rogue Access Points
- A rogue AP is an AP or wireless router that has been connected to a corporate network without explicit authorization and against corporate policy. Anyone with access to the premises can install (maliciously or non-maliciously) an inexpensive wireless router that can potentially allow access to a secure network resource.
- Once connected, the rogue AP can be used by an attacker to capture MAC addresses, capture data packets, gain access to network resources, or launch a man-in-the-middle attack.
- A personal network hotspot could also be used as a rogue AP. For example, a user with secure network access enables their authorized Windows host to become a Wi-Fi AP. Doing so circumvents the security measures and other unauthorized devices can now access network resources as a shared device.
- To prevent the installation of rogue APs, organizations must configure WLCs with rogue AP policies, and use monitoring software to actively monitor the radio spectrum for unauthorized APs.

### Main-In-The Middle Attack
- In a man-in-the-middle (MITM) attack, the hacker is positioned in between two legitimate entities in order to read or modify the data that passes between the two parties. There are many ways in which to create a MITM attack.
- A popular wireless MITM attack is called the “evil twin AP” attack, where an attacker introduces a rogue AP and configures it with the same SSID as a legitimate AP
- Locations offering free Wi-Fi, such as airports, cafes, and restaurants, are particularly popular spots for this type of attack due to the open authentication.
- Wireless clients attempting to connect to a WLAN would see two APs with the same SSID offering wireless access. Those near the rogue AP find the stronger signal and most likely associate with it.
- User traffic is now sent to the rogue AP, which in turn captures the data and forwards it to the legitimate AP
- Return traffic from the legitimate AP is sent to the rogue AP, captured, and then forwarded to the unsuspecting user. The attacker can steal the user’s passwords, personal information, gain access to their device, and compromise the system.
- Defeating an attack like an MITM attack depends on the sophistication of the WLAN infrastructure and the vigilance in monitoring activity on the network. The process begins with identifying legitimate devices on the WLAN. To do this, users must be authenticated. After all of the legitimate devices are known, the network can be monitored for abnormal devices or traffic.

## Secure WLANs

### SSID Cloacking and MAC Address Filtering
