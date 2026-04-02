## IP Services

### ARP Vulnerabilities
- Hosts broadcast an ARP Request to other hosts on the network segment to determine the MAC address of a host with a particular IP address. All hosts on the subnet receive and process the ARP Request. The host with the matching IP address in the ARP Request sends an ARP Reply.
- Any client can send an unsolicited ARP Reply called a “gratuitous ARP.” This is often done when a device first boots up to inform all other devices on the local network of the new device’s MAC address. When a host sends a gratuitous ARP, other hosts on the subnet store the MAC address and IP address contained in the gratuitous ARP in their ARP tables.
- However, this feature of ARP also means that any host can claim to be the owner of any IP/MAC they choose. A threat actor can poison the ARP cache of devices on the local network, creating an MiTM attack to redirect traffic.
- The goal is to associate the threat actor’s MAC address with the IP address of the default gateway in the ARP caches of hosts on the LAN segment. This positions the threat actor in between the victim and all other systems outside of the local subnet.

### DNS Attacks
- DNS Open Resolver attacks: Many organizations use the services of publicly open DNS servers such as GoogleDNS (8.8.8.8) to provide responses to queries. This type of DNS server is called an open resolver. A DNS open resolver answers queries from clients outside of its administrative domain.  They are vulnerable to DNS cache poisoning attacks, DNS amplication and reflection attacks, and DNS resource utilization attacks.
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
- Some types of attacks are:
  - Attachment-based attacks: Threat actors embed malicious content in business files such as an email from the IT department. Legitimate users open malicious content. Malware is used in broad attacks often targeting a specific business vertical to seem legitimate, enticing users working in that vertical to open attachments, or click embedded links.
  - Email spoofing: Threat actors create email messages with a forged sender address that is meant to fool the recipient into providing money or sensitive information. For example, a bank sends you an email asking you to update your credentials. When this email displays the identical bank logo as mail you have previously opened that was legitimate, it has a higher chance of being opened, having attachments opened and links clicked. The spoofed email may even ask you to verify your credentials so that the bank is assured that you are you, exposing your login information.
  - Spam email: Threat actors send unsolicited email containing advertisements or malicious files. This type of email is sent most often to solicit a response, telling the threat actor that the email is valid and a user has opened the spam.
  - open mail relay server: Threat actors take advantage of enterprise servers that are misconfigured as open mail relays to send large volumes of spam or malware to unsuspecting users. The open mail relay is an SMTP server that allows anybody on the internet to send mail. Because anyone can use the server, they are vulnerable to spammers and worms. Very large volumes of spam can be sent by using an open mail relay. It is important that corporate email servers are never set up as an open relay. This will considerably reduce the amount of unsolicited emails.
  - Homohlyps: Threat actors can use text characters that are very similar or even identical to legitimate text characters. For example, it can be difficult to distinguish between an O (upper case letter O) and a 0 (number zero) or a l (lower case “L”) and a 1 (number one). These can be used in phishing emails to make them look very convincing. In DNS, these characters are very different from the real thing. When the DNS record is searched, a completely different URL is found when the link with the homoglyph is used in the search.
- Just like any other service that is listening to a port for incoming connections, SMTP servers also may have vulnerabilities. Always keep SMTP software up to date with security and software patches and updates.

### Web-Exposed Databases
- Code Injection: Attackers are able to execute commands on a web server’s OS through a web application that is vulnerable. This might occur if the web application provides input fields to the attacker for entering malicious data. The attacker’s commands are executed through the web application and have the same permissions as the web application. This type of attack is used because often there is insufficient validation of input. An example is when a threat actor injects PHP code into an insecure input field on server page.
- SQL Injection: SQL is the language used to query a relational database. Threat actors use SQL injections to breach the relational database, create malicious SQL queries, and obtain sensitive data from the relational database.

