## Security Devices

### Firewalls
- A firewall is a system, or group of systems, that enforces an access control policy between networks.

- Common Firewall Properties:
  - Firewalls are resistant to network attacks.
  - Firewalls are the only transit point between internal corporate networks and external networks because all traffic flows through the firewall.
  - Firewalls enforce the access control policy.
 
- Firewall Benefits:
  - They prevent the exposure of sensitive hosts, resources, and applications to untrusted users.
  - They sanitize protocol flow, which prevents the exploitation of protocol flaws.
  - They block malicious data from servers and clients.
  - They reduce security management complexity by off-loading most of the network access control to a few firewalls in the network.
 
- Firewall Limitations
  - A misconfigured firewall can have serious consequences for the network, such as becoming a single point of failure.
  - The data from many applications cannot be passed over firewalls securely.
  -  Users might proactively search for ways around the firewall to receive blocked material, which exposes the network to potential attack.
  -  Network performance can slow down.
  -   Unauthorized traffic can be tunneled or hidden as legitimate traffic through the firewall.

### Common Security Architectures
- Firewall design is primarily about device interfaces permitting or denying traffic based on the source, the destination, and the type of traffic. Some designs are as simple as designating an outside network and inside network, which are determined by **two interfaces** on a firewall.
  - Private and Public:
    - With two interfaces the firewall Private and Public is configured as follows:
      - Traffic originating from the private network is permitted and inspected as it travels toward the public network. Inspected traffic returning from the public network and associated with traffic that originated from the private network is permitted.
      - Traffic originating from the public network and traveling to the private network is generally blocked.
  - Delimitarized Zone:
    - A demilitarized zone (DMZ) is a firewall design where there is typically one inside interface connected to the private network, one outside interface connected to the public network, and one DMZ interface
      - Traffic originating from the private network is inspected as it travels toward the public or DMZ network. This traffic is permitted with little or no restriction. Inspected traffic returning from the DMZ or public network to the private network is permitted.
      - Traffic originating from the DMZ network and traveling to the private network is usually blocked.
      - 
