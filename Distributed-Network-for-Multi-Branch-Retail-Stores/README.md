# Network Configuration For Hotel Management

Establish a reliable and segmented network across three floors, providing secure and efficient communication for each department, with dedicated VLANs to enhance security and manage network traffic.

---

## Table of content

1. [Question Scenerio](#Question-Scenerio)
2. [Network Diagram](#Network-Diagram)
3. [Conclusion](#Conclusion)

---

## Question Scenerio

The project involves designing a network to connect several retail branches located in different cities. Each branch will have its own local network for Point-of-Sale (POS) systems, employee computers, and inventory systems. All branches will connect to a central data center to store inventory, transaction data, and backups.
### Branch Locations:<br>
Assume we have the following branches in different cities:
1. New York (NYC) - Headquarters
2. Los Angeles (LA) - Branch 1
3. Chicago (CHI) - Branch 2
4. Houston (HOU) - Branch 3

### IP Addressing Plan:
We'll use private IP addressing with subnetting to assign different IP ranges to each branch and its respective local devices (POS, staff computers, etc.). A common practice is to use Class C subnets for each branch.
#### Central Data Center (HQ - New York)
1. IP Network: 10.10.10.0/28
2. Devices: DNS, DHCP, Database Servers, File Servers
#### Branch 1 (Los Angeles)
1. IP Network: 10.10.10.0/28
2. POS Devices: 192.168.1.0/24
3. Employee Computers: 192.168.2.0/24
4. Inventory System: 192.168.3.0/24

#### Branch 2 (Chicago)
1. IP Network: 10.10.10.0/28
2. POS Devices: 192.168.1.0/24
3. Employee Computers: 192.168.2.0/24
4. Inventory System: 192.168.3.0/24
#### Branch 3 (Houston)
1. IP Network: 10.10.10.0/28
2. POS Devices: 192.168.1.0/24
3. Employee Computers: 192.168.2.0/24
4. Inventory System: 192.168.3.0/24

### Network Design Overview:

#### Core Network (HQ - New York):
1. Centralized data center with servers for storing data and hosting backup services.
2. Routing: Use OSPF for internal routing between branches.
3. VPN: Secure communication between branches using site-to-site VPN tunnels (IPsec) or MPLS.
4. Redundancy: Use HSRP or VRRP for router redundancy at the central data center.
#### Branch Connectivity:
1. MPLS/VPN to connect remote branches to the data center.
2. Local Servers: Each branch has a local DHCP server for IP address assignment and DNS for local resolution.
3. POS Network: VLANs to segregate POS devices and inventory systems from employee networks.
#### Security:
1. ACLs to ensure that POS systems are only accessible from the employee VLAN and specific servers.
2. Use firewalls for securing the branches from external threats.

### Tasks Breakdown:

#### VLAN Configuration:
1. Configure VLANs for the following:
2. POS Systems
3. Employee Computers
4. Inventory Systems
#### Routing:
1. Use OSPF for internal routing.
2. Configure VPN tunnels between branches and the HQ.
#### DHCP Configuration:
1. Set up local DHCP servers at each branch to assign dynamic IPs to end devices.
#### Security Configuration:
1. Implement ACLs to restrict access to sensitive resources.
2. Set up firewalls at each branch's gateway.
#### Connectivity Testing:
1. Verify end-to-end connectivity between branches.
2. Ensure the central data center can be accessed securely.

### Suggested IP Address Layout:

| City/Branch     | Network Address    | Subnet Mask        | IP Range (Devices)                                  |
|-----------------|--------------------|--------------------|-----------------------------------------------------|
| New York (HQ)   | 10.10.10.0/28      | 255.255.255.240    | 192.168.1.0/24 (Servers)                           |
| Los Angeles     | 10.10.10.0/28      | 255.255.255.240    | 192.168.1.0 – 192.168.3.0 (POS, Staff, Inventory)  |
| Chicago         | 10.10.10.0/28      | 255.255.255.240    | 192.168.1.0 – 192.168.3.0 (POS, Staff, Inventory)  |
| Houston         | 10.10.10.0/28      | 255.255.255.240    | 192.168.1.0 – 192.168.3.0 (POS, Staff, Inventory)  |


### Next Steps:
1. Design the network topology in Cisco Packet Tracer, including routers, switches, and end devices (POS systems, employee PCs, etc.).
2. Configure VLANs, DHCP, routing (OSPF, VPN), and security features like ACLs and firewalls.
3. Test connectivity between all branches and the central data center.

---

## Network Diagram

---

## Conclusion
