## XSS
- Originally called cross-site because of browser security flaws
  - Information one site could be shared with another
- One of the most common web app vulnerabilities
  - Takes advantage of the trust a user has for a site
  - Complex and varied
- XSS commonly uses JavaScript

## Cross-site Scripting
1. Attacker sends a link containing a malicious script to a victim
2. Victim clicks link and visits legitimate site
3. Legitimate site loads in the victims browser. Malicious script is also executed
4. Malicious script sends victims data

## Non-Persisntent (reflected) XSS attack
- Website allows scripts to run in the user input
  - Search box is a common source
- Attacker emails a link that takes advantage of this vulenrability
  - Runs a script that sends credentials/session IDs/cookies to the attacker
- Script embedded in URL executes in the victim´s browser
  - As if it came from the server
- Attacker uses credentials/session IDs/cookies to steal victim´s informaiton without their knowledge

## Persistent (stored) XSS attack
- Attacker posts a message to a social network
  - Includes the malicious payload
- Its now persistent
  - Everyone gets the payload
- No specific target
- For social networking, this can spread quickly
- Everyone who views the message can have it posted to their page
- Where someone else can view it and propagate it further

## Protecting against XSS
- Be carefu when clicking untrusted links
- Never blindly click links
- Consider disabling JavaScript or control with an extension
- Keep your browser and apps updated
- Validate Input 
