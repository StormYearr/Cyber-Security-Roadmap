# 📦 Room: Packets & Frames (TryHackMe)

In networking, large messages are broken down into smaller, manageable pieces to prevent bottlenecks. This room explains the structure of these pieces and the protocols that govern their delivery.



## 📝 Packets vs. Frames

While often used interchangeably, they exist at different layers of the OSI model:

* **Packet (Layer 3):** A piece of data that contains **IP addressing** (Source/Destination IP) and the payload.
* **Frame (Layer 2):** Encapsulates the packet and adds **Physical addressing** (Source/Destination MAC addresses). Think of the frame as the envelope and the packet as the letter inside.

### Key IP Header Fields:
| Header | Description |
| :--- | :--- |
| **TTL (Time to Live)** | An expiry timer to prevent packets from looping infinitely. |
| **Checksum** | Ensures data integrity by detecting corruption during transit. |
| **Source/Dest Address** | The IP addresses defining the sender and receiver. |

---

## 🤝 TCP: The Three-Way Handshake

TCP (Transmission Control Protocol) is **connection-oriented**. Before data is sent, a connection must be established using a 3-step process:

1.  **SYN (Synchronize):** Client sends a request with an Initial Sequence Number (ISN).
2.  **SYN/ACK (Acknowledge):** Server acknowledges the request and sends its own ISN.
3.  **ACK (Acknowledge):** Client confirms the server's ISN. Connection is now established.



### Closing a Connection:
TCP uses a **FIN** (Finish) packet to gracefully close a connection, ensuring all data has been received before terminating system resources.

---

## ⚡ UDP: User Datagram Protocol

Unlike TCP, UDP is **stateless** and **connectionless**.
* **No Handshake:** Data is sent immediately without waiting for a connection.
* **No Reliability:** There is no guarantee that data arrives, and no error-checking.
* **Use Cases:** Ideal for speed-sensitive applications like Video Streaming, Gaming, and VoIP.

---

## 🚪 Ports 101

Ports are numerical values (**0-65535**) that act as "docking points" for specific services.

### Common Ports (0-1024):
| Protocol | Port | Description |
| :--- | :--- | :--- |
| **FTP** | 21 | File Transfer Protocol |
| **SSH** | 22 | Secure Shell (Remote Management) |
| **HTTP** | 80 | Web Traffic (Unencrypted) |
| **HTTPS** | 443 | Web Traffic (Encrypted) |
| **SMB** | 445 | Windows File Sharing |
| **RDP** | 3389 | Remote Desktop Protocol |

---

## 🚀 Practical Challenge
In the lab, I practiced connecting to a remote host using specific IP and Port combinations:
* **Target:** `8.8.8.8`
* **Port:** `1234`
* **Result:** Successfully established a connection and retrieved the flag.

---

## 🧠 Key Takeaways
* **Encapsulation:** Data is wrapped in multiple layers of headers as it moves down the stack.
* **TCP vs UDP:** Use TCP for accuracy (Files/Email) and UDP for speed (Media).
* **Port Awareness:** Standard services use well-known ports, but they can be configured to run on non-standard ports (e.g., HTTP on 8080).

---
**Task Status:** ✅ Completed