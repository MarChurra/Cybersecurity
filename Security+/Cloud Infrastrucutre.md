## Cloud responsability Matrix
- IaaS, PaaS, SaaS, etc.
  - Who is responsible for the security
- Security should be well documented
  - Most cloud providers, provide a matrix of responsibilities
- These responsibilities can vary
  - Different cloud providers
  - Contractual Agreements

## Hybrid considerations
- Hybrid cloud
  - More than one public or private cloud
  - This adds additional complexity
- Network protection mismatches
  - Authentication across platforms
  - Firewall configurations
  - Server settings
- Different security monitoring
  - Logs are diverse and cloud-specific
- Data leakage
  - Data is shared across the public Internet
 
## Third-party vendors in the cloud
- You, the cloud provider, and third parties 
  - Infrastructure technologies
  - Cloud-based appliances
- Ongoing vendor risk assessments
  - Part of an overall vendor risk management policy
- Include third-party impact for incident response
  - Everyone is part of the process
- Constant monitoring
  - Watch for changes and unusual activity
 
## Infrastructure as code
- Describe an infrastructure
  - Define servers, network, and applications as code
- Modify the infrastrucutre and create versions
  - The same way tou version app code
- Use the description (code) to build other app instances
  - Buuild it the same way, every time, based on the code
- An important concept for cloud computing
  - Build a perfect version every time

## Serverless architecture
- Function as a Service FaaS
  - Applications are separated into individual, autonomous functions
  - Remove the OS from the equiation
- Developer still creates the server-side logic
  - Runs in a stateless computer container
- May be event triggered and ephemeral
  - May only run for one event
- Managed by a third-party
  - All OS security concerns are at the 3rd party

## MicroServices and APIs
- Monolithic apps
  - One big application that does everything
  - Application contains all decision making processes
    - User interface
    - Business logic
    - Data input and output
  - Code challenges
    - Large codebase
    - Change control challenges
  - Taking advantage of Microservices via APIs
  - API is the "glue" for the microservices
    - Work teogether to act as the application
  - Scalable
    - Scale just the microservices you need
  - Resilient
    - Outages are contained
  - Security and compliance
    - Containment is built-in
