## Virtualization Security
- Quite different than non-virtual machines
  - Can appear anywhere and quickly
  - Quantity of resource vary between VMs
    - CPU, memory, storage
- Many similarities to physical machines
  - Complexity adds opportunity for the attackers
- Virtualization Vulnerabilities
  - Local privilege escalations
  - Command Injection
  - Information disclosure

## VM Escape Protection
- The virtual machine is self-contained
  - Virtual machine escape
  - Break out of the VM and interact with the host OS or hardware
- Once you escape the VM, you have great control
  - COntrol the host and other guest VMs
- This would be a huge exploit

## Resource REuse
- The hypervisor maanges the relationship betwee the physical and virtual resources
  - Available rAM, stroage space, CPU availability, etc
- These resources can be resued between VMs
  - Hypervisor host with 4GB of RAM
  - supports three VMs with 2GB of RAM each
  - RAM is allocated and shared between VMs
- Data can inadvertently be shared between VMs
  - Time to update the memory management features
  - Security patches can mitigate the risk
