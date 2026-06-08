- The Security of an application environment should be well defined
  - All application instances must folow this baseline
  - Firewall settings, patch levels, OS file versions
  - May require constant updates
- Integrity measurements check for the secure baseline
  - These should be performed often
  - Checl against well-documented baselines
  - Failure requires an immediate correction
 
## Establish baselines
- Create a series of baselines
  - Foundational security policies
- Security baselines are often available from the manufacturer
  - APp developer
  - OS manufacturer
  - Appliance manufacturer
- Many OS have extensive options
  - There are over 3000 group policy settings in Windows 10, for example
 
## Deploy baselines
- We now have established detailed security baselines
  - How do we put those baselines into action
- Deploy the baselines
  - Usually managed through a centrally administered console
- May require multiple deployment mechanisms
  - ACtive Directory group policy, MDM, etc.
- Automation is the key

## Maintain baselines
- Many of these are best practices
  - They rarely change
- Other baselines may require ongoing updates
  - A new vulnerability is discovered
  - A updated app has been deployed
  - A new OS is installed
- Test and measure to avoid conflicts
  - Some baselines may contradict others
