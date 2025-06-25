# TCP/IP Model 

The **TCP/IP model** is a **four-layer networking framework** developed by the U.S. Department of Defense in the 1970s. 
It enables **reliable and standardized communication** between devices over various networks like LANs, WANs, and the internet. 
It simplifies the **seven-layer OSI model** into four key layers, each handling different aspects of data transmission.

---

## Roles of TCP/IP

- Ensures interoperability between diverse systems and network types.
- Provides **accurate, reliable data delivery** through packet-based transmission and reassembly.
- Enables **global communication** by routing data efficiently.

---

## Layers of TCP/IP Model

### 1. Application Layer

- Closest to users and applications.
- Supports protocols like **HTTP, FTP, DNS, SMTP**.
- Manages data formatting, session, and encryption.

### 2. Transport Layer

- Ensures correct and reliable delivery of data.
- Uses:
  - **TCP** (Transmission Control Protocol) – reliable, connection-oriented.
  - **UDP** (User Datagram Protocol) – faster, connectionless.
- Manages **flow control**, **segmentation**, and **reassembly**.

### 3. Internet Layer

- Routes packets using **IP addressing**.
- Uses protocols like:
  - **IP** (Internet Protocol)
  - **ICMP** (Internet Control Message Protocol)
  - **ARP** (Address Resolution Protocol)
- Handles **packet forwarding**, **fragmentation**, and **logical addressing**.

### 4. Network Access Layer

- Interfaces with **physical hardware** (e.g., Ethernet, Wi-Fi).
- Manages:
  - **MAC addressing**
  - **Framing**
  - **Error detection**
- Includes technologies like **Ethernet**, **Wi-Fi**, etc.

---

# TCP Segment Structure

A **TCP segment** consists of two main parts:
1. **Header** (20 to 60 bytes)
2. **Data** (payload)

## TCP Header Fields

### 1. **Source Port Address (16-bit)**
- Identifies the port of the **sending application**.

### 2. **Destination Port Address (16-bit)**
- Identifies the port of the **receiving application**.

### 3. **Sequence Number (32-bit)**
- Indicates the **byte number** of the **first byte** in the segment.
- Helps in reordering segments at the receiver’s end.

### 4. **Acknowledgement Number (32-bit)**
- Specifies the **next byte** expected from the sender.
- Used for **cumulative acknowledgment**.

### 5. **Header Length (HLEN - 4-bit)**
- Length of the TCP header in **4-byte words**.
- Values range from **5 (20 bytes)** to **15 (60 bytes)**.

### 6. **Control Flags (6 bits)**
| Flag | Purpose |
|------|---------|
| URG  | Urgent pointer is valid |
| ACK  | Acknowledgment number is valid |
| PSH  | Push function |
| RST  | Reset the connection |
| SYN  | Synchronize sequence numbers |
| FIN  | Terminate the connection |

### 7. **Window Size (16-bit)**
- Specifies the **receiver’s buffer size** (flow control).

### 8. **Checksum (16-bit)**
- **Mandatory** for error checking in TCP.

### 9. **Urgent Pointer (16-bit)**
- Points to the **last urgent byte** in the data.
- Only valid if the **URG flag** is set.

---
