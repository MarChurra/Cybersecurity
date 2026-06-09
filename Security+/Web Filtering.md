## Content Filtering
- Control traffic based on data within the content
- URL filtering, website category filtering
- Corporate control of outbound and inbound data
  - Sensitive materials
- Control of inappropriate content
  - Not safe for work
  - Parental controls
- Protection against evil
  - Anti-virus, anti-malware

## URL scanning
- Allow or restrict based on Uniform REsource Locator
  - Also called a URI Uniform Resource Identifier
  - Allow list / Block List
- Managed by category
  - Auction, Hacking, Malware, Travel, Recreation, etc.
- Can have limited control, since URLs are not the only way to surf
- Often integrated into an NGFW
  - Filters traffic based on category or specific URLº

## Agent Based
- Install client software on the users device
  - Usually managed from a central console
- Users can be located anywhere
  - The local agent makes the filtering decisions
  - Always on, always filtering
- Updates must be distributed to all agents
  - Cloud-based updates
  - Udpates shown at the console
  
## Proxies
  - Sits between the users and the external network
  - Receives the user requests and sends the request on their behalf
  - Useful for caching information, access control, URL filtering, content scanning
- Applications may need to know how to use the proxy (explicit proxy)
- Some proxies are invisible (transparent)

## Forward proxy
- A centralized Internal proxy
  - Commonly used to protect and control user access to the Internet

## Block Rules
- Based on specific URL
- Category of site content
- Different dispositions

 ## Reputation
 - Filter URLs based on perceived risk
   - A good reputation is allowed
   - A bad reputation is blocked
   - Risk: turstworthy, low risk, Medium risk suspicious, high risk
 - Automated reputation
 - Manual reputation is also possible
 - Add these dispositions to the URL filter

## DNS filtering
- Before connecting to a website, get the IP address
  - Perform a DNS lookup
- DNS is updated with real-time threat intelligence
  - Both commercial and public lists
- Harmful sites are not resolved
  - NO IP address, no connection
- This works for any DNS lookup, not just web filtering.
