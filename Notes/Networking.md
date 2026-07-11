
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
### Definitions

**network segment** - group of networked devices using a shared medium or channel for information transfer ^networkSegment
**Telnet** - network protocol used to connect to remote systems and communicate using text commands. Command: telnet <ip_address> <port_number>