# Campus Area Network

## Table of content

1. [Question Scenerio](#Question-Scenerio)
2. [Network Diagram](#Network-Diagram)
3. [Conclusion](#Conclusion)

---

## Question Scenerio


Albien University is a large university which has two campuses situated 20 miles apart. The university's students and staff are distributed in 4 faculties. These include the faculties of Health and Sciences, Business, Engineering/Computing and Art/Design. Each member of staff has a PC and students have access to PCs in the labs.

### Requirements:<br>
Create a network topology with the main components to support the following: <br>
<h3>Main campus:</h3>
<b>Building A:</b><br> Administrative staff in the departments of management, HR and finance. The admin staff PCs are distributed in the building offices and it is expected that they will share some networking equipment (Hint: use of VLANs is expected here). The Faculty of Business is also situated in this building <br>
<b>Building B:</b><br> Faculty of Engineering and Computing and Faculty of Art and Design<br>
<b>Building C:</b><br> Students' labs and IT department. The IT department hosts the University Web server and other servers<br>
There is also an email server hosted externally on the cloud.<br>
<h3> Smaller campus: </h3>
Faculty of Health and Sciences (staff and students' labs are situated on separate floors)
<br>
You will be expected to configure the core devices and few end devices to provide end-to-end connectivity and access to the internal servers and the external server.

1.  Each department/faculty is expected to be on its own separate IP network
2.  The switches should be configured with appropriate VLANs and security settings
3.  RIPV2 will be used to provide routing for the routers in the internal network and static routing for the external server.
4.  The devices in building A will be expected to acquire dynamic IP addresses from a router-based DHCP server

<h4> Tasks:</h4>

1.  Your task is to plan, design, and prototype the network topology for Albion University's network using Cisco Packet Tracer. Formative feedback will be given on this task in week 6.
2.  Configure in Packet Tracer the network with appropriate settings to achieve the connectivity and functionalities specified in the requirements.
3.  Produce a report (max 1500 words) including evaluation your proposed network design and critical appraisal on your work. Your evaluation should include performance, scalability, reliability and security of your proposed network.

---

## Network Diagram

Below is a network diagram for Albion University's network. The network consists of two campuses,
each with its own router and switches. The main campus has three buildings, each with its own switch
and PCs. The smaller campus has two floors, each with its own switch and PCs.
### Main Campus:<br>
![](https://github.com/hussainahmad402/Networking-Projects/blob/main/Pictures/main%20campus.PNG)<br>
### Smaller Campus:<br>
![](https://github.com/hussainahmad402/Networking-Projects/blob/main/Pictures/sub%20campus.PNG)


---

## Conclusion

The network design for Albion University effectively meets the requirements for connectivity, scalability, reliability, and security across both campuses. VLAN segmentation ensures efficient traffic management and security, while RIPV2 dynamic routing enables seamless interdepartmental communication. Centralized services, such as the DHCP and internal web server, streamline operations, and security measures like port security and VLAN ACLs protect sensitive data.

This design supports current needs and future growth, providing a robust, scalable, and secure infrastructure to enhance the university's academic and administrative functions