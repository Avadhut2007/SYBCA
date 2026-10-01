# Part-2 Introduction Computer Network

## Computer Networks Reference Models

Figure 2.1 Tasks involved in sending a letter

![](Part-2%20Introduction%20Computer%20Network/imagesf377410d-0929-46a5-9669-976d4ee8c997-02_1322_1548_322_445.jpg)

## Protocol Hierarchies

![](Part-2%20Introduction%20Computer%20Network/imagesf377410d-0929-46a5-9669-976d4ee8c997-03_1223_1375_397_408.jpg)

## Index

- Protocols and Models
- Reference model
    - Seven-Layers of OSI(Open System Interconnection)
    - Concept of Layers
    - Benefit of using layered Models
- Summary of layers
- Protocols used at each layer
- Protocol Data Unit (PDU)
- TCP/IP Protocol Model
- Comparison of OSI and TCP/IP
- Addressing : Physical, Logical and Port addresses

## Protocols and Models

Communications Fundamentals - Networks vary in size, shape, and function. For communication to occur, devices must know “how” to communicate, including three elements in common:

- Message source (sender) - Message sources are people or electronic devices that need to send a message to other individuals or devices.
- Message Destination (receiver) - The destination receives the message and interprets it.
- Channel - This consists of the media that provides the pathway over which the message travels from source to destination.

Sending a message, whether face-to-face communication or over a network, is governed by rules called protocols. Protocols must account for the following requirements to successfully deliver a message that is understood by the receiver: An identified sender and receiver a Common language and grammar, Speed and timing of delivery, and Confirmation or acknowledgment requirements.

## Protocols and Models

Network Protocol Requirements - Common computer protocols include the following requirements:

- Message encoding
- Message formatting and encapsulation
- Message size
- Message timing
- Message delivery options

## Network Protocol Overview

Protocols are implemented by end devices and intermediary devices in software, hardware, or both. Each network protocol has its function, format, and rules for communications.

The table lists the various types of protocols that are needed to enable communications across one or more networks.

| Protocol Type | Description |
| --- | --- |
| Network Communications Protocols | Protocols enable two or more devices to communicate over one or more networks. The Ethernet family of technologies involves a variety of protocols such as IP, Transmission Control Protocol (TCP), HyperText Transfer Protocol (HTTP), and many more. |
| Network Security Protocols | Protocols secure data to provide authentication, data integrity, and data encryption. Examples of secure protocols include Secure Shell (SSH), Secure Sockets Layer (SSL), and Transport Layer Security (TLS). |
| Routing Protocols | Protocols enable routers to exchange route information, compare path information, and then to select the best path to the destination network. Examples of routing protocols include Open Shortest Path First (OSPF) and Border Gateway Protocol (BGP). |
| Service Discovery Protocols | Protocols are used for the automatic detection of devices or services. Examples of service discovery protocols include Dynamic Host Configuration Protocol (DHCP) which discovers services for IP address allocation, and Domain Name System (DNS) which is used to perform name-to-IP address translation. |

The functions of these protocols are addressing, reliability, flow control, sequencing, error detection, and application interface.

![](Part-2%20Introduction%20Computer%20Network/imagesf377410d-0929-46a5-9669-976d4ee8c997-08_1238_964_323_760.jpg)

Figure 1 OSI Reference Model

## Benefit of using layered model

- Assisting in protocol design because protocols that operate at a specific layer have defined information that they act upon and a defined interface to the layers above and below
- Fostering competition because products from different vendors can work together
- Preventing technology or capability changes in one layer from affecting other layers above and below
- Providing a common language to describe networking functions and capabilities
- Two models are: Open System Interconnection (OSI) Reference Model and TCP/IP Reference Model

![](Part-2%20Introduction%20Computer%20Network/imagesf377410d-0929-46a5-9669-976d4ee8c997-09_993_1915_765_284.jpg)

Figure 2 Shows network protocols and operations of layered model

## Reference model (OSI)

