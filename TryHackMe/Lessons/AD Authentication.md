- All credentials are stored in the Domain Controllers.
- Whenever a user tries to authenticate to a service using domain credentials, the service will need to ask the Domain Controller to verify if they are correct. Two protocols can be used for network authentication in windows domains:
  
- Kerberos: Used by any recent version of Windows. This is the default protocol in any recent domain.
- NetNTLM: Legacy authentication protocol kept for compatibility purposes.

- While NetNTLM should be considered obsolete, most networks will have both protocols enabled.

## Kerberos
- Users who log into a service using will be assigned tickets.
- Think of tickets as proof of a previous authentication. Users with tickets can present them to a service to demonstrate they have already authenticated into the network before and are therefore enabled to use it.
- The process is:
  1. The user sends their username and a timestamp encrypted using a key derived from their password to the Key Distribution Center (KDC), a service usually installed on the Domain Controller in charge of creating Kerberos tickets on the network.
  2. The KDC will create and send back a Ticket Granting Ticket (), which will allow the user to request additional tickets to access specific services. The need for a ticket to get more tickets may sound a bit weird, but it allows users to request service tickets without passing their credentials every time they want to connect to a service.  Along with the , a Session Key is given to the user, which they will need to generate the following requests.
  3.  The TGT  is encrypted using the krbtgt account's password hash, and therefore the user can't access its contents. It is essential to know that the encrypted includes a copy of the Session Key as part of its contents, and the KDC has no need to store the Session Key as it can recover a copy by decrypting the if needed.
  4.  When a user wants to connect to a service on the network like a share, website or database, they will use their TGT to ask the KDC for a Ticket Granting Service **TGS**. These are tickets that allow connection only to the specific service they were created for. To request a TGS, the user will send their username and a timestamp encrypted using the Session Key, along with the TGT and a Service Principal Name, which indicates the service and the server name we inteded to access.
  5.  As a result, the KDC will send us a TGS along with a Service Session Key, which we will need to authenticate to the service we want to access. The TGS is encrypted using a key derived from the Service Owner Hash. The Service Owner is the user or machine account that the service runs under.
 
  6.  ## NetNTLM Authentication
  7.  - NetNTLM works using a challenge-response mechanism.
      1. The client sends an authentication request to the server they want to access.
      2. The server generates a random number and sends it as a challenge to the client.
      3. The client combines their password hash with the challenge (and other known data) to generate a response to the challenge and sends it back to the server for verification.
      4. The server forwards the challenge and the response to the Domain Controller for verification.
      5. The domain controller uses the challenge to recalculate the response and compares it to the original response sent by the client. If they both match, the client is authenticated; otherwise, access is denied. The authentication result is sent back to the server.
      6. The server forwards the authentication result to the client.
      - Note that the user's password (or hash) is never transmitted through the network for security.

      ## Trees
      - Luckily for us, Active Directory supports integrating multiple domains so that you can partition your network into units that can be managed independently. If you have two domains that share the same namespace (thm.local in our example), those domains can be joined into a Tree.
      - If our thm.local domain was split into two subdomains for UK and US branches, you could build a tree with a root domain of thm.local and two subdomains called uk.thm.local and us.thm.local, each with its AD, computers and users
      - A new security group needs to be introduced when talking about trees and forests. The Enterprise Admins group will grant a user administrative privileges over all of an enterprise's domains
    
      - ### Forests
      - - The domains you manage can also be configured in different namespaces. Suppose your company continues growing and eventually acquires another company called MHT Inc. When both companies merge, you will probably have different domain trees for each company, each managed by its own IT department. The union of several trees with different namespaces into the same network is known as a forest.
       
        - ### Trust Relationships
        - - In simple terms, having a trust relationship between domains allows you to authorise a user from domain THM UK to access resources from domain MHT EU.
          - The simplest trust relationship that can be established is a one-way trust relationship. In a one-way trust, if Domain AAA trusts Domain BBB, this means that a user on BBB can be authorised to access resources on AAA.
          - Two-way trust relationships can also be made to allow both domains to mutually authorise users from the other. By default, joining several domains under a tree or a forest will form a two-way trust relationship.
          - It is important to note that having a trust relationship between domains doesn't automatically grant access to all resources on other domains
          -  Once a trust relationship is established, you have the chance to authorise users across different domains, but it's up to you what is actually authorised or not.
