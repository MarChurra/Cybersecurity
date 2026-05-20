- Many netwroks are relatively open on the inside.
  - OPnce you are through the firewall, there are few security controls.
- Zero trust ia a holistic approach to network security
  - Covers every device, every process, every person
- Everything must be verified
  - Nothing is inherently trusted
  - MFA, encryption, system permissions, additional firewalls, monitoring and analytics, etc

## Planes of Operation
- Split the network into functional planes
  - Applies to physical, virtual and cloud components

### Data Plane
  - Process the frames, packets, and network data
  - Processing, forwarding, trunking, encrypting, NAT

### Control Plane
- Manages the actions of the data plane
- Define polices and rules
- Determines how packets should be forwarded
- ROuting taboles, session tables, NAT tables

### Controlling Trust

#### Adaptive Identity
- Consider the source and the requested resources
- Multiple risk indicators, relationship to the organization, physical location, type of connection, IP address, etc
- Make the authentication stronger, if needed

#### Threat Scope Reduction
- Decrease the number of possible entry points
- Create a Policy-Driven access control
- Combine the adaptive identity with a predefined set of rules

## Security Zones
- More than a one-to-one relationship
- Broad categorizations provide a security-related foundation

- Where are you coming from and where are you going?
  - Trusted, untrusted
  - Internal network, external network
  - VPN 1, VPN5, VPN 11
  - Marketing, IT, Accounting, HR
 
- Using the zones may be enoguh by itself to deny access
  - For examples, Untrusted to Trusted Zone Traffic
  - Some zones are implicitly trusted, such as Trusted to Internal Zone Traffic

 ## Policy enforcement point
 - Subjects and systems
   - End users, applications, non-human entities
 - Policy Enforcement Point PEP
   - The gatekeeper
 - Allow, monitor, and terminate connections
   - Can consist of multiple components working together
  
## Applying trust in the planes
- Policy Decision Point
  - There is a process for making an authentication decision
- Policy Engine
  - Evaluates each access decision based on policy and other information sources
  - Grant, deny, or revoke
- Policy Administrator
  - Communicates with the PEP
  - Generates access tokens or credentials
  - Tells the PEP to allow or disallow access
- The Policy Decision point is the crossover of the Policyt Engine and the Policy Administrator 