- OSI: Open System Interconnect
- Established in 1947, the International Standards Organization (ISO) is a multinational body dedicated to worldwide agreement on international standards. An ISO standard that covers all aspects of network communications is the Open Systems Interconnection (OSI) model. It was first introduced in the late 1970s and formally published by the ISO in 1984.

## Layers of OSI model

![](Part-2%20Introduction%20Computer%20Network/imagesf377410d-0929-46a5-9669-976d4ee8c997-11_1172_2332_465_78.jpg)

Figure 4 Shows responsibilities of OSI model layersOSI Reference Models

![](Part-2%20Introduction%20Computer%20Network/imagesf377410d-0929-46a5-9669-976d4ee8c997-12_1579_2333_255_112.jpg)

## OSI Reference model

- It is a set of protocols that allow communication between two different systems, irrespective of their architecture.
- Helps in understanding and building a network architecture that is interoperable, flexible, and robust.
- A layer should be created where a different abstraction is needed.
- Each layer should perform a well-defined function.
- Protocol simply defines which task need to be done at which layer and protocols handles those tasks.
The number of layer should be large enough that distinct function need not be thrown together in the same layer and small enough that architecture does not become unwieldy.

## An exchange using the OSI model

Figure 6 shows the exchange of information using the OSI model and the transmission medium.

![](Part-2%20Introduction%20Computer%20Network/imagesf377410d-0929-46a5-9669-976d4ee8c997-14_1331_2073_385_240.jpg)

Figure 6 Exchange of information using OSI model.

## The Physical Layer (1/3)

- The physical layer coordinates the functions required to carry a bit stream over a physical medium. (hub/repeater)

![](Part-2%20Introduction%20Computer%20Network/imagesf377410d-0929-46a5-9669-976d4ee8c997-15_697_2100_762_138.jpg)

## The Physical Layer (2/3)

- The physical layer is also concerned with the following responsibilities:
    - Physical characteristics of the medium and the interface between devices, like the connector cable.
    - Representation of bits. The physical layer data consists of a stream of bits(sequence of 0s or 1s). The physical layer defines the encoding type.
    - Data rate. The transmission rate (number of bits sent per second) is also defined by the physical layer.

## The Physical Layer(3 / 3)

- The synchronization of the sender and receiver clocks must be maintained.
- Line configuration. The physical layer is concerned with connecting devices to the media. (point to point, multi point)
- Physical topology The physical topology defines how devices are connected to make a network.
- Transmission mode The physical layer also defines the direction of transmission between two devices: simplex, half-duplex, or full-duplex.

## The Data Link layer(1/3)

- In the data link layer, the sender breaks up the input data into data frames and transmits the frames sequentially. If the service is reliable, the receiver confirms correct receipt of each frame by sending back an acknowledgement frame.
- The data link layer is responsible for moving frames from one hop (node) to the next.
- IEEE splits this layer into 2 sublayers
    - Logical Link Control
    - Media Access Control

## The Data Link layer(2/3)

![](Part-2%20Introduction%20Computer%20Network/imagesf377410d-0929-46a5-9669-976d4ee8c997-19_788_1144_619_66.jpg)

![](Part-2%20Introduction%20Computer%20Network/imagesf377410d-0929-46a5-9669-976d4ee8c997-19_780_1142_623_1279.jpg)

Figure Shows the data link layer information transmitted in OSI model.

## The Data Link layer(3/3)

- Framing
- Physical Addressing
- Error Control
- Flow Control
- Multiple Access control
- Node-to-Node delivery

## The Data Link layer

- Framing. The data link layer divides the stream of bits received from the network layer into manageable data units called frames.
- Physical addressing. If frames are to be distributed to different systems on the network, the data link layer adds a header to the frame to define the physical address of the sender (source address) and/or receiver (destination address) of the frame. If the frame is intended for a system outside the sender’s network, the receiver address is the address of the device that connects one network to the next.
- Flow control. If the rate at which the data are absorbed by the receiver is less than the rate produced in the sender, the data link layer imposes a flow control mechanism to prevent overwhelming the receiver.
- Error control. The data link layer adds reliability to the physical layer by adding mechanisms to detect and retransmit damaged or lost frames. It also uses a mechanism to prevent duplication of frames. Error control is normally achieved through a trailer added to the end of the frame.
- Access control. When two or more devices are connected to the same link, data link layer protocols are necessary to determine which device has control over the link at any given time.

