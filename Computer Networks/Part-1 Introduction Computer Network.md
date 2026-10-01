# Part-1 Introduction Computer Network

## Unit 1 Introduction to Computer Networks

## Networks

- A network is set of devices (nodes) connected by communication links (media)
- A node can be a computer, printer, or other device capable of sending and/or receiving data.
- Link connecting the devices are often called communication channels

## Computer Networks

El A computer network is a group of interconnected nodes or computing devices that exchange data and resources with each other. A network connection between these devices can be established using cable or wireless media.

In The computers can be geographically located anywhere.

![](Part-1%20Introduction%20Computer%20Network/images5bb8631e-b214-453d-8635-50ccc7f80efb-03_712_806_835_1641.jpg)

## Network Components

- End Devices (Nodes/Host/sender/receiver): Computers, smartphones, printers, loT devices, servers.
- Message(data): The actual data or file being sent.
- Transmission Media: wired, wireless. The path through which data is transmitted.
- Connecting Devices: switch, hub, router. The devices used to interconnect end devices.
- Software Components: protocols.

![](Part-1%20Introduction%20Computer%20Network/images5bb8631e-b214-453d-8635-50ccc7f80efb-04_613_1399_1123_1041.jpg)

COMPUTER NETWORK COMPONENTS

## Network Components

## End Devices (Nodes) :

- Hosts:
Computers, smartphones, printers, loT devices.
- Servers:
Powerful computers providing shared resources, storage, and services (e.g., file, print, web servers).

The devices that initiate and accept the information.

## Network Components

- Message(data):
The actual data or file being sent.

## Network Components

## Connecting Devices (Intermediary Devices):

- Router: Connects different networks and directs traffic between them.
- Switch: Connects multiple devices within the same network, intelligently forwarding data.
- Hub: Connects devices, broadcasting data to all ports (older tech).
- Modem: Connects your network to the internet (ISP).
- Firewall: Monitors and controls incoming/outgoing network traffic for security.
- Wireless Access Point (WAP): Enables wireless connectivity.

## Connecting Devices

![](Part-1%20Introduction%20Computer%20Network/images5bb8631e-b214-453d-8635-50ccc7f80efb-08_813_1767_639_271.jpg)

Types of Network Devices

## Network Components

HOLS O

- Wired: Twisted pair, Coaxial cable, Fiber optic cables.
- Wireless: Radio waves (Wi-Fi, Bluetooth), microwaves, infrared.

![](Part-1%20Introduction%20Computer%20Network/images5bb8631e-b214-453d-8635-50ccc7f80efb-09_597_1463_1018_290.jpg)

## Network Components

## Software Components:

- Network Operating System (NOS): Software that runs servers (e.g., Windows Server, Linux).
- Protocols: Rules and standards (like TCP/IP, HTTP, DNS) that govern how devices communicate.

The predefined rules that standardize communication, ensuring both the sender and receiver understand each other.

- Network Applications: Software used for sharing (e.g., email, web browsers).

## Goals of Networks

r Resource Sharing
r. Hardware (computing resources, disks, printers)
- Software (application software)
Information Sharing
Elasy accessibility from anywhere (files, databases)
5 Search Capability (WWW)
Email Message broadcast
Communication
r High Reliability
Distribution of work
Cost saving
J. Security

## Applications of Computer Networks

Business Applications
Resource sharing
Daily communication
E-commerce(B-B)
Home Applications
Access to remote information
- Person to person communication.
- Entertainment
- E-commerce(B-C)
- E-learning
Mobile Applications
- M-commerce
- GPS
Mobile applications

## Applications of Computer Networks

- Business applications:
- Educational applications:
- Healthcare applications:
- Entertainment applications:
- Milifary applications:
- Scientific applications:
- Transportation applications:
- Banking and finance app|ications:

## Types of Topology

- The way in which a network is laid out physically
- 4 basic types: mesh, star, bus, ring
- May often see hybrid

![](Part-1%20Introduction%20Computer%20Network/images5bb8631e-b214-453d-8635-50ccc7f80efb-14_627_1637_994_305.jpg)

## Topology

