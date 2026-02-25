## Virtualization Overview
- Before, the rule was "One server = one application"
- In the early days, digital services were run on physical machines, and each had a single clear purpose, such as hosting a website or storing data.
- This added an High cost, low utilization since servers weren´t being used in full capacity, slow deplyoment and harder to scale.
- A virtualization layer, a **hypervisor** was introduced to act as a referee between virtual machines and allow each virtual computer to behave independently, like a physical computer.
- Each virtual computer, known as a Virtual Machine VM, ascts as an independent system with its own OS, apps and settings.

## Hypervisor 
- A special piece of software that:
  - Divides a phyiscal computer into multiple virtual ones
  - Gives each virtual machine its own share of CPU, memory and storage
  - Keeps everything isolated and safe
  - Manage the lifecycle of virtual machines

- Types of implementations:
  - Type 1 - Hypervisors run directly on the physical hardware, making them faster, efficient and ideal for servers and professional environments
  - Type 2- Hypervisors run within an existing operating system, making them easier to install and ideal for learning, testing or smaller setups.

## Virtual Machines
- A virtual computer with its own virtual CPU, RAM, storage nework and OS.
- You can deploy VMs using tools such as Oracle virtualBox and VMware Workstation. These act as a type 2 hypervisor.

## Containers
- A lightweight, isolated environment that runs a single application and all the necessary components to support it.
- It borrows the core of the existing system by running on the kernel, which is the part that communicates with the hardware and manages resources such as memory and running programs.
- It does not bring its own operating system
- They package the application and its dependencies, such as libraries, tools and versions.
- They share the hosts operating system, so they start almost instantly
- They remain isolated from each other, so a misbehaving container does not affect the others.
- They can run consistently on any machine, making them perfect for development, testing and scalable deployments.
- It can be deployed with software such as Docker.

## Managing Virtual Machines 