## Network layer

![](Part-2%20Introduction%20Computer%20Network/imagesf377410d-0929-46a5-9669-976d4ee8c997-22_809_2118_432_188.jpg)

Figure 9 Shows the network layer information transmitted in OSI model.

The network layer is responsible for the delivery of individual packets from the source host to the destination host.

## The Network layer Source to destination delivery

![](Part-2%20Introduction%20Computer%20Network/imagesf377410d-0929-46a5-9669-976d4ee8c997-23_1381_2274_387_104.jpg)

Figure 10 Shows the network layer detailed information transmitted in OSI model.

## The Network layer

- If the two systems are attached to different networks with connecting devices between the networks, there is often a need for the network layer
- Source-to-destination delivery, possibly across multiple networks
- Logical addressing
- Routing
- Congestion control
- Packet
- Host to Host Delivery

## The Transport layer

- The transport layer is responsible for process-to- process delivery of the entire message.
- A process is an application program running on a host.
- It isolates upper layers from lower layers so that complexities and physical functions are hidden from the user.

## The Transport layer

- Service-point addressing(Port addressing ):- The transport layer header include a type of address called a service-point address (application).
- Segmentation and reassembly :- This layer takes care of sequencing and reassembly of message at receiver end.
- Connection control :- The transport layer can be either connectionless or connection oriented.
- Flow control :- Like the data link layer, the transport layer is responsible for flow control.

Error control :- Like the data link layer, the transport layer is responsible for error control.

## Reliable process-to-process delivery of a message

![](Part-2%20Introduction%20Computer%20Network/imagesf377410d-0929-46a5-9669-976d4ee8c997-27_819_2322_677_123.jpg)

## The session layer

- The session layer allows users on different machines to establish a session between them. e.g. file transfer, remote login
- Session Layer is responsible for establishing, maintaining, and terminating sessions. Session ID works at the Session Layer.
    - Dialog control:- Regulates which side transmits, plus when and how long it transmits.
    - Token management:- preventing two parties from attempting the same critical operation.
    - Synchronization:- Add checkpoints or synchronization points, so that communication can continue from the point of crash or disconnection.

## The presentation layer

- The presentation layer is concern with syntax and semantics of the information transmitted i.e. format of data to be exchanged.
- The presentation layer is responsible for
    - Translation :- Sender changes the information from its sender-dependent format into a common format. Receiving machine changes the common format into its receiverdependent format.

## The presentation layer

- Compression :- Data compression reduces the number of bits contained in the information so that bandwidth utilization is less. (images, audio, and video)
- Encryption :- This layer allows Encryption and Decryption to maintain security of data.

## Application Layer

- Enables user access to the network.
- Provides User interfaces and support for services such as
    - E-Mail
    - File transfer and access
    - Remote log-in
    - WWW

## Protocol supported at various layers

| Layer | Name | Protocols |
| --- | --- | --- |
| Layer 7 | Application | SMTP, HTTP, FTP, POP3, SNMP |
| Layer 6 | Presentation | MPEG, ASCH, SSL, TLS |
| Layer 5 | Session | NetBIOS, SAP |
| Layer 4 | Transport | TCP, UDP |
| Layer 3 | Network | IPV5, IPV6, ICMP, IPSEC, ARP, MPLS. |
| Layer 2 | Data Link | RAPA, PPP, Frame Relay, ATM, Fiber Cable, etc. |
| Layer 1 | Physical | RS232, 100BaseTX, ISDN, 11. |

Example OSI as a courier service story:

