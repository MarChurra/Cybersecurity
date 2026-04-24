### Physical Access Controls
- Barriers deployed to prevent direct physical contact wih systems.
- The goal is to prevent unauthorized users from gaining physical access to facilities, equipment and other organizational assets.
- For example, physical access control determines who can enter (or exit), where they can enter (or exit) and when they can enter (or exit).
- Some are:
  - Guards
  - Fences
  - Motion detectors
  - Laptop locks
  - Locked doors
  - Swipe cards
  - Guard dogs
  - Video cameras to monitor
  - Mantrap-style entry systems to stagger the flow of people
  - Alarms
 
### Logical Access Controls
- Logical access controls are the hardware and software solutions used to manage access to resources and systems. These technology-based solutions include tools and protocols that computer systems use for identification, authentication, authorization and accountability.
- Some Logic Access Control examples include:
  - Encryption is the process of taking plaintext and creating ciphertext.
  - Smart cards have an embedded microchip
  - Biometric are user´s physical characteristics
  - ACLs Access Control Lists define the type of traffic allowed on a network
  - Protocol are set of rules that govern the exchange of data between devices
  - Passwords are protected strings of characters.
  - Firewalls prevent unwanted network traffic.
  - Routers connect at least two networks.
  - Intrusion detection systems monitor a network for suspicious activities.
  - Clipping levels are certain allowed thresholds for errors before triggering a red flag.

 ### Administrative Access Controls
- Administrative access controls are the policies and procedures defined by organizations to implement and enforce all aspects of controlling unauthorized access.
- Administrative controls focus on personnel and business practices.
- Policies are statements of intent
- Procedures are the detailed steps required to perform an activity
- Hiring practices define the steps an organization takes to find qualified employees
- Background checks are a type of employee screening
- Data classification categorizes data based on its sensitivity
- Security training educates employees
- Reviews evaluate an employee´s job performance

### Administrative Access Controls in Detail
- The concept of administrative access controls involves three security services: authentication, authorization and accounting (AAA).
- These services provide the primary framework to control access, preventing unauthorized access to a computer, network, database or other data resourc
- Authentication: Verifies the identity of each user, with a password, token, or fingerprint.
- Authorization: Authorization services determine which resources users can access, along with the operations that users can perform. This can be accomplished via ACL
- Accounting: keeps track of what users do — including what they access, the amount of time they access resources, and any changes they make.

### Federated Identity Management
- Federated identity management refers to multiple enterprises that let their users use the same identification credentials to gain access to the networks of all enterprises in the group.
- Unfortunately, this broadens the scope and increases the probability of a cascading effect should an attack occur.
- Generally speaking, a federated identity links a subject’s electronic identity across separate identity management systems, such as being able to access several websites using the same social login credentials.
- It is imperative that organizations scrutinize the identifying information shared with partners, even within the same corporate group.

### MFA
- multi-factor authentication uses at least two methods of verification — such as a password and something you have, for example, a security key fob. This can be taken a step further by adding something you are, such as a fingerprint scan

## Access Control Concepts

### Zero Trust Security
- Zero trust is a comprehensive approach to securing all access across networks, applications, and environments. This approach helps secure access from users, end-user devices, APIs, IoT, microservices, containers, and more. It protects an organization’s workforce, workloads, and the workplace. The principle of a zero trust approach is, “never trust, always verify.” Assume zero trust any time someone or something requests access to assets. A zero trust security framework helps to prevent unauthorized access, contain breaches, and reduce the risk of an attacker's lateral movement through a network.
- Traditionally, the network perimeter, or edge, was the boundary between inside and outside, or trusted and untrusted.
- In a Zero trust approach, any place at which an access control decision is required should be considered a perimeter.
- This means that although a user or other entity may have successfully passed access control previously, they are not trusted to access another area or resource until they are authenticated. In some cases, users may be required to authenticate multiple times and in different ways, to gain access to different layers of the network.
- Zero trust for the Workforce: This pillar consists of people (e.g., employees, contractors, partners, and vendors) who access work applications by using their personal or corporate-managed devices. This pillar ensures only the right users and secure devices can access applications, regardless of location.
- Zero trust for Workloads: This pillar is concerned with applications that are running in the cloud, in data centers, and other virtualized environments that interact with one another. It focuses on secure access when an API, a microservice, or a container is accessing a database within an application.
- Zero trust for the workplace: This pillar focuses on secure access for any and all devices, including on the internet of things (IoT), that connect to enterprise networks, such as user endpoints, physical and virtual servers, printers, cameras, HVAC systems, kiosks, infusion pumps, industrial control systems, and more.

### Access Control Modes
- An organization must implement proper access controls to protect its network resources, information system resources, and information.
- A security analyst should understand the different basic access control models to have a better understanding of how attackers can break the access controls.
  - Discretionary Access Control DAC: This is the least restrictive model, and allows users to control access to their data as owners. It may use ACLs or other methods to specify which users or group of users have access to the information.
  - Mandatory Access Control MAC: Applies the strictest access control and is typically used in military or mission crticial applications. it assigns security level labels to information and enables users with access based on their security level clearance.
  - Role Based Access Control RBAC: Access decisions are based on an individual's roles and responsibilites within the organization. Individuals are assigned to the RBAC profile for the role.
  - Attribute/based access control ABAC: ABAC allows access based on attributes of the object (resource) to be accessed. The subjet, the user accessing the resource, and environmental factors regarding how the object is to be acessed, such as time of day.
  - Rule/based access control RBAC: Network security staff specify sets of rules regarding on conditions that are associated with access to data or systems. These rules may specify permitted or denied IP addresses, or certain protocols.
  - Time-based access control: TAC allows access to network resources based on the time of the day.
