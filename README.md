# Cisco Packet Tracer Networking Project

This project demonstrates subnetting, router configuration, and inter-department communication in **Cisco Packet Tracer**.  
The network was designed to connect two departments: **Accounts** and **Delivery**, ensuring that PCs in different subnets can communicate with each other through a router.

---

##  Project Overview
- Subnetted a **Class C network (192.168.40.0/24)** into **two /25 subnets**.
- Configured a router with IP addresses on GigabitEthernet interfaces.
- Deployed switches to connect PCs and printers within each department.
- Assigned IP addresses, subnet masks, and default gateways to PCs.
- Verified connectivity using the `ping` command.

---

##  Network Topology
- **Accounts Department (Subnet 1)**  
  - Network ID: `192.168.40.0/25`  
  - Gateway (Router Gig0/0): `192.168.40.1`  
  - Example PC IPs: `192.168.40.2`, `192.168.40.3`  

- **Delivery Department (Subnet 2)**  
  - Network ID: `192.168.40.128/25`  
  - Gateway (Router Gig0/1): `192.168.40.129`  
  - Example PC IPs: `192.168.40.130`, `192.168.40.131`  

---

##  Configuration Details
### Router
- **GigabitEthernet0/0** → `192.168.40.1 255.255.255.128`  
- **GigabitEthernet0/1** → `192.168.40.129 255.255.255.128`  

### PCs
- **Accounts PCs**:  
  - IPs: `192.168.40.2 – 192.168.40.126`  
  - Gateway: `192.168.40.1`  

- **Delivery PCs**:  
  - IPs: `192.168.40.130 – 192.168.40.254`  
  - Gateway: `192.168.40.129`  

---

##  Verification

### Router Interfaces (`show ip interface brief`)
