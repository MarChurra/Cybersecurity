## Identification
- This is who you claim to be

## Authentication
- Prove who you say you are
- Password and other authenticaiton methods
- You can rely on certificates

## Authorization
- Based on your identificaton and authentication, checks your roles and accessess

## Accounting
- Resources used and logs


## Authenticating Systems
- You have to manage several devices
- A system can´t type a password, and you may not want to store one
- You can authenticate a device, with a signed certificate digitally on the device
- Other business processes rely on the certificate
  - Access to the VPN from authorized devices
  - Management software can validate the end device
 
## Certificate Authentication
- An organization has a trusted CA Certificate Authority
  - Most organizations maintain their own CAs
- The organization creates a certificate for a device
  - And digitally signs the certificate with the organization´s CA
- The certificates can now be included on a device as an authentication factor
  - The CA´s digital signature is used to validate the certificate

## Certificate-based authentication
- The Server is signed by a Root CA
- The devices are then signed by the CA of our server

## Authorization models
- The user or device has now authenticated
  - What do they now have access?
  - Time to apply an authorization model
- Users and Services -> data and apps
  - Associating individual users to access rights does not scale
- Put an authorization model in the middle
  - Define by Roles, Organizations, Attributes, etc.
- Adds an abstraction, reducing complexity and creates a clear relationship between users and resources
- Administration is streamlined, via Groups, for Examples. Easier to understand and supports any number of users or resources
## No-Authorization Model
- Uses a simple relationshp of User '> Resource, which does not scael well.
- Difficult to udnerstand why an authorizaion may exist

  
