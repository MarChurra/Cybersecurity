## DNS
- DOmain Name System provides a simple way for us to communicate with devices on the internet without remembering complex numbers.
- It maps the hostname and domain to an public IP address

## Domain Hierarchy
- **TLD Top level Domain**:
    - The most righthand part of a domain name. There are two types, **gTLD Generic Top Level** and **ccTLD Country Code Top Level Domain**
    - Historically, a gTLD was meant to tell the user the domain name´s purpose.
    - A ccTLD was used for geographical purposes
 
- **Second-Level Domain**:
    - The name of the domain itself

- **Subdomain**
    - Sites on the left hand side of the SLD using a period to separate it. It creates a logical separation inside the accessible contents of an domain
 
## DNS Record Types
  - Multiple types of DNS record exists, and the yare not meant only for websites. Some of the most common are:
      - A Record - Resolve to an IPv4 Address
      - AAAA Record - Resolove to an IPv6 address
      - CNAME Record - Resolve to another domain name.
      - MX Record - Resolve to the address of the servers that handle the email for the domain you are querying.  Come with a priority flag, to tell the client in which order to try the servers.
      - TXT Record - Free text fields where any text-based data cant be stored. They have several uses, but some common ones can be to list servers that have the authority to send an email o behalf of the domain, or verify ownership of the domain name when signing up for third party services.

## Flow of a DNS Request
  1. When you request a domain name, your computer first checks its local cache to see if you have preivoulsy looked up the address recently. If not,m a request to your Recursive DNS Server will be made.
  2. A Recursive DNS Server is usually provided by your ISP, but you can also choose your own. THis server has a local cache of recently looked up domain names. If a result is found locally, it sends back to your computer. If it cannot be found, a query is made, starting with the internet´s root DNS servers.
  3. The root servers act as the DNS backbone of the internet. it redirects you to the correct Top Level Domain Server, depending on the request.
  4. The TLD server holds records for where to find the authoritative server to answer the DNS request. The authoritative server is often also known as the nameserver for the domain.
  5. An auhthoritative DNS server is the one responsible for storing the DNS records for a particular domain name and where any updates to your domain name DNS records would be made. Depending on the record type, the DNS record is then sent back to the Recursive DNS Server, where it stores a local cache copy for future requests. DNS Records all come with a Time to Live value, represented in seconds, that says for how long it wil be cached.
