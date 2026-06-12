## Authorization
- The process of ensuring only authorized rights are exercised
- Policy enforcement
- The process of determining rights
- Policy Definition
- Users receive rights based on Access Control Models
  - Different business needs or mission requirements

## Least Privilege
- Rights and permissions should be set to the bare minimum
  - You only get exactly what is needed to complete your objective
- All user accounts must be limited
  - Applications should run with minimal privileges
- DOnt allow users to run with administrative privileges

## Mandatory Access Control MAC
- The operating system limits the operation of an object
  - Based on security clearance levels
- Every object gets a label
  - Confidential, secret, top secret, etc.
- Labeling of objects uses predefined rules
  - The administrator decides who gets access to what security level
  - Users cannot change these settings

 ## Discretionary Access Control DAC
 - Used in most OS
   - A familiar access control model
 - You create a document
   - As the owner, you control who has access
   - You can moodify access at any time
 - Very flexible access control
   - And very weak security
  
## Role-based Access control RBAC
- You have a role in your organization
  - Manager, director, team lead, project manager
- Administrators provide access based on the role of the user
  - Rights are gained implicitly instead of explicitly
- In Windows, use Groups to provide role-based access control
  - You are in shipping and receiving, so you can use the shipping software
- You are the manager, so you can review shipping logs

## Rule-based access control
- Generic term for following rules
  - Conditions other than who you area
- Access is detemined through system-enforced rules
  - System Administrators, not users
- The rule is associated with the object
  - System checks the ACLs for that object
- Rule examples:
  - Lab network access available between 9AM to 5PM
  - Only Chrome Browsers may complete this web form.

## Attribute-based access control (ABAC)
- Users can have complex relationships to applications and data
  - Access may be based on many different criteria
- ABAC can consider many parameters
  - A "next generation"authorization model
  - Aware of context
- Combine and evaluate multiple parameters
  - Resource information, IP Address, time of day, desired action, relationship to the data, etc.

## Time-of-day restrictions
- Almost all security devices include a time-of-day option
  - Restrict access during certain times or days of the week
  - Usually not the only access control
- Can be difficult to implement
  - Especially in a 24-hour environment
- Time-of-day restrictions
  - Training room network is inacessible between midnight and 6AM
  - Conference room access is limited after 8PM
  - R&D databases are only after between 8AM and 6PM.
