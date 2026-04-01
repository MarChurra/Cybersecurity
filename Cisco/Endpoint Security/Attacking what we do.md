## IP Services

### ARP Vulnerabilities
- Hosts broadcast an ARP Request to other hosts on the network segment to determine the MAC address of a host with a particular IP address. All hosts on the subnet receive and process the ARP Request. The host with the matching IP address in the ARP Request sends an ARP Reply.
- Any client can send an unsolicited ARP Reply called a “gratuitous ARP.” This is often done when a device first boots up to inform all other devices on the local network of the new device’s MAC address. When a host sends a gratuitous ARP, other hosts on the subnet store the MAC address and IP address contained in the gratuitous ARP in their ARP tables.
- However, this feature of ARP also means that any host can claim to be the owner of any IP/MAC they choose. A threat actor can poison the ARP cache of devices on the local network, creating an MiTM attack to redirect traffic.
- The goal is to associate the threat actor’s MAC address with the IP address of the default gateway in the ARP caches of hosts on the LAN segment. This positions the threat actor in between the victim and all other systems outside of the local subnet.

### DNS Attacks
- DNS Open Resolver attacks: Many organizations use the services of publicly open DNS servers such as GoogleDNS (8.8.8.8) to provide responses to queries. This type of DNS server is called an open resolver. A DNS open resolver answers queries from clients outside of its administrative domain.  They are vulnerable to DNS cache poisoning attacks, DNS amplication and relfection attacks, and DNS resource utilization attacks.
- DNS stealth attacks:
  - Fast Flux: Threat actors use this technique to hide their phishing and malware delivery sites behind a quickly-changing network of compromised DNS hosts. The DNS IP addresses are continuously changed within minutes. Botnets often employ Fast Flux techniques to effectively hide malicious servers from being detected.
  - Double IP Flux: Threat actors use this technique to rapidly change the hostname to IP address mappings and to also change the authoritative name server. This increases the difficulty of identifying the source of the attack.
  - Domain GEneration Algorithms: Threat actors use this technique in malware to randomly generate domain names that can then be used as rendezvous points to their command and control (C&C) servers.
- DNS domain shadowing attacks
- DNS tunneling attacks
- DNS Domain Shadowing Attacks: Domain shadowing involves the threat actor gathering domain account credentials in order to silently create multiple sub-domains to be used during the attacks. These subdomains typically point to malicious servers without alerting the actual owner of the parent domain.

### DNS tunneling
- Botnets have become a popular attack method of threat actors. Most often, botnets are used to spread malware or launch DDoS and phishing attacks.
- DNS in the enterprise is sometimes overlooked as a protocol which can be used by botnets. Because of this, when DNS traffic is determined to be part of an incident, the attack is often already over. It is necessary for the cybersecurity analyst to be able to detect when an attacker is using DNS tunneling to steal data, and prevent and contain the attack.
- To accomplish this, the security analyst must implement a solution that can block the outbound communications from the infected hosts.
- Threat actors who use DNS tunneling place non-DNS traffic within DNS traffic. This method often circumvents security solutions. For the threat actor to use DNS tunneling, the different types of DNS records such as TXT, MX, SRV, NULL, A, or CNAME are altered. For example, a TXT record can store the commands that are sent to the infected host bots as DNS replies. A DNS tunneling attack using TXT works like this:
  a.  The data is split into multiple encoded chunks.
  b.  Each chunk is placed into a lower level domain name label of the DNS query.
  c.  Because there is no response from the local or networked DNS for the query, the request is sent to the ISP’s recursive DNS servers.
  d.  The recursive DNS service will forward the query to the attacker’s authoritative name server.
  e.  The process is repeated until all of the queries containing the chunks are sent.
  f.  When the attacker’s authoritative name server receives the DNS queries from the infected devices, it sends responses for each DNS query, which contains the encapsulated, encoded commands.
  g.  The malware on the compromised host recombines the chunks and executes the commands hidden within.

- To be able to stop DNS tunneling, a filter that inspects DNS traffic must be used. Pay particular attention to DNS queries that are longer than average, or those that have a suspicious domain name.
- Also, DNS security solutions, such as Cisco Umbrella (formerly Cisco OpenDNS), block much of the DNS tunneling traffic by identifying suspicious domains. Domains associated with Dynamic DNS services should be considered highly suspect.

### DHCP Attacks
- DHCP Spoofing Attack: A DHCP spoofing attack occurs when a rogue DHCP server is connected to the network and provides false IP configuration parameters to legitimate clients. A rogue server can provide a variety of misleading information:
  - Wrong default ageway -  Threat actor provides an invalid gateway, or the IP address of its host to create a MiTM attack. This may go entirely undetected as the intruder intercepts the data flow through the network.
  - Wrong DNS Server -  Threat actor provides an incorrect DNS server address pointing the user to a malicious website.
  - Wrong IP Address - Threat actor provides an invalid IP address, invalid default gateway IP address, or both. The threat actor then creates a DoS attack on the DHCP client.

