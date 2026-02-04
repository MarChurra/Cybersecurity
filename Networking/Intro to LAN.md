## LAN Topologies
- Topology refers to the design or look of the network at hand.

### Types of Topologies:
  - Star Topology - Devices are individually connected via a central networking device such as a swsitch or hub. This topology is the most commonly found today, since it is reliable and scalability. It´s costly and all information sent to a device is sent via the central device to which it connects. It requires more caling and the purchase of dedicated networking equipment. It can fail if the central device is down.
  - Bus Topology - This type of connection relies upon a single connection, known as a backbone cable. Similiar to leafs on a tree branch. Since all the information flows via a single cable, it is prone to becoming slow and bottlenecked. Simpler and more cost-efficient. There is little redundancy in place in case of failures.
  - Ring Topology - Also known as token topology. Devices such as computers are connected directly to each other to form a loop, meaning that there is little caling required and less dependence on dedicated hardware such as within a star topology. It works by sending data across the loop until it reaches thea destined device, using other devices along the loop to forward data. A device will only send received data from another device in this topology if it does not have any to send itself. If the device happens to have data to send, it will its own data first before sending data from another device. It only has one direction for data to travel across this topology, it is fairly easy to troubleshoot. It is not an efficient way of data travelling however.

### Switch
  - These are dedicated devices within a network that are designed to aggregate multiple other devices, such as computer. These various devices plug into a switch port. They are usually found in larger networks such as businesses and schools, when there are many devices connected to the network. They can have 4,8,16,24,32,64 ports to be plugged.
  - They are more efficient that their lesser counterpart (hubs / repeaters). Switches keep track of what device is connected to which port. This way, when a packet is received, it sends the data to the intended target, instead of replicating that packet to every port like a hub.
  - Both Switches and Routers can be connected to one another. This increaswes the redundancy of a network by adding multiple paths for data to take. If one path goes down, another one can be used.
    
### Router
  - It connects networks and passes data between them. It does it by using routing.
  - Routing is the label given to the process of data travelling across networks. Routing involves creating a path between networks so that this data can be sucessfully delivered.
  - Routing is sueful when devices are connected by many paths.

## Primer on Subnetting
- Subnetting is the term given to splitting up a network into smaller, miniature networks within itself
- Network administrators use subnetting to categorise and assign specific parts of a network to reflect this
- Subnetting is achieved by splitting up the number of hosts that can fit within the network, represented by a number called a subnet mask.
- A subnet mask is also represented as a number of four bytes (32 bits), ranging from 0 to 255.
- Subnets use IP adresses in three different ways:
    - Identify the network address
    - Identify the host address
    - Identify the default gateway
- Network Address - Identifies the start of teh actual network and is used to identify a network´s existence. A device with an IP of 192.168.1.100 will be on the network identified by 192.168.1.0
- Host Address - AN IP address here is used to identify a device on the subnet. A device wil have the network address of 192.168.1.1
- Default Gateway - Is a special address assigned to a device on the network that is capable of sending information to another network. Any data that needs to go to a device in an external network, will be sent to this device. They can use any host address but usually use either the first or last host address in a network, such as .1 a .254
  
 