$$
\begin{aligned}
& \text { Application = Customer } \\
& \text { Transport = Courier service } \\
& \text { Network = Route planner } \\
& \text { Data Link = Local delivery } \\
& \text { Physical = Road }
\end{aligned}
$$

| Layer # | Layer Name | Primary Function | Unit of Data (PDU) | Common Protocols & Devices | Addressing / Identifier |
| --- | --- | --- | --- | --- | --- |
|  | 7Application | Network process to application. It provides services directly to user applications (like a web browser). | Data | HTTP, HTTPS, FTP, SMTP, DNS, SSH | Specialized User IDs(e.g., URL, Email Address) |
|  | 6Presentation | Data representation and encryption. It translates data between the application and network formats (syntax layer). | Data | SSL/TLS, JPEG, GIF, ASCII, EBCDIC | N/A |
|  | 5Session | Interhost communication. It establishes, manages, and terminates connections between applications. | Data | NetBIOS, RPC, PPTP | Session ID |
|  | 4Transport | End-to-end connections and reliability. It ensures complete data transfer and error recovery. | Segment / Datagram | TCP, UDP, Firewalls | Port Numbers (e.g., Port 80, 443) |
|  | 3Network | Path determination and logical addressing (IP). It routes data packets between different networks. | Packet | IP (IPv4, IPv6), ICMP, IPSec, Routers | Logical Address (IP)(e.g., 192.168.1.5) |
|  | 2Data Link | Physical addressing (MAC). It handles error detection and data transfer between adjacent nodes. | Frame | Ethernet, Wi-Fi (802.11), PPP, Switches, Bridges | Physical Address (MAC)(e.g., 00:1A:2B:3C:4D :5E) |
|  | 1Physical | Media, signal, and binary transmission. It defines the physical specifications (volts, cables, pins). | Bit | Cables (Cat6, Fiber), Hubs, Repeaters, Network Cards | N/A |

## Introduction TCP/IP

- The Internet Protocol Suite (commonly known as TCP/IP) is the set of communications protocols used for the Internet and other similar networks.
- It is named from two of the most important protocols in it:
- Transmission Control Protocol (TCP) and
- Internet Protocol (IP), the first two networking protocols defined in this standard.

## Reference Models

![](Part-2%20Introduction%20Computer%20Network/imagesf377410d-0929-46a5-9669-976d4ee8c997-36_1322_2238_432_110.jpg)

## TCP/IP Reference Model

Protocols and networks in the TCP/IP model initially.

| Application | HTTP, DNS, DHCP, FTP | Application |
| --- | --- | --- |
| Presentation |  |  |
| Session |  |  |
| Transport | TCP, UDP | Transport |
| Network | IPv4, IPv6, ICMPv4, ICMPv6 | Internet |
| Data Link  Physical | PPP, Frame Relay, b. Ethernet | Network Access |

## Host-to-network

Physical and Data Link Layers

- At the physical and data link layers, TCP/IP does not define any specific protocol.
- It supports all the standard and proprietary protocols.

## Internet Layer

- This represents network layer.
- The job of internet layer is to injects packets into any network and have them travel independently to the destination.
- The internet layer defines protocol called
    - IP (Internet protocol) and
    - four supporting protocols:

ARP,RARP, ICMP, and IGMP

## Internet Layer

- Internet protocol
    - It is an unreliable connectionless protocol-a best-effort delivery service.
    - The term best effort means that IP provides no error checking or tracking.
    - IP transports data in packets called datagrams, each of which is transported separately.
    - Datagrams can travel along different routes and can arrive out of sequence or be duplicated. IP does not keep track o the routes and has no facility for reordering datagrams once they arrive at their destination.

## Internet Layer

Supporting protocols-

- Address Resolution Protocol (ARP) is used to associate a logical address with a physical address. ARP is used to find the physical address of the node when its Internet address is known.
- Reverse Address Resolution Protocol (RARP) allows a host to discover its Internet address when it knows only its physical address. It is used when a computer is connected to a network for the first time.
»
- Internet Control Message Protocol (ICMP) is a mechanism used by hosts and gateways to send notification of datagram problems back to the sender. ICMP sends query and error reporting messages.
- Internet Group Message Protocol (IGMP) is used to facilitate the simultaneous transmission of a message to a group of recipients.

