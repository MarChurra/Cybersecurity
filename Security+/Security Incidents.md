- User clicks an email attachment and executes malware
  - Malware then communicates with external servers
- DDoS
  - botnet attack
- Confidential information is stolen
  - Thief wants money or it goes public
- User installs perr-to-peer software and allows external access to innternal servers

## NIST SP800-61
- National Institute of Standards and Technology
  - NIST Special Publication 800-61 Revision 2
  - Computer Security Incident
  - Handling GUide
- The Incident response lifecycle
  - Preparation
  - Detection and Analysis
  - Containment, Eradication, and REcovery
  - Post-Incident Activity

## Preparing for an incident
- Communication methods
  - Phones and contact information
- Incident handling hardware and software
  - Laptops, removable media, forensic software, digital cameras
- Incident analysis resources
  - Documentation, network diagrams, baselines, critical file hash values
- Incident mitigation software
  - Clean OS and application images

## The challenge of detection
- Many different detection sources
  - Different levels of detail, different levels of perception
- A large amount of "volume"
  - Attacks are incoming all the time
  - How do you identify the legimate threats
- Incidents are almost always complex
   Extensive knowledge needed

## Analysis
- An incident might occur in the future
  - This is your heads-up
- Web server log
  - Vulnerability scanner in use
- Exploit announcement
  - Monthly Microsoft patch release,ADobe PDF sfotware update
- Direct Threats
- An attack is underway
  - Or an exploit is successful
- Buffer overflow attempt
  - Identified by an IPS/IDS system
- Antivirus software identifies malware
- Hostbased monitor detects a configuration change
- Network traffic flows deviate from the norm

## Isolation and Containment
- Generally a bad idea to let things run their course
  - An incident can spread quickly
  - Its your fault at that point
- Sandboxes
  - An isolated operating system
  - Run malware and analyze the results
  - Clean out the standbow when done
- Isolation can sometimes be problematic
  - Malware or infections can monitor connectivity
  - When it is lost, everything could be deleted/encrypted/damaged

## Recovery after an incident
- Get things back to normal
  - Remove the bad, keep the good
- Eradicate the bug
  - Remove malware
  - Disable breached user accounts
  - Fix vulnerabilities
- Recover the system
  - REstore from backups
  - Rebuild from scratch
  - Replace compromised files
  - Tighten down the perimeter

## Lessons learned
- Learn and improve
  - No system is perfect
- Post-incident meeting
  - Invite everyone affected by the incident
- Dont wait too long
  - Memories fade
  - Some recommendations can be applied to the next event

## Answer the tough questions
- What happened, exactly?
  - Timestamp of events
- How did your incident plans work?
  - Did the process operate sucessfully
- What would you do differently next time?
  - Retrospective views provide context
- Which indicators would you watch next time?

## Training for an incident
- There is a limited on-the-job training when a security event occurs
- Train the team prior to an incident
  - Initial response
  - Investigation plans
  - Incident reporting
  - And so on...
- This can be a expensive endeavor
- 
