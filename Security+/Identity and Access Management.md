## IAM
- Applications are available everywhere
- Data can be located anywhere
- Many different application users
  - Employees, vendors, contractors, customer
- Give the right permissions to the right people at the right time

## Identity and Access Management
- Identify Lifecycle management
  - Every entity gets a digital identity, human or non-human
- Access Control
  - An entity only gets access to what they need
- Authentication and authorization
  - Entities must prove they are who they claim to be
- Identity governance
  - Track an entity´s resource access
  - May be a regulatory requirement

## Provisioning /de-provisioning user accounts
- The user account creation process
  - And the account removal process
- Provisioning and de-provisoning occurs for certain events
  - Hiring, transfers, promotions, job separation
- Account details
  - Name, attributes, group permissions, other permissions
- An important part of the IAM process
  - An initial checkpoint to limit access
  - Nobdy gets Administrator process
 
## Permission assignments
- Each entity gets limited permissions
  - Just enough to do their job
  - Group assignments are common
- Storage and files can be private to that user
  - Even if another person is uisng the same computer
- No privileged access to the OS
  - Specifically not allowed on a user account

## Identity Proofing
- I could be anyone
  - The IAM process should confirm who the user is
- Resolution
  - Who the system thinks you are
- Validation
  - Gathering information from the user (password, MFA, security questions)
- Verification / Attestation
  - Passport, in person meeting, etc.
  - Automated verification is also an option

## Single sign-on SSO
- Provide credentials one time
  - Get access to all available or assigned resources
  - No additional authentication required
  -   Usually limited by time
- A single authentication can work for 24 hours, it can expire after the timer expires
- The underlying authentication infrastrucutre must support SSO

## LDAP Lightweight Directory Access Protocol
- Protocol for reading and writing directories over an IP network
  - A organized set of records
- X.500 specification was written by the Internal Telecommunications Union
- DAP ran on the OSI protocol stack
  - LDAP is lightweight
- LDAP is the protocol used to query and update an X.500 directory
  - used in Active Directory, Apple Open Directory, Novell eDirectory, etc.

## X.500 Distinguished Names
- Attribute= value pairs
- Most specific attribute is listed first
  - This may be similar to the way you already think

## X.500 Directory Information Tree
- Hierarchical Structure
  - Builds a tree
- Container Objects
  - Coutry, OU, organizations
- Leaf objects
  - Users, nodes

## Security Assertion Markup Language SAML
- Open standard for authetnication and authorization
  - You can authenticate through a third-party to gain access
  - One standard does it all
- Not originally designed for mobile Devices

## OAuth
- Authorization Framework
  - Determines what resources a user will be able to access
- Created by Twitter, Google, and many others
- Not an authentication protocol
  - OpenID Connect handles the sign-on authentication
  - OAuth provides authorizationb etween apps
 
## Federation
- Provide Network access to others
  - Not just employees - Partners, suppliers, customers, etc.
  - Provides SSO and more
- Third-parties can establish a federated network
  - Authenticate and auhtorize between the two organizations
- The third-parties must establish a trust relationship and the degree of trust

## Interoperability
- Many different ways to communicate with an authentication server
  - More than a simple login process
- often determined by what is at hand
  - VPN concentrator can talk to a LDAP server
  - We have an LDAP server
- A new app uses OAuth
  - Need to allow authentication API access
- The interoperability is dependent on the environment
