## Digital Certificates
- A public key certificate
  - Binds a public key with a digital signature
  - And other details about the key holder
- A digital signature adds trust- PKI uses a CA for additional trust
  - Web of Trust adds other users for additional trust
- Certificate creation can be built into the OS
 - Part of Windows Domain Services or 3rd party Tools

## Digital certificates Content
- X.509
  - Standard Format
- Certiificate Details
  - Serial number
  - Version
  - Signature Algorithm
  - Issuer
  - Name of the cert holder
  - Public key
  - Extensions

## Root of Trust
- Everything associated with IT security requires trust
- How to build trust from something unknown
  - Someone/something trustworthy provides their approval
- Refer to the root of trust
  - An inherently trusted component
  - Hardware,software,firmware,or other component
  - Hardware security Module, Secure Enclave, CA, etc.

## Certificate Authorities
- You connect to a random website, do you trist it?
- Need a good way to trust an unknown entity
  - Use a trusted third-party
  - An authority
- CA has digitally signed the website certificate
  - You trust the CA, therefore you trust the website
  - Rea-time Verification

## Third-Party certificate authorities
- built-in to your browser
  - any browser
- Purchase your web site certificate
  - It will be trusted by everyone´s browser
- CA is responsible for vetting the request
  - They will confirm the certificate owner
  - Additional verifiication information may be required by the CA

## Certificate Signing Requests
- Create a key pair, then send the public key to the CA to be signed
  - A certificate signing reqquest CSR
- The CA validates the request
  - Confirms DNS emails and website ownership+
- CA digitally signs the cert
  - Returns to the applicant

## Private Certificate Authorities
- YOu are your own CA
  - Build it in-house
  - Your devices must trust the internal CA
- Needed for medium-to-large organizations
  - Many web servers and privacy requirements
- Implement as part of your overall computing strategy
  - Windows Certificate Services, OpenCA

## Self-Signed certificates
- INternal certificates dont need to be signed by a public CA
  - Your company is the only one going to use it
  - No need to purchase trust for devices that already trust your
- Build your own CA
  - Issue your own certificates signed by ytour own CA
- Install the CA certificate/trusted chain on all devices
  - They now trust any certificates signed by your internal CA
  - Works exactly like a certificate you purchased

## Wildcard certificates
- Subject ALternative Name SAN
   - Extension to an X.509 certificate
   - Lists additional identification information
   - Allows a certificate to support many different domains
 - Wildcard domain
   - Certificates are based on the name of the server
   - A wildcard domain will apply to all server names in a domain
  
## Key Revocation
- Certificate Revocation List CRL
  - Maintained by the CA
  - Can contain many revocations in a large file
- Many different reasons
  - Changes all the time
- Can be used in case of vulnerabilities, or trust revokation, for example

## OCSP stapling
- Online Certificate Status Protocol
  - Provides scalability for OCSP checks
- The CA is responsible for responding to all clients OCSP requests
  - This may not scale well
- The CA is responsible for responding to all client OCSP requests
  - This may not scale well
- Instead, have the certificate holder verify their own status
  - Status information is stored on the certificate holder´s server
- OCSP status is "stapled" into the SSL/TLS handhsake
  - Digitally signed by the CA
- Messages usually sent to an OCSP responder via  HTTP, being easier to support and more efficient
- Not all browsers/aps support OCSP
