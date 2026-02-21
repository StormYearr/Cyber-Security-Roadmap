# 🕸️ Room: Network Topologies and Protocols (TryHackMe)

This module explores how devices are physically and logically organized in a network, how data is routed, and how fundamental protocols like ARP and DHCP manage device identities and configurations.

## 📐 Network Topologies

Network topology refers to the arrangement of elements (links, nodes, etc.) in a communication network.



[Image of network topologies: Bus, Star, and Ring]


### 1. Star Topology
* **Concept:** Devices are connected to a central hub or switch.
* **Pros:** Highly scalable and reliable. If one cable fails, only that device is affected.
* **Cons:** Expensive due to cabling and dedicated equipment. If the central device fails, the whole network goes down (**Single Point of Failure**).

### 2. Bus Topology
* **Concept:** All devices share a single backbone cable.
* **Pros:** Cost-effective and easy to set up.
* **Cons:** Performance bottlenecks and difficult to troubleshoot. A break in the backbone cable takes down the entire network.

### 3. Ring Topology
* **Concept:** Devices are connected in a loop.
* **Pros:** Less cabling than Star; less prone to bottlenecks than Bus.
* **Cons:** Not efficient (data must pass through multiple devices). A single device failure can break the entire loop.

---

## 🛠️ Networking Hardware

| Device | Function |
| :--- | :--- |
| **Switch** | Connects devices within a LAN. It is efficient because it learns MAC addresses and sends data only to the intended port. |
| **Router** | Connects different networks and routes traffic between them using IP addresses. |

---

## 🍰 Subnetting: Slicing the Network
Subnetting is the process of dividing a large network into smaller, manageable "sub-networks."

* **Subnet Mask:** A 32-bit number (e.g., `255.255.255.0`) that defines the size of the network.
* **Network Address:** Identifies the start of the network (e.g., `.0`).
* **Default Gateway:** The device (Router) that allows communication with other networks.
* **Benefits:** Efficiency, improved security (segmentation), and better control.

---

## 📡 Essential Protocols

### 1. ARP (Address Resolution Protocol)
ARP is the bridge between the **Logical (IP)** and **Physical (MAC)** identifiers.
* **ARP Request:** "Who has IP 192.168.1.5? Tell me (the MAC)." (Broadcast)
* **ARP Reply:** "I have that IP. My MAC is AA:BB:CC..." (Unicast)
* **ARP Cache:** A local ledger where devices store these mappings.



### 2. DHCP (Dynamic Host Configuration Protocol)
Automates the assignment of IP addresses using the **DORA** process:
1.  **D**iscover: Client searches for a server.
2.  **O**ffer: Server offers an IP.
3.  **R**equest: Client requests the offered IP.
4.  **A**cknowledge (ACK): Server confirms the assignment.

---

## 🧠 Key Takeaways
* **Switching vs. Routing:** Switches work at the local level (MAC addresses), while Routers connect us to the wider world (IP addresses).
* **Network Segmentation:** Subnetting is a core security concept—separating guest Wi-Fi from internal employee systems prevents lateral movement by attackers.
* **Protocol Vulnerabilities:** Understanding ARP and DHCP is crucial for learning attacks like **ARP Spoofing** or **DHCP Starvation** later.

---
**Task Status:** ✅ Completed