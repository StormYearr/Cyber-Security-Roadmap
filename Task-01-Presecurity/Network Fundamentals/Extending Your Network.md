# 🌐 Room: Extending Your Network (TryHackMe)

This room focuses on the technologies required to extend a local network to the Internet securely. It covers how data is routed, how access is controlled, and how privacy is maintained across public networks.

## 🌉 Port Forwarding
Port Forwarding allows external devices on the Internet to access services (like a web server or game server) inside a private network.
* **Mechanism:** It maps a specific port on your **Router's Public IP** to a specific port on a **Device's Private IP**.
* **Use Case:** Making a local website (Intranet) available to the public.
* **Configuration:** Always configured at the **Router** level.

---

## 🧱 Firewalls 101
A Firewall is the "Border Security" of a network. It monitors and filters incoming and outgoing traffic based on an administrator's rules.

### Firewall Categories:
| Category | Description |
| :--- | :--- |
| **Stateful** | High-resource usage. It tracks the **entire connection** state. If a connection behavior becomes suspicious, it can block the entire device. |
| **Stateless** | Low-resource usage. It inspects **individual packets** against static rules. It doesn't care about the history of the connection. |

* **Operating Layers:** Firewalls typically operate at **Layer 3 & 4** of the OSI model, though modern Web Application Firewalls (WAFs) can reach Layer 7.

---

## 🔒 Virtual Private Networks (VPN)
A VPN creates a secure, encrypted "tunnel" between two devices over the Internet, effectively making them part of the same private network.

### Key Benefits:
* **Privacy:** Uses encryption to prevent "sniffing" (e.g., on public Wi-Fi).
* **Anonymity:** Hides your real IP address from the websites you visit.
* **Geographical Flexibility:** Connects branch offices in different cities into one logical network.

### Common VPN Technologies:
* **PPP:** Provides authentication and encryption but is non-routable.
* **PPTP:** Allows PPP data to travel across the Internet. Easy to set up but has weaker encryption.
* **IPSec:** Uses the existing IP framework. Offers strong encryption but is more complex to configure.

---

## 🔄 Routers vs. Switches (Advanced)

### Routers (Layer 3)
* **Function:** Their job is **Routing**—finding the optimal path for data between different networks based on shortest path, reliability, and speed.

### Switches (Layer 2 & 3)
* **Layer 2 Switch:** Forwards frames within a local network using **MAC addresses**.
* **Layer 3 Switch:** More sophisticated; it can forward frames like a L2 switch but also perform **Routing** using IP addresses.
* **VLAN (Virtual LAN):** A technology used in switches to virtually split a physical network into separate departments (e.g., Sales vs. Accounting) for improved security and traffic management.

---

## 🚀 Practical Lab: Network Simulation
In the interactive lab, I simulated the flow of a **TCP Three-Way Handshake** between computers across different network segments.
* **Key Learning:** Observed how routers pass packets and how many "handshake" steps are logged during a connection.
* **Result:** Successfully routed a TCP packet from Computer 1 to Computer 3 and retrieved the flag.

---

## 🧠 Key Takeaways
* **Segmentation:** Using VLANs and Firewalls is essential to restrict lateral movement within a network.
* **Security vs. Resources:** Stateful firewalls provide better security but require more hardware power than stateless ones.
* **VPN for Pentesting:** VPNs are crucial for ethical hackers to securely connect to target labs without exposing internal traffic to the ISP.

---
**Task Status:** ✅ Completed