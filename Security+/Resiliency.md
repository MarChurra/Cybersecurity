## High Availability
- REdundancy does not always mean it is always available
  - May need to be powered on manually
- HA (High Availability)
  - Always on, always available
- May include many different components working together
  - Active/Active can provide scalability advantages
- Higher availability almost always means higher costs
  - Tehre is always another contigency you could add
  - Upgraded pwoer, high-quality server components, etc.

## Server Clustering
- COmbine two or more servers
  - Appears and opeartes as a single large server
  - Users only see and interact with one server
- Easily increase capacity and availability
  - Add more servers to the cluster
- Usually configured in the OS
  - All devices in the cluster commonly use the same OS
 
## Load Balancing
- Load is distributed across multiplle servers
  - The servers are often unaware of each other
- Distribute the load across multiple devices
  - Can be different OS, or the same.
  - The Load Balancer is the one who manages and maintains this load
- The load balancer adds or removes devices
  - Adds a server to increase capacity
  - Remove any servers not responding

## Site REsiliency
- Recovery site is prepped
  - Data is synchronized
- A disaster is called
  - Business processes failover to the alternate processing site
- Problem is addressed
  - This can take hours, weeks, or longer
- Revert back to the primary location
  - The process must be documented for both directions
 
## Hot Site
- An exact replica of your datacenter
- Stocked with hardware
   - Constantly updated
   - You buy two of everything
 - Applications and software are constanly updated
- Flip a switch and everything moves

## Cold Sites
- No hardware
  - Empty Building
- No data present, you bring it with you
- You bring the personal

## Warm Site
- A middle grouind, where soemd ata and equipment and staff may be present, but not all

## Geographic dispersion
- These sites should be phyisically different than the organization´s primary location
  - Many disruptions can affect a large area
- Can be a logistical challenge
  - Transporting Equipment
  - Getting employee´s on-site
  - Getting back to the main office

## Platform Diversity
- Every OS contains potential security issues
- Many security vulnerabilities are specific to a single OS
  - Windows vulnerabilities dont comonly affect Linux or macOS
- Use many different platforms
  - Different applications, clients, and OSes
  - Spread the risk around

## Multi-cloud systems
- There are many cloud providers
  - Amazon Web Service, Azure, Google Cloud, etc.
- Plan for cloud outages
- Plan for every contigency

## Continuity of Operations Planning COOP
- Not everything goes according to plan
  - Di9sasters can cause a disruption to the norm
- We rely on our computer systems
- Technology is pervasive
- There needs to ben an alternative
  - Manual Transactions
  - Paper receipts
  - Phone calls for transaction approvals
- These must be documented and tested before a problem occurs
- 
