# Network Configuration For Hotel Management

Establish a reliable and segmented network across three floors, providing secure and efficient communication for each department, with dedicated VLANs to enhance security and manage network traffic.

---

## Table of content

1. [Question Scenerio](#Question-Scenerio)
2. [Network Diagram](#Network-Diagram)
3. [Conclusion](#Conclusion)

---

## Question Scenerio

As a part of your end year networking project, you are required to design and implement Vic
Modern Hotel network. The hotel has three floors; in the first floor there three departments
(Reception, store and Logistics), in the second floor there are three departments (Finance, HR
and Sales/Marketing), while the third floor hosts the IT and Admin. Therefore, the following
are part of the considerations during the design and implementation.
1. There should be three routers connecting each floor.
2. All routers should be connected to each other using serial DCE cable.
3. The network between the routers should be 10.10.10.0/30,10.10.10.4/30,10.10.10.8/30
4. Each floor is expected to have one switch (placed in the respective floor).
5. Each floor is expected to have WIFI networks connected to laptops and phones.
6. Each department is expected to have a printer.
7. Each department is expected to be in different VLAN.
8. Use OSPF as the routing protocol to advertise routes.
9. All devices are expected to obtain IP address dynamically with them
respective router configured as the DHCP server.
10. All the devices in the network are expected to communicate with each other.
11. Configure SSH in all the routers for remote login.
12. In IT department, add PC called Test-PC to port fa0/1 and use it to test remote login.
13. Configure port security to IT-dept switch to allow only Test-PC to access port fa0/1
(use sticky method to obtain mac-address with violation mode of shutdown.)

#### 1st Floor
  1. Reception- VLAN 80, Network of 192.168.8.0/24
  2. Store- VLAN 70, Network of 192.168.7.0/24
  3. Logistics- VLAN 60, Network of 192.168.6.0/24
  
#### 2nd Floor
  1. Finance- VLAN 50, Network of 192.168.5.0/24
  2. HR-VLAN 40, Network of 192.168.4.0/24
  3. Sales- VLAN 30, Network of 192.168.3.0/24
  
#### 3rd Floor
  1. Admin- VLAN 20, Network of 192.168.2.0/24
  2. IT-VLAN 10, Network of 192.168.1.0/24

---

## Network Diagram

![](https://github.com/hussainahmad402/Networking-Projects/blob/main/Pictures/Hotel%20Management%20Network.PNG)

---
## Conclusion

This project implements a robust network infrastructure for Vic Modern Hotel across three floors, each with distinct departments and VLANs. Key configurations include:

#### Routers: Three routers connect each floor with OSPF routing and serial DCE links for inter-router communication.
VLAN Segmentation: Each department is assigned a unique VLAN for secure data flow, aligning with hotel department needs.
#### DHCP Setup: Dynamic IP allocation per floor, with routers as DHCP servers.
Wireless Access: Wi-Fi connectivity for laptops and smartphones on each floor.
#### Remote Access & Security: SSH configured for router management and port security in the IT department, allowing only authorized devices.
This design ensures isolated departmental networks with full connectivity and secure remote access.



