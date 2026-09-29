<div align="center">
  <h1>🌐 Network Simulation: RIP, Voice VLAN & DHCP</h1>
  
  <p>
    <b>Task 4: Implementation of Routing Information Protocol, Voice VLAN, and DHCP Server using Cisco Packet Tracer.</b>
  </p>

<br />

## 📖 Project Overview
This repository contains the configuration and testing documentation for a network topology built in Cisco Packet Tracer. This project was developed to meet evaluation criteria that include dynamic routing (RIP), VLAN segmentation, Inter-VLAN Routing, automated IP distribution (DHCP), and Voice over IP (VoIP) services across a multi-router network architecture.

## 🗺️ Network Topology
The network architecture consists of four interconnected routers (RouterA, RouterB, RouterC, RouterD), dividing the network into specific segments for Data and Voice traffic.

<div align="center">
  <img width="716" height="348" alt="{A76F8E08-1C9D-43A0-AD4F-CD243D6DE0D3}" src="https://github.com/user-attachments/assets/ca5575b8-e16d-4744-9a31-9cde64087010" />

</div>

---

## 🛠️ Technology & Implementation Details

Here is a breakdown of the key technologies implemented in this topology:

*   **Dynamic Routing (RIP):** We used Routing Information Protocol (RIP) to enable communication between the four routers (RouterA, RouterB, RouterC, and RouterD). By looking at the Routing Tables, RIP successfully learned and advertised all the different network segments, allowing packets to reach their destinations seamlessly.
*   **VLAN & Inter-VLAN Routing:** The network is segmented into multiple VLANs (e.g., VLAN 10, 11, 12, 13, 14, 15, 16) to separate traffic logically. To allow these VLANs to communicate with each other and reach the outside network, Inter-VLAN routing (Router-on-a-Stick method) is configured on the router sub-interfaces.
*   **Voice VLAN & IP Phone:** Voice VLANs are implemented specifically for the Cisco 7960 IP Phones. The network utilizes Cisco's Call Manager Express (CME) or Telephony Service on the routers to assign Directory Numbers (DN) to the IP phones, enabling VoIP calls across the network.
*   **DHCP Server:** The DHCP server is configured (either centrally on a Server-PT or distributed on the routers) to automatically assign IP addresses, subnet masks, default gateways, and DNS server addresses to end devices like PCs, Laptops, and Smartphones.
*   **DNS & Web Server:** A central Server-PT is configured as a Web Server and a DNS Server. End devices use the DNS server
---

## 🎯 Task Achievements & Documentation
Below is the documentation of the testing results based on the task requirements:

### 1. 🖧 Routing Tables Across All Routers
Verification of the routing tables using the `show ip route` command on RouterA, RouterB, RouterC, and RouterD to ensure the **RIP** protocol has successfully advertised all network segments.

### 2. ⚡ Client Connectivity Test Between Routers
ICMP Ping testing between End Devices (PCs, Laptops, Smartphones, and Printers) located in different network segments to ensure seamless routing without Request Time Out (RTO).

### 3. 🖥️ Client IP Configuration (DHCP)
Verification that the **DHCP Server** successfully distributes IP Configurations automatically to all connected clients, 

### 4. 📞 IP Phone Connectivity Test (Voice VLAN)

### 5. 🌍 DNS Server Connection Test
Testing domain resolution by accessing `tkj.com` from various client devices to the central Server-PT.