### Client-side Scripting
- Cross Site Scripting: Not all attacks are initiated from the server side. Cross-Site Scripting (XSS) is where web pages that are executed on the client-side, within their own web browser, are injected with malicious scripts. These scripts can be used by Visual Basic, JavaScript, and others to access a computer, collect sensitive information, or deploy more attacks and spread malware. As with SQL injection, this is often due to the attacker posting content to a trusted website with a lack of input validation. Future visitors to the trusted web site will be exposed to the content provided by the attacker.
- They can be two types of XSS:
  - Stored (persistent): This is permanently stored on the infected server and is received by all visitors to the infected page.
  - Reflected (non-persistent): This only requires that the malicious script is located in a link and visitors must click the infected link to become infected.
- TO avoid them, its important for developers to be aware of them, an IPS implementation, a web p+roxy or services that block these threats.

## Mitigasting Common Network Attacks

### Defending the Network
- Constant vigilance and ongoing education are required to defend your network against attack. The following are best practices for securing a network:
  1. Develop a written security policy for the company.
  2. Educate employees about the risks of social engineering, and develop strategies to validate identities over the phone, via email, or in person.
  3. Control physical access to systems.
  4. Use strong passwords and change them often.
  5. Encrypt and password-protect sensitive data.
  6. Implement security hardware and software such as firewalls, intrusion prevention systems (IPS), virtual private network (VPN) devices, antivirus software, and content filtering.
  7. Perform backups and test the backed-up files on a regular basis.
  8. Shut down unnecessary services and ports.
  9. Keep patches up-to-date by installing them weekly or daily, if possible, to prevent buffer overflow and privilege escalation attacks.
  10. Perform security audits to test the network.

### Mitigating Malware
- Malware, including viruses, worms, and Trojan horses, can cause serious problems on networks and end devices. Network administrators have several means of mitigating these attacks.
- Note: Mitigation techniques are often referred to in the security community as “countermeasures”.
- One way of mitigating virus and Trojan horse attacks is antivirus software. Antivirus software helps prevent hosts from getting infected and spreading malicious code. It requires much more time to clean up infected computers than it does to maintain up-to-date antivirus software and antivirus definitions on the same machines.
- Antivirus products have update automation options so that new virus definitions and new software updates can be downloaded automatically or on demand. This practice is the most critical requirement for keeping a network free of viruses and should be formalized in a network security policy.
- Antivirus products are host-based. These products are installed on computers and servers to detect and eliminate viruses. However, they do not prevent viruses from entering the network, so a network security professional must be aware of the major viruses and keep track of security updates regarding emerging viruses.
- Another way to mitigate malware threats is to prevent malware files from entering the network at all. Security devices at the network perimeter can identify known malware files based on their indicators of compromise. The files can be removed from the incoming data stream before they can cause an incident
- Unfortunately, threat actors are aware of this countermeasure and frequently alter their malware enough that it evades detection. These exploits will enter the network and will also evade antivirus software. No mitigation technique can be 100% effective. Security incidents are going to happen.

### Mitigating Worms
- Worms are more network-based than viruses. Worm mitigation requires diligence and coordination on the part of network security professionals.
- A worm attack can be broken down into four phases: containment, inoculation, quarantine, and treatment.
  - Containement: The containment phase involves limiting the spread of a worm infection to areas of the network that are already affected. This requires compartmentalization and segmentation of the network to slow down or stop the worm and to prevent currently infected hosts from targeting and infecting other systems. Containment requires using both outgoing and incoming ACLs on routers and firewalls at control points within the network.
  - Inoculation: The inoculation phase runs parallel to or subsequent to the containment phase. During the inoculation phase, all uninfected systems are patched with the appropriate vendor patch. The inoculation process further deprives the worm of any available targets.
  - Quarantine: The quarantine phase involves tracking down and identifying infected machines within the contained areas and disconnecting, blocking, or removing them. This isolates these systems appropriately for the treatment phase.
  - Treatment: The treatment phase involves actively disinfecting infected systems. This can involve terminating the worm process, removing modified files or system settings that the worm introduced, and patching the vulnerability the worm used to exploit the system. Alternatively, in more severe cases, the system may need to be reinstalled to ensure that the worm and its by-products are removed.
 
