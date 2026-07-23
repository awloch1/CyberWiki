**OSI Model:**
- 1. Phisical - provides the physical connection between devices and is responsible for transmitting raw bits over a communication medium.
- 2. Data Link - Describes an agreement between the different systems on the same [[#^networkSegment|network segment]] on how to communicate - *==Frames==*
- 3.  Network - Sending data between different networks. **E.g. IP, ICMP, VPN, IPSec and SSL/TLS VPN.** - *==Packet==*
- 4. Transport - enables end-to-end communication between running applications on different hosts. E.g **UDP - ==Datagram== , TCP - ==Segment==**
- 5. Session Establishing, maintaining, and synchronising sessions. E.g. **NFS, RPC**
- 6. Presentation - Data encoding, encryption, and compression. E.g. Unicode, **MIME, JPEG, PNG, MPEG**
- 7. Application - Providing services and interfaces to applications.  E.g. **HTTP, FTP, DNS, POP3, SMTP, IMAP**

**TCP/IP Model:**
- 1. **Application Layer** -  The OSI model application, presentation and session layers, i.e., layers 5, 6, and 7
- 2. **Transport Layer** - same as layer 4 from OSI model
- 3. **Internet Layer** - same as network layer from OSI
- 4. Link Layer - same as data link layer from OSI 

**Private IP addresses:**
- `10.0.0.0` - `10.255.255.255`
- `172.16.0.0` - `172.31.255.255`
- `192.168.0.0` - `192.168.255.255`

### TCP (Transmission Control Protocol)
TCP is a connection-oriented transport protocol, which means that a TCP connection must be established between two devices before any data can be transmitted.

A TCP connection is established using what’s called a three-way handshake:
1. **SYN: ** The client initiates the connection by sending a SYN packet to the server. This packet contains the client’s randomly chosen initial sequence number.
2. **SYN+ACK:** The server responds to the SYN packet with a SYN-ACK packet, which adds the initial sequence number randomly chosen by the server.
3. **ACK:** The three-way handshake is completed as the client sends an ACK packet to acknowledge the reception of the SYN-ACK packet.

### UDP (User Datagram Protocol)
 UDP is a simple connectionless protocol, which means that it does not need to establish a connection unlike TCP.

### DHCP (Dynamic Host Configuration Protocol)
DHCP is an application-level protocol that relies on UDP; the server listens on UDP port 67, and the client sends from UDP port 68
DHCP follows four steps:
- **Discover**: The client broadcasts a ==DHCPDISCOVER== message seeking the local DHCP server if one exists.
- **Offer**: The server responds with a ==DHCPOFFER== message with an IP address available for the client to accept.
- **Request**: The client responds with a ==DHCPREQUEST== message to indicate that it has accepted the offered IP.
- **Acknowledge**: The server responds with a ==DHCPACK== message to confirm that the offered IP address is now assigned to this client.
### ARP (Address Resolution Protocol)
Allows a host device to determine the MAC address of another device on the local network.
ARP process;:
- ARP sends a broadcast request to the MAC address `ff:ff:ff:ff:ff:ff`
- Only the device with the requested IP address responds with its MAC address

### ICMP (Internet Control Message Protocol)
Protocol that is mainly used for network diagnostics and error reporting.
The commands are:
- Ping
- Traceroute

### NAT (Network Address Translation)
The idea behind NAT lies in using **one public IP address** to provide Internet access to **many private IP addresses**

### Routing Protocols
- **OSPF (Open Shortest Path First)** – a **link-state routing protocol** that shares network topology information and calculates the best path based on **cost** (e.g., bandwidth).
- **EIGRP (Enhanced Interior Gateway Routing Protocol)** – a **Cisco proprietary advanced distance-vector routing protocol** that exchanges routing information and selects the best path using multiple metrics, such as **bandwidth** and **delay**.
- **BGP (Border Gateway Protocol)** – an **inter-domain routing protocol** used to exchange routing information **between autonomous systems (ASes)** on the Internet and determine the best external routes.
- **RIP (Routing Information Protocol)** – a **distance-vector routing protocol** that exchanges routing information and selects the best path based on the **fewest number of hops**, making it suitable for small networks. 

### DNS (Domain Name System)

**DNS** is a system that translates **domain names** (e.g., `google.com`) into **IP addresses** so computers can communicate with each other over the Internet.
**DNS records** are entries stored in the DNS database. They contain information about a domain.
**Examples:**
- **A Record** - maps a domain name to an **IPv4 address**.  
  Example: `example.com → 172.17.2.172`
- **AAAA Record** - maps a domain name to an **IPv6 address**.  
  Example: `example.com → 2001:db8::1`
- **CNAME Record** - maps one domain name to another domain name (an alias).  
  Example: `www.example.com → example.com`
- **MX Record** - specifies the mail server responsible for handling emails for a domain.  
  Example: `example.com → mail.example.com`

### FTP (File Transfer Protocol)
Protocol used to transfer files between a client and a server over a network. FTP listens on TCP port **21** by default;
Example commands:
- `USER` is used to input the username
- `PASS` is used to enter the password
- `RETR` (retrieve) is used to download a file from the FTP server to the client.
- `STOR` (store) is used to upload a file from the client to the FTP server.

### Emails

##### **SMTP (Simple Mail Transfer Protocol)**  
Protocol that defines how a mail client talks with a mail server and how a mail server talks with another. The SMTP server listens on TCP port **25** by default.
Commands:
- `HELO` or `EHLO` initiates an SMTP session
- `MAIL FROM` specifies the sender’s email address
- `RCPT TO` specifies the recipient’s email address
- `DATA` indicates that the client will begin sending the content of the email message
- `.` is sent on a line by itself to indicate the end of the email message
##### **POP3 (Post Office Protocol version 3)**
Protocol designed to allow the client to communicate with a mail server and retrieve email messages. POP3 server listens on TCP port **110** by default

##### **IMAP (Internet Message Access Protocol)**
Protocol that allows synchronizing read, moved, and deleted messages. IMAP server listens on TCP port **143** by default.



### Commands:
`WHOIS <website address>` -  provides information about the entity that registered a domain name, including the registrant's name, phone number, email address, and physical address.

### Definitions

**network segment** - group of networked devices using a shared medium or channel for information transfer ^networkSegment

**Telnet** - network protocol used to connect to remote systems and communicate using text commands. Command: telnet <ip_address> <port_number>


### Ports

|**Protocol**|**Transport Protocol**|**Default Port Number**|
|---|---|---|
|TELNET|TCP|23|
|DNS|UDP or TCP|53|
|HTTP|TCP|80|
|HTTPS|TCP|443|
|FTP|TCP|21|
|SMTP|TCP|25|
|POP3|TCP|110|
|IMAP|TCP|143|