- Network topologies are the different ways devices are arranged and interconnected in a network, defining how data flows between them and encompassing both the physical (how devices are physically connected) and logical (how data travels) structures.
- The choice of topology depends on factors such as network size, cost, scalability, and reliability requirements.

## Selection Criteria for Topologies

–Each n/w topology has is own advantages & disadvantages; selection of topology depends on the needs of the particular application.
–Size of the n/w & no. of devices(nodes) being connected.
–Ease of configuration & installing
–The ease of adding a new device(user) in an existing n/w.
–The ease of fault indication & correction.
–No. of physical links required to be used for connecting devices.
–Whether connecting devices such as repeaters, switches, hubs are required or not.
–Costs involved.
–Need for data security
–Need of n/w administration.

## Star Topology

–In star topology, all computers are connected via cables to a central location, where they are all connected by a device called a hub.
–There is no direct connections among computers.
–star are used in concentrated n/w where the endpoints are directly reachable from a central location, when n/w expansion is expected & when greater reliability is needed.

![](Part-1%20Introduction%20Computer%20Network/images5bb8631e-b214-453d-8635-50ccc7f80efb-17_552_1345_1306_1098.jpg)

Advantage-

1. It is easy to add new computers without disturbing rest n/w.
2. Easy to install and maintain
3. Fault diagnosis is easy
4. If a computer or link fails it does not bring down the whole n/w.
5. Different types of cable can be used in n/w.

Disadvantage-

1. If the central Hub is fails, the whole $\mathrm{n} / \mathrm{w}$ fails.
2. Many star $\mathrm{n} / \mathrm{w}$ require a device at the central point to rebroadcast.
3. Cabling costs more.

## Mesh Topology

–In Mesh Topology, every device is physically connected to every other device with a point-to-point dedicated link.
–Dedicated means the link carries data only between 2 devices.
–It doesn’t have a traffic congestion problem.

![](Part-1%20Introduction%20Computer%20Network/images5bb8631e-b214-453d-8635-50ccc7f80efb-19_845_1092_1027_1368.jpg)

Advantages-

1. Robust because the failure of any one computer doesn’t bring down the entire n/w.
2. Provides security & Privacy.
3. Point-to-point links make fault diagnosis easy
4. Each connection can carry data reliably.
5. MAC Address need not be used.

Disadvantage-

1. Since every computer is connected to every computer, installation & reconfiguration is difficult.
2. Cabling costs more.
3. Suitable for smaller n/w.
4. The $\mathrm{h} / \mathrm{w}$ required to connect each link I/O & cable is expensive.

## Bus Topology

–A long cable called a bus is used as the backbone to all the nodes. The tap is a connector that connects the node to the metallic core of the bus via a drop line.
–When 1 computer sends a signal on the cable, all the computers on the n/w receive the information. However, only one with the address that matches the destination address stored in the message accepts the information, while all others reject the message.
–The speed is low because one computer can send a message at a time.

![](Part-1%20Introduction%20Computer%20Network/images5bb8631e-b214-453d-8635-50ccc7f80efb-21_507_2417_1355_19.jpg)

## Advantages of Bus Topology-

1. It is easy to understand, install & use for small $\mathrm{n} / \mathrm{ws}$.
2. The cabling cost is less as it requires a small length of cable to connect the computers.
3. It is easy to expand by joining two cables with a BNC
4. In the expansion of bus topology, repeaters can be used to boost the signal & increase the distance.

## Disadvantages of Bus Topology-

1. Heavy n/w traffic slows down the bus speed. In bus topology, only one computer can transmit & other have to wait till their turn comes & there is no coordination between computers for reservation of the transmitting time slot.
2. A cable break or loose BNC connector will cause reflections & bring down the whole n/w, causing all n/w activity to stop.

## Ring Topology

- In a ring topology, each computer is connected to the next computer, with the last one connected to the first.
– Rings are used in high performance n/ws.
–Every computer is connected to the next computer in the ring & each retransmits what it receives from the previous computer hence, the ring is an active n/w.
–The message flow around the ring is in one direction. There is no termination because there is no end to the ring.
–Some ring n/w’s do token passing. A short message called a token is passed around the ring.
–Each token is sent around the ring until it reaches its final destination.
–Ring is a flow of information in only one direction, is not used if a large no. of nodes are connected.

