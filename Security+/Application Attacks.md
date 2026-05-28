## Injection ATtacks
- Code Injection- Adding your own information into a data stream
  - Enabled because of bad programming- The application should proplerly handle input and output
- So many different injectable data types
  - HTML, SQL, XML, LDAP

## Buffer Overflows
- Overwriting a buffer of memory- Spills into other memory areas
- Developers need to perform bounds checking
  - The attacker spend a lot of time looking for openings
- Not a simple exploit
  - Takes  time to avoid crashing things
  - Takes time to make it od what you want
- A really usefull buffer overflow is repeatable

## Replay Attack
- Useful information is transmitted over the network
  - A crafy hacker will take advantage of this
- Need access to the raw network data
  - Network Tap, ARP poisoning, Malware o the victim compuiter
- The gathered informaiton may help the attacker
  - Replay the data to appear as someone else
- This is not an on-path atack
  - The actual replay does not require the original workstation
 
## Privilege Escalation
- Gain higher-level access to a system
  - Exploit a Vulnerability
  - Might be a bug or a design flaw
- Higher-level access means more capabilities
  - This is commonly  the highest level access
  - This is a concern
- These are hiogh-priority vulenrability patches
  - You want to get these closed very quiockly
- Horizontal Privilege Escalation
  - User A can access user B resources
- To mitigate, it is required to patch quickly
- Update anti-virusd and anti-malware software
- Data Execution Prevention
  - Only data in executable areas can run
- Address space layout randomization
  - Prevents a buffer overrun at a known memory address

## Cross-site Requests
- Cross-site requests are common and legitimate
  - You visit a Website
  - Your browser loads text from the web servers
  - Loads a video from Youtube
  - Loads pictures from Instagram
- HTML on a website directs requests from your browser
  - This is normal and expected
  - Most of these are unauthenticated requests

## The client and the server
- Website pages consist of client-side code and sedrver-side code
 - Many moving parts
- Client Side
  - Renders the page on the Screen
  - HTML, Javascript, CSS
- Server Side
  - Performs requests from the client
  - HTML, PHP
  - Handles the transaction or request

## Cross-site request forgery
- One-click attack, session riding
  - XSRF, CSRF (sea Surf)
- Takes advantage of the trust that a web app has for the user- The web site tursts your browser
- Requests are made without your consent or your knowledge
- Attacker postos a Facebook status on your account
- Significant web app development oversight
  - The application should have anti-forgery techniques added
  - usually a cryptographic token to prevent a forgery
 
## Directory Traversal
- Path traversal / Directory Traversal
  - Read files from a web server that are outisde of the websites file directory
- Users should not be able to browse the Windows Folder 
- Web Server software vulnerability
- Wont stop users from browsing past the web server root
- Web application code vulnerability
- Takes advantage of badly written code
   
