## The universal security control
- Standard issue
  - Home, office, and in your OS
- Control the flow of network traffic
  - Everything passes through the firewall
- Corporate control of outbound and inbound data
  - Sensisitve Data
- Control of Inappropriate content
  - NSF, parental control
- Protection against evil
  - ANti-virus, anti-Malware

## Network-based firewalls
- Filter traffic by port number or app
  - OSI layer 4 vs Layer 7 (more modern)
  - Traditional vs NGFW firewalls
- Encrypt traffic
  - VPN between sites
- Most firewalls can be layer 3 devices (routers)
  - Often sits on the ingress/egress of the network
  - Provide NAT

  ## UTM / All-in-one security appliance
  - Unified Threat Management
    - Web security gateway
    - URL filter / Content inspection
  - Malware inspection
  - Spam filter
  - CSU/DSU
  - Router, Switch
  - Firewall
  - IDS/IPS
  - Bandwidth shaper
  - VPN endpoint

## Next-Generation Firewall NGFW
- The OSI APP Layer 7
  - All data in every packet
- Can be called by more anmes
  - Application Layer gateway
  - Stateful multilayer inspection
  - Deep packet inspection
- requires some advanced decodes
  - Every packet must be analyzed and cateogrized before a security decision is determined

## NGFWs
- Network-based firewalls
  - Control traffic flows based on the application
- IPS
  - Identify the application
  - Apply application specific vulnerability signatures to the traffic
- Content filtering
  - URL filters
  - COntrol website traffic by category
- Web Application FIrewall WAF
  - Not like a normal firewall
    - Applies rules to HTTP/HTTPS conversations
  - Allow or deny based on expected input
    - Unexpected input is a common method of exploiting an application
  - SQL injection
    - Add your own commands to an app´s SQL query
  - A major focus of Payment Card Industry Data security Standard (DSS)
  
