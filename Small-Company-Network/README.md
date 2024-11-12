# Network Configuration For Small Company

This network design is intended for a small company divided into three departments: Admin/IT, Finance/HR, and Customer/Reception. The network infrastructure consists of one router and one switch with different VLANs, ensuring efficient communication and resource sharing among the departments

---

## Table of Contents
1. [Question Scenario](#Question-Scenario)
2. [Network Diagram](#Network-Diagram)
3. [Configuration Details](#Configuration-Details)
4. [Conclusion](#Conclusion)

---

## Question Scenario

Being a small network, the company has the following requirements during implementation;
1. One router and one switch to be used (all CISCO products).
2. 3 departments (Admin/IT, Finance/HR and Customer service/Reception)
3. Each department is required to be in different VLANS.
4. Each department is required to have wireless network for the users.
5. Host devices in the network are required to obtain IPv4 address automatically.
6. Devices in all the departments are required to communicate with each other.
Assume the ISP gave out a base network of 192.168.1.0.

---

## Network Diagram

![](https://github.com/hussainahmad402/Networking-Projects/blob/main/Pictures/Small-Company-Network.PNG)

---

## Configuration Details
1. Switch
'''bash
Enable
Configuration terminal
Vlan 10
Name Admin
Int range fa0/1-5
Switchport mode access
Switchport access vlan 10
Vlan 20
Name Finance
Int range fa0/6-10
Switchport mode access
Switchport access vlan 20
Vlan 30
Name Reception
Int range fa0/11-15
Switchport mode access
Switchport access vlan 30
Int fa0/24
Switchport mode trunk
Do wr

2. Router
'''bash
Enable 
Configuration secret
Int gig0/0/0
No shutdown
Exit
Int gig0/0/0.10
Encapsulation dot1Q 10
Ip address 192.168.1.1 255.255.255.192
Exit
Int gig0/0/0.20
Encapsulation dot1Q 20
Ip address 192.168.1.65 255.255.255.192
Exit
Int gig0/0/0.20
Ip address 192.168.1.129 255.255.255.192
Exit
Service dhcp
Ip dhcp pool Admin-pool
Network 192.168.1.0 255.255.255.192
Default-router 192.168.1.1
Exit
Ip dhcp pool Fianace-pool
Network 192.168.1.64 255.255.255.192
Default-router 192.168.1.65
Exit
Ip dhcp pool Reception-pool
Network 192.168.1.128 255.255.255.192
Default-router 192.168.1.129
Exit
Do wr


---

## Conclusion


