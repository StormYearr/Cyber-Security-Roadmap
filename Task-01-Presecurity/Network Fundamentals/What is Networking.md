# 🌐 Room: What is Networking? (TryHackMe)

Networking is the backbone of Cybersecurity. This room covers the fundamentals of how devices communicate, identify each other, and how to test connectivity between them.



## 📝 Core Concepts

### 1. What is a Network?
A network is simply a group of connected devices (from 2 to billions) that exchange data. Examples include the Internet, public transportation systems, and even social circles.

### 2. The Internet
The Internet is a **"Network of Networks."** - **Private Network:** A local network (like your home Wi-Fi) where devices communicate internally.
- **Public Network:** The global network (The Internet) that connects these small private networks.
- **Key Figure:** Tim Berners-Lee invented the World Wide Web (WWW) in 1989.

---

## 🆔 Identifying Devices on a Network

Just like humans have names and fingerprints, devices have two primary identifiers:

### 1. IP Address (Internet Protocol)
Think of this as a device's "mailing address."
- **IPv4:** Uses 4 octets (e.g., `192.168.1.1`). Limited to ~4.29 billion addresses.
- **IPv6:** The modern standard with 8 groups of hex digits. Supports 340 undecillion addresses to solve IPv4 exhaustion.
- **Private vs. Public:** Private IPs identify you inside your home; Public IPs identify your entire home to the outside world.

### 2. MAC Address (Media Access Control)
Think of this as a device's "fingerprint."
- It is a unique 12-character hexadecimal physical address assigned at the factory.
- **Security Note:** MAC addresses can be **spoofed** (faked) to bypass security filters (e.g., bypassing a paid Wi-Fi gate).



---

## 🛠 Tool Highlight: `ping` (ICMP)

`ping` is one of the most fundamental tools for network troubleshooting. It uses the **ICMP** (Internet Control Message Protocol) to check if a remote host is "alive."

**How it works:**
1. Your device sends an **ICMP Echo Request**.
2. The target device (if reachable) sends back an **ICMP Echo Reply**.
3. The tool measures the **Round Trip Time (RTT)** in milliseconds (ms).

**Command Syntax:**
```bash
# Ping an IP address
ping 8.8.8.8

# Ping a domain name
ping tryhackme.com