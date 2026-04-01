## TLS
- he first step for every server (or client) that needs to identify itself is to get a signed TLS certificate.
- Generally, the server administrator creates a Certificate Signing Request (CSR) and submits it to a Certificate Authority CA
- The CA verifies the CSR and issues a digital certificate
- Once the signed certificate is received, it can be used to identify the server, or client, to others, who can confirm the validity of the siognature.
- For a host to confirm the validity of a signed certificate, the certificates of the signing authorities need to be installed on the host.
- Generally speaking, getting a certificate signed requires paying an annual fee. However, Let’s Encrypt (opens in new tab) allows you to get your certificate signed for free.
- Finally, we should mention that some users opt to create a self-signed certificate. A self-signed certificate cannot prove the server’s authenticity as no third party has confirmed it.

## HTTPS
- HTTPS stands for Hypertext Transfer Protocol Secure. It is basically HTTP over TLS. Consequently, requesting a page over HTTPS will require the following three steps (after resolving the domain name):
  1. Establish a three-way handshake with the target server
  2. Establish a TLS session
  3. Communicate using the HTTP protocol.
 
## Getting the Encryption Key
- Adding to leads to all the packets being encrypted. We can no longer see the contents of the exchanged packets unless we get access to the private key.