## Ring Topology

![](Part-1%20Introduction%20Computer%20Network/images5bb8631e-b214-453d-8635-50ccc7f80efb-24_1365_1673_328_494.jpg)

## Advantages of Ring Topology-

–Every computer gets equal access.
–Even when the load on the network increases, its performance is better than that of Bus topology.

## Disadvantages of Ring Topology-

–Failure of one component on the ring can affect the whole n/w
–Difficult to troubleshoot
–Each packet of data must pass through all the computers between source and destination. This makes it slower than a star topology.
–Adding or removing a computer is difficult. It disturb n/w

## Tree Topology

–It is a variation of a star.
–Not every computer is plugged into the central hub. Most of the hosts are connected to the secondary hub, which in turn is connected to the central hub.
–The central hub is active, which contains repeaters, which amplify the signal & increase the distance a signal can travel.
–Secondary hubs may be active or passive. Passive only provide connection.

![](Part-1%20Introduction%20Computer%20Network/images5bb8631e-b214-453d-8635-50ccc7f80efb-26_971_1628_874_624.jpg)

## Hybrid Topology

–It makes use of 2 or more basic topologies together.
–There are different ways in which a hybrid n/w is created.
–Practical n/w generally use hybrid topology.

![](Part-1%20Introduction%20Computer%20Network/images5bb8631e-b214-453d-8635-50ccc7f80efb-27_919_1984_829_269.jpg)

## Types of Computer Networks

The computer networks can be categorized into four categories.

1. Based on Geographical Area
2. Based on Transmission Medium
3. Based on Communication Type
4. Based on Ownership

## Based on Geographical Area

Classification of interconnected processors by network scale.

| Interprocessor distance | Processors located in same | Example  Personal area network  Local area network  Metropolitan area network  Wide area network  The Internet |
| --- | --- | --- |
| 1 m | Square meter |  |
| 10 m | Room |  |
| 100 m | Building |  |
| 1 km | Campus |  |
| 10 km | City |  |
| 100 km | Country |  |
| 1000 km | Continent |  |
| $10,000 \mathrm{~km}$ | Planet |  |

## Personal Area Network

- A PAN is a network that is used for communicating among computers and computer devices (including telephones) in close proximity of around a few meters within a room.
- PAN’s can be wired or wireless
    - PAN’s can be wired with a computer bus such as a universal serial bus: USB (a serial bus standard for connecting devices to a computer-many devices can be connected concurrently)
    - PAN’s can also be wireless through the use of bluetooth, wireless USB ,Z-wave, Zigbee.

![](Part-1%20Introduction%20Computer%20Network/images5bb8631e-b214-453d-8635-50ccc7f80efb-30_1094_866_490_1519.jpg)

## Home Network