### Mitigating Reconnaissance Attacks
- Reconnaissance attacks are typically the precursor to other attacks that have the intent of gaining unauthorized access to a network or disrupting network functionality.
- A network security professional can detect when a reconnaissance attack is underway by receiving notifications from preconfigured alarms
- These alarms are triggered when certain parameters are exceeded, such as the number of ICMP requests per second. A variety of technologies and devices can be used to monitor this type of activity and generate an alarm.
- They can be mitigated via:
  - Implementing authentication to ensure proper access.
  - Using encryption to render packet sniffer attacks useless.
  - Using anti-sniffer tools to detect packet sniffer attacks.
  - Implementing a switched infrastructure.
  - Using a firewall and IPS.
- Anti-sniffer software and hardware tools detect changes in the response time of hosts to determine whether the hosts are processing more traffic than their own traffic loads would indicate. While this does not completely eliminate the threat, as part of an overall mitigation system, it can reduce the number of instances of threat.
- Encryption is also effective for mitigating packet sniffer attacks. If traffic is encrypted, using a packet sniffer is of little use because captured data is not readable.
- It is impossible to mitigate port scanning but using an intrusion prevention system (IPS) and firewall can limit the information that can be discovered with a port scanner. Ping sweeps can be stopped if ICMP echo and echo-reply are turned off on edge routers; however, when these services are turned off, network diagnostic data is lost. Additionally, port scans can be run without full ping sweeps. The scans simply take longer because inactive IP addresses are also scanned.

### Mitigating Access Attacks
- Several techniques are available for mitigating access attacks. These include strong password security, principle of minimum trust, cryptography, and applying operating system and application patches.
- A surprising number of access attacks are carried out through simple password guessing or brute-force dictionary attacks against passwords. To defend against this, create and enforce a strong authentication policy which includes:
  - **Use strong passwords**
  - **Disable accounts after a specified number of unsucessful login has ocurred.**
- The network should also be designed using the principle of minimum trust. This means that systems should not use one another unnecessarily. For example, if an organization has a trusted server that is used by untrusted devices, such as web servers, the trusted server should not trust the untrusted devices unconditionally.
- Cryptography is a critical component of any modern secure network. Using encryption for remote access to a network is recommended. Routing protocol traffic should also be encrypted. The more that traffic is encrypted, the fewer opportunities hackers have for intercepting data with man-in-the-middle attacks.
- The use of encrypted or hashed authentication protocols, along with a strong password policy, greatly reduces the probability of successful access attacks.
- In general, access attacks can be detected by reviewing logs, bandwidth utilization, and process loads. The network security policy should specify that logs are formally maintained for all network devices and servers. By reviewing logs, network security personnel can determine if an unusual number of failed login attempts have occurred.

### Mitigating DoS Attacks
- One of the first signs of a DoS attack is a large number of user complaints about unavailable resources or unusually slow network performance
-  To minimize the number of attacks, a network utilization software package should be running at all times. Network behavior analysis can detect unusual patterns of usage that indicate that a DoS attack is occurring. A means of detecting unusual network behavior should be required by the organization’s network security policy
-  A network utilization graph showing unusual activity could also indicate a DoS attack.
-  DoS attacks could be a component of a larger offensive. DoS attacks can lead to problems in the network segments of the computers being attacked. For example, the packet-per-second capacity of a router between the internet and a LAN might be exceeded by an attack, compromising not only the target system but also the network devices that the traffic must pass through. If the attack is conducted on a sufficiently large scale, entire geographical regions of internet connectivity could be compromised.
-  Historically, many DoS attacks were sourced from spoofed addresses. Cisco routers and switches support a number of antispoofing technologies, such as port security, Dynamic Host Configuration Protocol (DHCP) snooping, IP Source Guard, Dynamic Address Resolution Protocol (DAI) Inspection, and access control lists (ACLs).