- Another access control model is the principle of least privilege, which specifies a limited, as-needed approach to granting user and process access rights to specific information and tools. The principle of least privilege states that users should be granted the minimum amount of access required to perform their work function.
- A common exploit is known as privilege escalation. In this exploit, vulnerabilities in servers or access control systems are exploited to grant an unauthorized user, or software process, higher levels of privilege than they should have. After the privilege is granted, the threat actor can access sensitive information or take control of a system.

### Network Access Control NAC Systems
- Network access control (NAC) systems support access management by enforcing organizational policies regarding the people and devices that are attempting to access the network. NAC systems allow cybersecurity professionals to monitor the users and devices that are attached to the network, and manually control access as required.
- Network access control systems provide the following capabilities>
  - Rapidly enforcing access policies that have been created for different operational conditions;
  - Recognizing and profiling connected users and devices to prevent malicious software on non-compliant systems from causing damage;
  - Providing secure access to network guests, often through registration portals;
  - Evaluating device compliance with security policies by user type, device type, and operating system prior to permitting network access.
  - Mitigating security incidents by blocking, isolating, or repairing non-compliant devices.
- Because BYOD and IoT networking greatly expand the network attack surface, NAC system automation features make focused control of network access by such devices practical. The NAC system is configured to enforce organizational policies. The relevant policies are enacted to permit or deny network access according to a wide range of factors that the NAC system detects on the devices that are attempting access. Without NAC systems it would be impossible for cybersecurity personnel to evaluate the thousands of devices that could attempt to access the network.

## Account Management

### Account Types
- An organization should not share accounts for privileged users, administrators or applications. The administrator account should only be used to administer a system. If a user accesses a malware-infected website or opens a malicious email while using the administrator account, this would put the organization at risk.
- This is because default accounts such as the guest or administrator account can be a security risk in older systems as attackers are familiar with the default settings used. To improve security, always replace any default accounts and make sure that all account types require a password.
  - On hiring a new employee, create an identity profile, register the employee's computer and mobile devices, and enable access to the organization's network. As the Identity Provider IdP, the organization is responsible fro authenticating their identity.
  - Disable or deactivate any accounts that are no longer needed and retrieve any organizational data of applications from the user's devices.
  - Grant a user no more access than is necessary to perform tasks.
  - Review user access to identy any access control adjustments that need to be made.
  - Use time of day restrictions to control when a user can log in.
  - Use location restrictions to control where or user can log in from.
    - Geofencing triggers an actions when a user enters or exists a boundary
    - Geolocation identifies a device based on its location
    - Geotagging adds an identifier to something based on the location
   
### Privileged Accounts
- Organizations should adopt robust practices for securing privileged accounts.
  - Identify and reduce the number of privileged accounts.
  - Enforce the principle of least privilege.
  - Revoke access rights when employees leave or change jobs
  - Eliminate shared accounts with passwords that do not expire.
  - Secure password storage.
  - Eliminate shared credentials for multiple admins
  - Record privileged sessions.
  - Implement a process to change embedded passwords for scripts and service accounts.
  - Log all user activity
  - Generate alerts for unusual behavior
  - Disable inactive privileged accouints
  - Use MFA for all administrative access
  - Implement a gateway between the end user and sensitive assets to limit network exposure to malware.
 
### File Access Control
- Permissions are rules configured to limit folder or file access for an individual or a group. Users should be limited to only the resources they need on a computer system or network. For example, they should not be able to access all files on a server if they only need access to a single folder. It may be easier to provide access to the entire drive, but it is more secure to limit access to only the folder they need. This is the principle of least privilege and closely connected to the concept of ‘need to know’ access. Limiting access to resources also prevents cybercriminals from accessing those resources if the user’s computer becomes infected.
  - Full Control
  - Modify (Users can change and delete existing files and folders but cannot create new ones)
  - Read and Execute
  - Write
  - Read
 
### Authentication Management
- Authentication and authorization issues include unencrypted credentials, incorrect permissions and access violations. But how do you keep cybercriminals out while still making it easy for authorized users to log in? Authentication management aims to ensure secure sign in while still providing ease of use.
  - Single Sign on SSO
  - OAuth: A standard that enables a user's account information to be used by third-party services.
  - A password vault
  - Knowledge-Based Authentication: providesd a password reset for users, based on personal information.
 
### Hash-Based Message Authentication Code
- Uses an encryption key with a hash function to authenticate a web server.
- Many web services use basic authentication, which does not encrypt the username and password during transmission.
- Using HMAC, the user sends a private key identifier and an HMAC.
- The server looks up the user's private key and creates an HMAC.
- The user;s HMAC must match the one calculated by the server.
- VPNs using IPsec rely on HHMAC functions to authenticate the origin of every packet and provide data integrity checking.

### AAA Operation
- A network must be designed to control who is allowed to connect to it and what they are allowed to do when they are connected. These design requirements are identified in the network security policy.
- The policy specifies how network administrators, corporate users, remote users, business partners, and clients access network resources. The network security policy can also mandate the implementation of an accounting system that tracks who logged in and when and what they did while logged in. Some compliance regulations may specify that access must be logged and the logs retained for a set period of time.
- The Authentication, Authorization, and Accounting (AAA) protocol provides the necessary framework to enable scalable access security.
- It can be a Local (router) or a Server-Based  (Centralized AAA) AAA Authentication.
- Devices communicate witht he centralized AAA server using either the RADIUS or TACACS+ Protocols
- 