- Computers (desktop PC, PDA, shared peripherals
- Entertainment (TV, DVD, VCR, camera, stereo, MP3)
- Telecomm (telephone, cell phone, intercom, fax)
- Appliances (microwave, fridge, AC, washing machine)
- Telemetry (utility meter, alarm, baby cam).

## Home Network

![](Part-1%20Introduction%20Computer%20Network/images5bb8631e-b214-453d-8635-50ccc7f80efb-32_1243_1579_428_428.jpg)

## Local Area Network

- Usually privately owned and links the devices in a single office, building, or campus
- LAN size is limited to a few kilometers.
- LANs are designed to allow resources to be shared (hardware, software and data )
- Today LANs to have data rates of 100 Mbps to 10Gbps
- Multiple LANs can be connected by devices like bridges or switches.

## Local Area Network

Figure 1-2

![](Part-1%20Introduction%20Computer%20Network/images5bb8631e-b214-453d-8635-50ccc7f80efb-34_1075_2009_414_207.jpg)

## Local Area Network

Figure 1-2

![](Part-1%20Introduction%20Computer%20Network/images5bb8631e-b214-453d-8635-50ccc7f80efb-35_1358_1823_357_328.jpg)

## Metropolitan Area Network

- MAN covers a city.
- A MAN has no specific topology.
- Can be used for both voice and data.
- Best example of MAN is cable television network available in many cities.
- Company LANs connected by MAN within city.
- Wireless MAN is called as WIMAX

## Metropolitan Area Networks

- A metropolitan area network based on cable TV.

![](Part-1%20Introduction%20Computer%20Network/images5bb8631e-b214-453d-8635-50ccc7f80efb-37_1093_1966_631_246.jpg)

## Wide Area Network

- WAN spans a large geographical area, often a country or continent
- WAN provides long-distance transmission of data, voice, image, and video information over large geographical areas
- Use public, private, or leased communication equipment.

## Wide Area Network

![](Part-1%20Introduction%20Computer%20Network/images5bb8631e-b214-453d-8635-50ccc7f80efb-39_913_2479_536_10.jpg)

Wide Area Networks

![](Part-1%20Introduction%20Computer%20Network/images5bb8631e-b214-453d-8635-50ccc7f80efb-40_835_2282_520_112.jpg)

## Based on Transmission medita

- Wired Medium
- Wireless Medium

## Wireless Networks

Categories of wireless networks:

- System interconnection
- Wireless LANs
- Wireless WANs

## Wireless Networks

![](Part-1%20Introduction%20Computer%20Network/images5bb8631e-b214-453d-8635-50ccc7f80efb-43_988_2170_479_194.jpg)

## Communication Types

- Point-to-point - dedicated link

![](Part-1%20Introduction%20Computer%20Network/images5bb8631e-b214-453d-8635-50ccc7f80efb-44_763_1842_744_367.jpg)

- Multipoint (Multidrop, Broadcast) - shared a single link

![](Part-1%20Introduction%20Computer%20Network/images5bb8631e-b214-453d-8635-50ccc7f80efb-45_841_1845_744_325.jpg)

## Modes of Communication

- Simplex - unidirectional; one transmits, other receives

![](Part-1%20Introduction%20Computer%20Network/images5bb8631e-b214-453d-8635-50ccc7f80efb-46_549_1456_897_448.jpg)

## Direction of Data Flow

- Half-duplex - each can transmit/receive; communication must alternate

![](Part-1%20Introduction%20Computer%20Network/images5bb8631e-b214-453d-8635-50ccc7f80efb-47_370_1826_929_305.jpg)

## Direction of Data Flow

- Full-duplex - both can transmit/receive simultaneously

![](Part-1%20Introduction%20Computer%20Network/images5bb8631e-b214-453d-8635-50ccc7f80efb-48_406_2031_890_244.jpg)

## Based on Ownership

Private networks are owned by individuals or organizations (e.g., LANs)
public networks are owned by government or service providers (e.g., Internet, WAN).

Other types include Intranets (internal, single-org ownership) and

## Protocols and Standards

- Why do we need them?
- A protocol is a set of rules that governs data communication; the key elements of a protocol are
    - Syntax - data formats and Signal levels
    - Semantics - control information and error handling
    - Timing - speed matching and sequencing
- Standards are necessary to ensure that products from different manufacturers can work together as expected.

## Standards

- Need-
    - To maintain open and competitive market for various equipment manufacturers
    - To guarantee ,technology and processes used operate at national and international levels.
    - To provide guideline for equipment manufacturers, vendors, government agencies and other service providers to ensure interconnectivity is achieved at international communication.
- Types -
    - De facto - by convention or widespread use
    - De jure (Formal) - legislated by an officially recognized body
- Standards Organizations
    - Committees - ISO, ITU-T, ANSI, IEEE, and EIA

## Summary

- Definition of Computer Network
- Types of Networks
- Topology & types of topology
- Communication Types
- Modes of Communication
- Server Based LANs & Peer-to-PeerLANs
- standards

## Question Bank

2 Marks Questions:

- Define Computer networks.
- Define topology. What are the two types of topology?
- List any four goals of networking.
- What is peer entities?
- Which are the two types of transmission technologies in computer networks?
- Define broadcast networks.
- What are point-to-point networks?
- State the difference between De-Facto and De-Jury standards.
- What is meant by acknowledged connectionless service.

## Question Bank

5 Marks Questions:

- What are computer networks and what are network goals?
- Explain applications of computer networks.
- State the difference between LAN and WAN.
- Explain different types of networks.
- State and explain different topologies in detail.