## Enterprise Services

### HTTP and HTTPPs
- Some common web attacks are:
  a.  The victim unknowingly visits a web page that has been compromised by malware.
  b.  The compromised web page redirects the user, often through many compromised servers, to a site containing malicious code.
  c. The user visits this site with malicious code and their computer becomes infected. This is known as a drive by download. When the user visits the site, an exploit kit scans the software running on the victim’s computer including the OS, Java, or Flash player looking for an exploit in the software. The exploit kit is often a PHP script and provides the attacker with a management console to manage the attack.
  d.  After identifying a vulnerable software package running on the victim’s computer, the exploit kit contacts the exploit kit server to download code that can use the vulnerability to run malicious code on the victim’s computer.
  e.  After the victim’s computer has been compromised, it connects to the malware server and downloads a payload. This could be malware, or a file download service that downloads other malware.
  f.  The final malware package is run on the victim’s computer.
  
- Independent of the type of attack being used, the main goal of the threat actor is to ensure the victim’s web browser ends up on the threat actor’s web page, which then serves out the malicious exploit to the victim.
- Some malicious sites take advantage of vulnerable plugins or browser vulnerabilities to compromise the client’s system. Larger networks rely on IDSs to scan downloaded files for malware. If detected, the IDS issues alerts and records the event to log files for later analysis.
- Server connection logs can reveal information about the type of scan or attack:
  - Informational 1xx - his is a provisional response, consisting only of the Status-Line and optional headers. It is terminated by an empty line. There are no required headers for this class of status code. Servers MUST NOT send a 1xx response to an HTTP/1.0 client except under experimental conditions.
  - Sucessfull 2xx - The client’s request was successfully received, understood, and accepted.
  - Redirection 3xx - Further action must be taken by the user agent to fulfill the request. A client SHOULD detect infinite redirection loops, because these loops generate network traffic for each redirection.
  - Client Error 4xx - For cases in which the client seems to have erred. Except when responding to a HEAD request, the server SHOULD include an entity containing an explanation of the situation, and if it is temporary. User agents SHOULD display any included entity to the user.
  - Server Errro 5xx - For cases where the server is aware that it has erred, or it cannot perform the request. Except when responding to a HEAD request, the server SHOULD include an entity containing an explanation of the error situation, and if it is temporary. User agents SHOULD display any included entity to the user.
- To defend against web-based attacks, the following countermeasures shouild be used:
  - Always update the OS and browsers with current patches and updates.
  - Use a web proxy like Cisco Cloud Web Security or Cisco Web Security Appliance to block malicious sites.
  - Use the best security practices from the Open Web Application Security Project (OWASP) when developing web applications.
  - Educate end users by showing them how to avoid web-based attacks.

### Common HTTP Exploits
- Malicious iFrames: Threat actors often make use of malicious inline frames (iFrames). An iFrame is an HTML element that allows the browser to load another web page from another source. iFrame attacks have become very common, as they are often used to insert advertisements from other sources into the page. Threat actors compromise a webserver and modify web pages by adding HTML for the malicious iFrame. The HTML links to the threat actor’s webserver. In some instances, the iFrame page that is loaded consists of only a few pixels. This makes it very hard for the user to see. Because the iFrame is run in the page, it can be used to deliver a malicious exploit, such as spam advertising, an exploit kit, and other malware.
  - It is recommended to use a web proxy to block malicious sites. Because attackers often change the source HTML of the iFrame in a compromised web site, make sure web developers do not use iFrames. This will isolate any content from third-party web sites and make modified pages easier to find..
- HTTP 302 Cushioning: Another type of HTTP attack is the HTTP 302 cushioning attack. Threat actors use the 302 Found HTTP response status code to direct the user’s web browser to a new location. Threat actors often use legitimate HTTP functions such as HTTP redirects to carry out their attacks. HTTP allows servers to redirect a client’s HTTP request to a different server. HTTP redirection is used, for example, when web content has moved to a different URL or domain name. This allows old URLs and bookmarks to continue to function. Therefore, security analysts should understand how a function such as HTTP redirection works and how it can be used during attacks.
  - When the response from the server is a 302 Found status, it also provides the URL in the location field. The browser believes that the new location is the URL provided in the header. The browser is invited to request this new URL. This redirect function can be used multiple times until the browser finally lands on the page that contains the exploit. The redirects may be difficult to detect due to the fact that legitimate redirects frequently occur on the network.
  - Recommended to use a web proxy to block malicious sites.
- Domain Shadowing: When a threat actor wishes to create a domain shadowing attack, the threat actor must first compromise a domain. Then, the threat actor must create multiple subdomains of that domain to be used for the attacks. Hijacked domain registration logins are then used to create the many subdomains needed. After these subdomains have been created, attackers can use them as they wish, even if they are found out to be malicious domains. They can simply make more from the parent domain. The following sequence is typically used by threat actors.
  - Use a web proxy to block malicious sites. Secure all domain owner accounts with strong apsswords and 2FA.

### Email
- 