## The Transport Layer

- Two end-to-end transport protocols have been defined here
    - TCP (Transmission Control Protocol)
    - UDP (User Datagram Protocol)
- TCP is reliable connection-oriented protocol that allows byte stream originating on one machine to delivered without error on another machine in the network
- UDP is unreliable connectionless protocol for application that do not want TCP’s sequence flow. The application in which prompt delivery is very important UDP is used.

## Application Layer

- Does not have session or presentation layer.
- The application layer contains higher level protocols like
TELNET (Remote terminal access)
FTP (File transfer)
SMTP/POP3 (Electronic mail)
DNS (mapping host name on their network address)
HTTP(access to World Wide Web)

| OSI Model | TCP/IP Model |
| --- | --- |
| It is developed by ISO (International Standard Organization) | It is developed by ARPANET (Advanced Research Project Agency Network). |
| OSI model provides a clear distinction between interfaces, services, and protocols. | TCP/IP doesn’t have any clear distinguishing points between services, interfaces, and protocols. |
| Network layer has data unit packets | Internet layer has data unit Datagram |
| OSI uses the network layer to define routing standards and protocols. | TCP/IP uses only the Internet layer. |
| OSI layers have seven layers. | TCP/IP has four layers. |
| In the OSI model, the transport layer is only connection-oriented. | A layer of the TCP/IP model is both connectionoriented and connectionless. |
| In the OSI model, the data link layer and physical are separate layers. | In TCP, physical and data link are both combined as a single host-to-network layer. |
| Session and presentation layers are a part of the OSI model. | There is no session and presentation layer in the TCP model. |
| It is defined after the advent of the Internet. | It is defined before the advent of the internet. |

## Protocols at Application layer

- TELNET: Telnet stands for the TELetype NETwork. It helps in termin allows Telnet clients to access the resources of the Telnet server. It is use files on the internet. It is used for the initial setup of devices like switc command is a command that uses the Telnet protocol to communicate with a or system. Port number of telnet is 23.
- FTP: FTP stands for file transfer protocol. It is the protocol that actually let files. It can facilitate this between any two machines using it. But FTP is not ju but it is also a program. FTP promotes sharing of files via remote computers with rel. and efficient data transfer. The Port number for FTP is 20 for data and 21 for control.
- TFTP: The Trivial File Transfer Protocol (TFTP) is the stripped-down, stock versio FTP, but it’s the protocol of choice if you know exactly what you want and where a technology for transferring files between network devices and is a simplified version FTP. The Port number for TFTP is 69.

## Continued….

- SMTP: It stands for Simple Mail Transfer Protocol. It is a part of the I Using a process called “store and forward,” SMTP moves your email networks. It works closely with something called the Mail Transfer Agent your communication to the right computer and email inbox. The Port number for S is 25.
- SNMP: It stands for Simple Network Management Protocol. It gathers data the devices on the network from a management station at fixed or randon requiring them to disclose certain information. It is a way that servers information about their current state, and also a channel through which an administr can modify pre-defined values. The Port number of SNMP is 161(TCP) and 162(UDP).
- DNS: It stands for Domain Name System. Every time you use a domain name, therefo a DNS service must translate the name into the corresponding IP address. For example the domain name www.abc.com might translate to 198.105. The Port number for DNS is 53
- DHCP: It stands for Dynamic Host Configuration Protocol (DHCP). It addresses to hosts. There is a lot of information a DHCP server can provide when the host is registering for an IP address with the DHCP server. Por DHCP is 67, 68.

## Presentation layer protocols

- MPEG: The Moving Pictures Experts Group’s standard compression and coding of motion video for CD’s is very popular. QuickTime: This is for use with Machintosh or Power PC programs, it manages audio and video applications.
- SSL (Secure Socket Layer) and TLS (Transport Layer Security) are popular cryptographic protocols that are used to imbue web communications with integrity, security, and resilience against unauthorized tampering.

