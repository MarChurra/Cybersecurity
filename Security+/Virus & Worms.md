## Virus
- Malware that can reproduce itself
  - It needs you to execute a program
- reproduces through file systems or the network
  - Just running a program can spread a virus
- May or may not cause problems
  - Some viruses are invisible
- Anti-virus is very common
  - Thousands of new viruses every week
  - Is your signature file updated

## Virus Types
- Program Viruses
  - Part of the application
- Boot Sector Viruses
- Script Viruses
  - Opearting System and browser-based
- Macro Viruses
  - Common in Office Apps
 
## Fileless Virus
- A stealth attack
  - Does a good job of avoiding anti-virus detection
- Operates in memory
  - But never installed in a file or application
- User clicks onm a malicious website link, Website exploits a Flash/Java/Windows vulnerability
- Launches a PowerShell and downloads payload in RAM
- Runs PowerShell scripts and executables in memory, exfiltrates data, damages files
- Adds an auto-start to REgistry

## Worms
- Malware that self-replicates
  - Does not need you to do anything
  - Uses the network as a transmission medium
  - Self-propagates and spreads quickly
- Worms are pretty bad
  - Can take over many systems very quickly
- Firewalls and IDS/IPS can mitigate many worm infestations
  - Does not help much once the worm gets inside
