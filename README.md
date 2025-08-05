# **Implementation and Analysis of BGP Peering and IGP Routing in a Telecom Backbone Network**

## **Project Overview**

This project demonstrates the **implementation and analysis of Border Gateway Protocol (BGP)** and **Interior Gateway Protocol (IGP)** in a **telecom backbone network**. The goal is to model how **BGP** facilitates communication between different **Autonomous Systems (AS)** and how **OSPF** (Open Shortest Path First), a widely used **IGP**, ensures efficient routing within a single AS. By simulating the integration of these protocols, the project provides insight into how data is transferred across telecom infrastructure.

The project aims to solve real-world telecom network challenges by combining both **inter-domain** and **intra-domain** routing in a seamless manner, allowing for optimal communication, fault tolerance, and scalability.

## **Project Components**

### **1. Network Topology and Design**

The network consists of a series of routers, each configured with **BGP** and **OSPF** for routing, and **PCs** to simulate end-user connectivity. The topology is as follows:

- **Router 1 (AS 65001)** connects to **Router 3 (AS 65010)** using **BGP** for inter-AS communication.
- **Router 2 (AS 65002)** connects to **Router 6 (AS 65002)** also using **BGP** for inter-AS communication.
- **Routers 3, 4, 5, and 6** use **OSPF** to establish routing within their own respective AS.

The network is designed to simulate a **telecom backbone** by connecting routers across different ASes while ensuring internal routing within each AS using OSPF.

### **2. Configured Routing Protocols**

- **BGP (Border Gateway Protocol)**: 
  - **Used for inter-domain communication**, specifically for routing between **different Autonomous Systems (AS)**. This ensures that data can be routed across different networks that are administratively separate but still need to communicate.
  - Configured between **Router 1 (AS 65001)** and **Router 3 (AS 65010)**, and between **Router 2 (AS 65002)** and **Router 6 (AS 65002)**.

- **OSPF (Open Shortest Path First)**: 
  - **Used for intra-domain communication** within a single AS. It ensures efficient and loop-free routing between routers in the same AS.
  - Configured between **Routers 3, 4, 5, and 6**, creating an internal backbone network for routing.

### **3. Tools and Technologies Used**

- **Cisco Packet Tracer**: The simulation software used to design and test the network topology.
- **Cisco CLI Commands**: Used for configuring BGP, OSPF, and interfaces, as well as for troubleshooting and verifying network status.
- **Ping/Traceroute**: For testing connectivity between devices and visualizing the routing path.

### **4. Configuration Files and Resources**

- **routers_and_bgp_igp_config.txt**: Contains the complete CLI configuration for both **BGP** and **OSPF** setups across all routers. This is the core configuration file that can be used to replicate the setup.
- **bgp_summary_screenshot.png**: A screenshot showing the output of the `show ip bgp summary` command, displaying the status of BGP neighbor relationships.
- **network_topology.png**: A visual diagram of the network topology, showing how the routers, switches, and PCs are interconnected.

## **Testing & Validation**

### **Ping Test**

To test the connectivity between **PC1** and **PC2**:

```bash
ping 10.1.1.2

ping 10.2.1.2