## Session layer protocols

- NetBIOS is a non-routable OSI Session Layer 5 Protocol and a service that allows applications on computers to communicate with one another over a local area network (LAN). NetBIOS was developed in 1983 by Sytek Inc. as an API for software communication over IBM PC Network LAN technology.
- SAP: The protocol used by SAP programs that communicate using the NI interface is called the SAP Protocol. This is an enhanced version of the TCP/IP protocol, which has been supplemented by one length field and some options for error information .

## Transport layer protocol

- Transmission Control Protocol (TCP) - is a transport protocol that is used on top of IP to ensure reliable transmission of packets. TCP includes mechanisms to solve many of the problems that arise from packet- based messaging, such as lost packets, out of order packets, duplicate packets, and corrupted packets.
- User Datagram Protocol (UDP) - a communications protocol that facilitates the exchange of messages between computing devices in a network. It’s an alternative to the transmission control protocol (TCP). In a network that uses the Internet Protocol (IP), it is sometimes referred to as UDP/IP.

## Internet protocol

- IPV6: Internet Protocol version 6 is the most recent version of the Internet Protocol, the communications protocol that provides an identification and location system for computers on networks and routes traffic across Internet.
- ICMP: ICMP is a network level protocol. ICMP messages communica information about network connectivity issues back to the source of the compromised transmission. It sends control messages such as destinatio network unreachable, source route failed, and source quench.
- MPLS: Multiprotocol Label Switching, or MPLS, is a networkin technology that routes traffic using the shortest path based on “labels, rather than network addresses, to handle forwarding over private wide area networks.
- ARP: ARP is the protocol used to associate the IP address to a address. When a host wants to send a packet to another host, say IP 10.5. 5.1, on its local area network (LAN), it first sends out (broac ARP packet.

## Data Link Layer Protocol

- PPP: In computer networking, Point-to-Point Protocol is a data link layer communication protocol between two routers directly without any host or any other networking in between. It can provide connection authentication, transmission encryption, and data compression.
- ATM: ATM is a core protocol used in the SONET/SDH backbone of the public switched telephone network (PSTN) and in the Integrated Services Digital Network (ISDN), but has largely been superseded in favor of nextgeneration networks based on Internet Protocol (IP) technology

## Physical layer Protocols

- ISDN: ISDN or Integrated Services Digital Network is a circuit- switched telephone network system that transmits both data and voice over a digital line. You can also think of it as a set communication standards to transmit data, voice, and signaling These digital lines could be copper lines.
- 100Base-TX: 100Base-TX is an Ethernet networking standard (IEEE 802.3u standard.) that supports up to 100 Mbps transfer speed. 100Base-TX was also called as FastEthernet, because Ethernet was 10 Mbps that time and FastEthernet was faster than Ethernet.

Physical Address (MAC Address)

- Layer: Data Link Layer (Layer 2).
- Definition: A 48-bit unique identifier burned into the Network Interface Card (NIC) by the manufacturer.
- Purpose: Local delivery between directly connected nodes on the same network (subnet).
- Scope: Changes at each hop (router) along the path from source to destination.
- Example: 00:1A:2B:3C:4D:5E.

Logical Address (IPAddress)

- Layer: Network Layer (Layer 3).
- Definition: A hierarchical address (32-bit for IPv4, 128-bit for IPv6) that represents a host’s location in a network.
- Purpose: Routing data packets across different networks (globally).
- Scope: Remains constant from source to final destination.
- Example: 192.168.1.1.

Port Address (Port Number)

- Layer: Transport Layer (Layer 4).
- Definition: A 16-bit identifier (0 to 65,535) assigned by the OS to specific applications or services.
- Purpose: Identifies specific processes or applications (e.g., Web, Email) on a host.
- Example: Port 80 (HTTP), Port 443 (HTTPS).