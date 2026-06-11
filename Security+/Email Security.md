## Email Security Challenges
- The protocols used to transfer emails include relatively few security checks
  - It is very easy to spoof an email
- Spoofing happens all the time
  - Check your spam folder
- The email looks as if it originated from james@professormesser.com
  - But did it? How can you tell?
- A reputable sender will configure email validation
  - Publicly available on the sender´s DNS server

## Mail Gateway
- The gatekeeper
  - Evaluates the source of inbound email messages
  - Blocks it at the gateway before it reaches the user
  - On-site or cloud-based

## Sender Policy Framework SPF
- SPF protocol
  - Sender configures a list of all serfvers authorized to send emails for a domain
- List of authorized mail servers are added to a DNS txt record
  - Receivingh mail servers perform a check to see if incoming mail really did come from an authorized host

## Domain Keys Identified Mail DKIM
- A mail server digitally signs all outgoing mail
  - The public key is in the DKIM TXT record
- THe signature is validated by the receiving mail servers
  - Not usually seen by the user
 
## DMARC
- Domain-based Message Authentication, Reporting, and Conformance
  - An extension of SPF and DKIM
- The domain owner devices that receiving email servers should do with emails not validatingusing SPF and DKIM
  - That policy is written into a DNS TXT records
  - Accept all, sned to spam, or reject the mail
- Compliance reports are sent to the email administrator
