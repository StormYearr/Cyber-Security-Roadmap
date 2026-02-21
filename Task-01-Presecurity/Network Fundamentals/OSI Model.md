# 📑 Room: The OSI Model (TryHackMe)

The Open Systems Interconnection (OSI) Model is a theoretical framework that describes how data is transmitted over a network. It consists of **7 layers**, each with specific functions and protocols.



[Image of the 7 layers of the OSI model]


## 🛠️ Key Concepts

### Encapsulation
As data travels down the OSI layers (from Layer 7 to Layer 1), each layer adds specific information (headers) to the data. This process is called **Encapsulation**. When the receiving device processes the data, it removes these headers layer by layer, which is called **De-encapsulation**.

---

## 🏗️ The 7 Layers of OSI

### Layer 7: Application
This is the layer users interact with directly. It provides a GUI for applications to communicate with the network.
* **Protocols:** HTTP/HTTPS (Browsers), SMTP/IMAP (Email), FTP (File Transfer), DNS.

### Layer 6: Presentation
Acts as a **translator**. It ensures that data is in a usable format and handles data compression and encryption.
* **Key Function:** Data Encryption (e.g., SSL/TLS) and formatting (e.g., JPEG, GIF, PNG).

### Layer 5: Session
Manages the "dialogue" between computers. It creates, maintains, and terminates connections (sessions).
* **Key Function:** Synchronization and checkpoints (to resume data transfer if interrupted).

### Layer 4: Transport
Responsible for the delivery of data. It chooses between two main protocols based on the need for speed vs. reliability.
* **TCP (Transmission Control Protocol):** Guarantees delivery, error-checking, and order. Used for Web, Email, and File sharing.
* **UDP (User Datagram Protocol):** Faster but lacks reliability (no error checking). Used for Video Streaming, Gaming, and VoIP.



### Layer 3: Network
This layer is responsible for **Routing**. It finds the most optimal path for data to travel across different networks using **IP Addresses**.
* **Devices:** Routers.
* **Protocols:** IP, OSPF (Open Shortest Path First), RIP (Routing Information Protocol).

### Layer 2: Data Link (Recap)
Provides physical addressing and handles error detection from the physical layer.
* **Key Identifier:** MAC Address.
* **Devices:** Switches.

### Layer 1: Physical
The lowest layer, representing the physical hardware. Data is transmitted as **Electrical Signals** or pulses of light in **Binary** (0s and 1s).
* **Hardware:** Ethernet cables (Copper/Fiber), Hubs, Repeaters.

---

## 🧠 Why is the OSI Model Important for Security?
* **Troubleshooting:** Helps isolate where a problem is occurring (e.g., "Is it a Layer 1 cable issue or a Layer 3 routing issue?").
* **Attack Categorization:** Attacks are often described by their OSI layer. For example:
    * **Layer 3/4 Attacks:** DDoS attacks targeting bandwidth or connection limits.
    * **Layer 7 Attacks:** Web application attacks like SQL Injection or XSS.
* **Defense in Depth:** Understanding these layers allows us to implement security controls at every level (Firewalls at L3/L4, WAFs at L7).

---
**Task Status:** ✅ Completed