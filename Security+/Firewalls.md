## Network-based Firewalls
- Filter traffic by port number or application
  - Traditional vs NGFW
- Encrypt traffic
  - VPN between sites
- Most firewalls can be layer 3 devices (routers)
- Often sits on the ingress/egress of the network
- Can do NAT and Routing

## NGFW Next-Generation Firewall
- The OSI Application Layer
  - Layer 7 Firewall
- Can be called different names
  - Application Layer gateway
  - Stateful multilayer inspection
  - Deep packet inspection
- Requires some advanced decodes
  - Every packet must be analyzed, categorized, and a security decision determined
- Ports and protocols
  - Make forwarding decisions based on protocol TCP or UDP port number
  - Traditional port-based firewalls
  - Add to an NGFW for additional security policy options
- Based on destination protocol and port (socket)
  - Web server
  - SSH Server
  - Microsoft RDP
  - DNS query
  - NTP

## Firewall rules
- A logical path
  - Usually top-to-bottom
- Can be very general or very specific
  - Specific rules are usually at the top
- Implicit deny
  - Most firewalls include a deny at the bottom
- Access Control Lists ACLS
  - ALlow or dissalow traffic
  - Grouping into categories
 
## Screened subnet
- An additional layer of security between the you and the internet
  - Public access to public resources
  - Private data remains inacessible
 
## IPS rules
- Intrusion Prevention System
  - Usually integrated into an NGFW
- Different ways to find malicious traffic
  - Look at traffic as it passes by
- Signature-based
  - Look for a perfect match
- Anomaly-based
  - build a baseline of the normal
  - Unusua traffic patterns are blocked
- You determine what happens when unwanted traffic appears
  - block, allow, send an alert, etc.
- Thousand of rules
  - Or more
- Rules can be customized by group
  - Or as individual rules
- This can take time to find the right balance
  - Security / alert "noise"
