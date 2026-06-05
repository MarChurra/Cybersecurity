## Jump Server
- Access secure network zones
  - Provides an access mechanism to a protected network
- Highly-secured device
  - Hardened and monitored
- SSH / Tunnel / VPN to the jump server
  - RDP, SSH, or jump from there
- A significant security concern

## Proxies
- Sits between the users and the external network
- Receives the user requests and sends the request on their behalf (the proxy)
- Useful for caching information, access control, URL filtering, content scanning
- Applications may need to know how to use the proxy (explicit)
- Some proxies are invisible (transparent)

## Application proxies
- One of the simplest proxies is NAT
  - A network-level proxy
- Most proxies in use are app proxies
  - It understands the way the app works
- A proxy may only know one application or protocol
  - HTTP
- Or it can know multi proxies
  - HTTP, HTTPS, FTP, SSH...

## Forward Proxy
- An internal proxy
  - Commonly used to protect and control user access to the internet

## Reverse Proxy
- Inbound traffic from the internet to your internal network or service

## Open Proxy
- A 3rd party, uncontrolled proxy
  - Can be a significant security concern
  - Often used to circumvent existing security controls

## Load Balancer
- Distribute the Load
  - Multiple servers
  - Invisible to the end-user
- Large-scale implementations
  - Web server farms, database farms
- Fault Tolerance
  - Server outages have no effect
  - Very fast convergence

## Active/active Load Balancing
- Configurable load
  - Manage across servers
- TCP offload
  - Protocol overhead
- SSL offload
  - Encryption/Decryption
- Caching
  - Fast Response
- Prioritization
  - QoS
- content switching
  - Application-centric balancing
 
## Active/passive load balancing
- Some servers are active
  - Others are on standy
- If an active server fails, the passive server takes its place

## Sensors and collectors
- Aggregate information from network devices
  - Built-in sensors, separate devices
- Integrated into switches, routers, servers, firewalls, etc.

## Sensors and collectors
- Aggregate information from network devices
  - Built-in sensors, separate devices
  - Integrated into switches, routers, servers, firewalls, etc
- Sensors
  - IPS, firewalls logs, auth logs, web server access logs, database transactions, email logs
- Collectors
  - Properitary console IPs, Firewalls
  - SIEM consoles
  - Syslog Servers
  - Many Siems include a correlation engine to compare diverse sensor data 
