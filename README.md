# Network Subnetting with VLSM, DHCP, OSPF Routing, and Access Control-Computer Networks 


## Description
This project uses VLSM for efficient IP allocation across three subnets with DHCP for dynamic IP assignment and OSPF for routing. A second network configuration restricts communication between a new PC in Network A and Network C using access control. Network address: 192.16.2.0.

### Network Requirements
- **Network A**: 62 hosts (plus 1 additional PC)
- **Network B**: 26 hosts
- **Network C**: 3 hosts
- **Network Address**: 192.16.2.0

### Steps Involved
1. **VLSM Calculation**: Calculate subnet masks and IP ranges for each subnet.
2. **DHCP Configuration**: Set up DHCP to assign IP addresses dynamically.
3. **OSPF Routing**: Configure OSPF routing to enable communication between subnets.
4. **Access Control**: Implement access control to restrict communication between the new PC in Network A and Network C.

### VLSM Calculation
1. **Network A**: Requires 62 hosts.
    - Subnet Mask: 255.255.255.192 (/26)
    - IP Range: 192.16.2.1 - 192.16.2.62
    - Network Address: 192.16.2.0
    - Broadcast Address: 192.16.2.63

2. **Network B**: Requires 26 hosts.
    - Subnet Mask: 255.255.255.224 (/27)
    - IP Range: 192.16.2.65 - 192.16.2.90
    - Network Address: 192.16.2.64
    - Broadcast Address: 192.16.2.95

3. **Network C**: Requires 3 hosts.
    - Subnet Mask: 255.255.255.248 (/29)
    - IP Range: 192.16.2.97 - 192.16.2.99
    - Network Address: 192.16.2.96
    - Broadcast Address: 192.16.2.103

### DHCP Configuration
1. Set up a DHCP server to allocate IP addresses dynamically within the calculated IP ranges for each subnet.
2. Ensure that the DHCP server is configured to assign the correct default gateway and DNS server information.

### OSPF Routing Configuration
1. Configure OSPF on each router to advertise the subnets.
2. Ensure that OSPF neighbors are correctly established and routes are propagated.

### Access Control Configuration
1. Add a new PC in Network A with an IP within the range of Network A.
2. Implement access control lists (ACLs) to restrict communication between the new PC in Network A and Network C.

### Implementation Details
- **VLSM Calculation**: Python script or manual calculation
- **DHCP Configuration**: Configuration files for the DHCP server
- **OSPF Routing**: Configuration files for routers
- **Access Control**: ACL configurations on routers

### Prerequisites
- Basic understanding of networking concepts.
- Access to network simulation tools (e.g., Cisco Packet Tracer, GNS3).
- Basic knowledge of DHCP, OSPF, and ACL configuration.

### Getting Started
1. Clone this repository:
    ```bash
    [git clone https://github.com/thelaibaasif/Network-Subnetting-with-VLSM-DHCP-OSPF-Routing-and-Access-Control/
    ```
2. Follow the steps in the `Implementation Details` section to set up the network.
3. Verify the network setup by testing IP allocation, routing between subnets, and access control.

### Author
Laiba Asif

### License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
