## Physical Isolation
- Devices are phsically separate
  - Air gap between a Swtich A and B
- Web servers in one rack
  - Database servers on another
- Customer A on one switch, customer B on another
  - No opportunity for mixing data

## Physical Segmentation
- Separate Devices
  - Multiple units, separate infrastructure

## Logical segmentation with VLANs
- VLANs Virtual Local Area Networks
  -Separated logically instead of physically
  - Cannot communicate between VLANs without a Layer 3 device / router

## SDN Software Defined Networking
- Networking devices have different functional planes of operationº
  - Data,control, and management planes
- Split the functions into separate logical units
  - Extend the functionality and management of a singel device
  - Perfectly built for the cloud
- Infrastructure Layer / Data Plane
  - Process the network frames and packets
  - Forwarding, trunking, encrypting, NAT
- Control Layer / Control Plane
  - Manages the actions of the data plane
  - Routing tables, session tables, NAT tables
  - Dynamic routing protocol updates
- Application Layer / Management plane
  - Configure and manage the device
  - SSH, browser API
