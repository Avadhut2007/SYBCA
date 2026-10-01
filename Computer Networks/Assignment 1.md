# Assignment 1

**Assignment 1**

#### Q1. Explain how networks affect our lives with suitable examples.

A computer network is a collection of interconnected devices computers, phones, servers, and other equipment — that can exchange data and share resources. Over the last three decades, networks have moved from being a convenience used mainly by large organisations to being an invisible layer underneath almost every activity of daily life. Their influence can be seen in communication, business, education, entertainment, governance, and even physical infrastructure such as power grids and traffic systems.

**1. Communication**

Email, instant messaging, voice/video calls (WhatsApp, Zoom, Teams) and social media all rely on networks to carry messages instantly across the globe. A person in India can have a real-time video call with a relative in the United States because underlying networks (LAN → ISP → WAN → Internet) relay the data in milliseconds.

**2. Business and E-commerce**

Online banking, stock trading, and e-commerce platforms such as Amazon or Flipkart depend on networks connecting customers to remote servers. Enterprise networks link branch offices so that inventory, payroll, and customer data stay synchronised across locations.

**3. Education**

Networks enable e-learning platforms, virtual classrooms, digital libraries, and remote examinations. During events such as the COVID-19 pandemic, networked video-conferencing tools allowed schools and colleges to continue teaching without physical classrooms.

**4. Entertainment**

Streaming services (Netflix, YouTube, Spotify) and online multiplayer gaming depend entirely on high-speed networks to deliver audio, video, and interactive data with minimal delay.

**5. Healthcare**

Hospitals use networks for electronic health records, telemedicine consultations, and remote monitoring of patients through connected medical devices, improving access to care in remote areas.

**6. Governance and Infrastructure**

Government services (e-governance portals, digital identity systems such as Aadhaar, online tax filing) and smart-city infrastructure (traffic signals, surveillance, smart grids) all run on networked systems that collect and exchange data continuously.

In short, networks have transformed how people communicate, work, learn, shop, and are governed — making information exchange faster, cheaper, and available almost anywhere, while also raising new concerns such as privacy, security, and the digital divide.

#### Q2. Describe the components of a computer network with neat diagrams.

A computer network is built from a combination of hardware and software elements that work together to allow devices to communicate. The major components are described below.

**1. Nodes (End Devices)**

Any device connected to the network that can send or receive data — computers, laptops, smartphones, printers, and servers. Each node has a Network Interface Card (NIC) that provides the hardware connection point and a unique physical (MAC) address.

**2. Server**

A powerful computer that provides resources or services (files, web pages, email, printing) to other computers (clients) on the network.

**3. Transmission Medium**

The physical or wireless path over which data travels — twisted-pair cable, coaxial cable, fibre-optic cable, or wireless radio waves (Wi-Fi, Bluetooth, satellite).

**4. Networking (Connecting) Devices**

- Hub — a simple multi-port repeater that broadcasts incoming data to all connected ports.
- Switch — an intelligent device that forwards data only to the intended destination port using MAC addresses.
- Router — connects different networks and forwards data based on IP addresses, choosing the best path.
- Modem — converts digital signals to analog (and back) so data can travel over telephone/cable lines.

**5. Protocols**

A protocol is a set of rules that governs how data is formatted, transmitted, and received (e.g., TCP/IP, HTTP, FTP). Protocols ensure that devices from different manufacturers can still understand each other.

**6. Network Software**

Operating systems and applications (Network OS, drivers, network management software) that control how hardware resources are shared and how communication is managed.

![](Assignment%201/67c241fc3afaa839f36d887814d6bf9188bb2741.png)

*Fig 2.1 — Basic components of a computer network*

#### Q3. Differentiate between Client–Server and Peer-to-Peer networks.

Networks can be organised in two broad architectural models depending on how resources and control are distributed among the connected devices.

![](Assignment%201/6cfc69a0c5ac8bd5804807a48cce971144d97b32.png)

*Fig 3.1 — Client–Server architecture (left) vs Peer-to-Peer architecture (right)*

| **Aspect** | **Client–Server Network** | **Peer-to-Peer (P2P) Network** |
| --- | --- | --- |
| Architecture | Centralised — dedicated server(s) provide services | Decentralised — every node is both client and server |
| Resource sharing | Managed and controlled by the server | Resources shared directly between peers |
| Cost | Higher (needs dedicated server hardware/software) | Lower (no dedicated server required) |
| Security | Centralised and easier to enforce | Weaker; each peer manages its own security |
| Scalability | Scales well with proper server capacity planning | Becomes difficult to manage as peers increase |
| Performance | Depends on server capacity; can bottleneck | Distributed load; no single bottleneck |
| Administration | Requires a trained network administrator | Simple; each user administers their own machine |
| Reliability | Single point of failure (server down = service down) | More fault-tolerant; failure of one peer has limited effect |
| Typical use | Corporate networks, websites, email, banking | Home networks, small offices, file-sharing (BitTorrent) |

#### Q4. Explain LAN, MAN, and WAN with one example each.

Networks are classified by the geographical area they span. The three most common categories are LAN, MAN, and WAN.

**LAN — Local Area Network**

A LAN connects computers and devices within a small, limited geographical area such as a single building, office, or campus, typically spanning up to a few kilometres. LANs offer high data transfer rates (100 Mbps to several Gbps), low cost, and are usually owned and managed by a single organisation using Ethernet cables or Wi-Fi.

**Example:** The computer lab in a college, where all systems are connected through switches to share a common printer and internet connection.

**MAN — Metropolitan Area Network**

A MAN spans a larger area than a LAN, typically covering a city or town, connecting several LANs together. It is generally owned by a group of organisations or a single large provider and uses high-speed links such as fibre-optic cable.

**Example:** A cable television network or a city-wide network connecting all branches of a bank within the same city.

**WAN — Wide Area Network**

A WAN spans a very large geographical area — across cities, countries, or even continents — by connecting multiple LANs and MANs, usually through leased telephone lines, satellite links, or fibre backbones. WANs generally have lower speeds than LANs and involve multiple owners/carriers.

**Example:** The Internet itself, or a multinational company's network connecting its offices in India, the USA, and the UK.

| **Feature** | **LAN** | **MAN** | **WAN** |
| --- | --- | --- | --- |
| Coverage | Building / campus | City | Country / global |
| Ownership | Single organisation | One or few organisations | Multiple organisations/ISPs |
| Speed | Very high | High | Comparatively lower |
| Cost of setup | Low | Moderate | High |
| Example | College computer lab | City cable network | The Internet |

#### Q5. Compare simplex, half-duplex, and full-duplex modes of communication.

The transmission mode (or communication mode) defines the direction in which data can flow between two connected devices over a link.

**Simplex Mode**

Data flows in only one direction — one device is always the sender and the other is always the receiver. The full capacity of the channel is used in a single direction, and the receiver cannot send data back on the same channel.

**Example:** Keyboard to CPU, television broadcasting, or radio broadcasting.

**Half-Duplex Mode**

Data can flow in both directions, but only one direction at a time — while one device transmits, the other can only receive, and they must take turns. The full bandwidth is available to whichever device is transmitting at that moment.

**Example:** Walkie-talkies, where only one person can speak at a time while the other listens.

**Full-Duplex Mode**

Data can flow in both directions simultaneously — both devices can send and receive at the same time. This offers the best utilisation of channel capacity, typically because the channel's total bandwidth is split (or separate channels are used) for each direction.

**Example:** A telephone conversation, where both people can speak and listen at the same time.

| **Aspect** | **Simplex** | **Half-Duplex** | **Full-Duplex** |
| --- | --- | --- | --- |
| Direction of data flow | One direction only | Both directions, one at a time | Both directions simultaneously |
| Channel utilisation | Used fully by sender only | Shared, used alternately | Used efficiently by both |
| Example device | Keyboard, TV remote | Walkie-talkie | Telephone |
| Efficiency | Low (one-way only) | Moderate | High |

#### Q6. Explain different network topologies (Star, Bus, Ring, Mesh, Tree) with diagrams, advantages and disadvantages.

Network topology refers to the physical or logical arrangement of nodes and links in a network. The choice of topology affects cost, reliability, scalability, and ease of troubleshooting.

**1. Star Topology**

![](Assignment%201/9f65bf193334658b47e37887eb1caf93db7d7ff1.png)

*Fig 6.1 — Star Topology: every node connects to a central hub/switch*

Every device is connected individually to a central device (hub or switch); all data passes through this centre.

- Advantage: Easy to install and troubleshoot; failure of one node does not affect others.
- Advantage: Centralised management and easy to add/remove nodes.
- Disadvantage: If the central hub/switch fails, the entire network goes down.
- Disadvantage: Requires more cabling than bus topology, increasing cost.

**2. Bus Topology**

![](Assignment%201/972f4fdaa005e88c0db503782fdaa69b88ed23ca.png)

*Fig 6.2 — Bus Topology: all nodes share a single common backbone cable*

All devices are connected to a single central cable (the 'bus' or backbone), with terminators at both ends.

- Advantage: Simple, low-cost, and requires less cable than other topologies.
- Advantage: Easy to extend by adding new nodes to the bus.
- Disadvantage: A break in the main cable brings down the entire network.
- Disadvantage: Performance degrades as more devices are added (collisions increase).

**3. Ring Topology**

![](Assignment%201/a8cc4d60f56c4835163e4fa07788aa2840401268.png)

*Fig 6.3 — Ring Topology: each node connects to exactly two neighbours, forming a closed loop*

Each device is connected to exactly two other devices, forming a closed loop; data travels around the ring in one (or both) directions.

- Advantage: Data flows in a predictable, orderly fashion with no collisions (using token passing).
- Advantage: Easier to identify a faulty node than in a bus network.
- Disadvantage: A single break in the ring can disrupt the entire network (unless a dual ring is used).
- Disadvantage: Adding or removing a node disrupts network activity.

**4. Mesh Topology**

![](Assignment%201/af102efc9a5983e8cdea191ca9def510f7c2065f.png)

*Fig 6.4 — Mesh Topology: every node connects directly to every other node*

Every device has a dedicated point-to-point link to every other device in the network.

- Advantage: Highly reliable — failure of one link/node does not affect the rest.
- Advantage: Excellent for high-priority, high-security communication (e.g., military, backbone networks).
- Disadvantage: Very expensive and difficult to install due to the large amount of cabling (n(n-1)/2 links).
- Disadvantage: Complex to manage and reconfigure as the network grows.

**5. Tree Topology**

![](Assignment%201/b7a388b1643fd2e57f3dc0e15e8065c33ba2671c.png)

*Fig 6.5 — Tree Topology: a hierarchical structure combining multiple star networks*

A hierarchical structure that combines characteristics of star and bus topologies — groups of star-configured devices connect to a central 'root' bus/hub.

- Advantage: Easily scalable; new branches (star networks) can be added without disturbing the whole network.
- Advantage: Fault isolation is easier since branches can be managed independently.
- Disadvantage: Heavily dependent on the root/backbone — its failure affects all connected branches.
- Disadvantage: Requires more cabling and complex configuration compared to a simple star.

#### Q7. Discuss the functions of Hub, Switch, and Router.

![](Assignment%201/8ad535be9aeb5eb81553cb7fd0bc7d35bbc8d187.png)

*Fig 7.1 — Hub, Switch, and Router operate at different OSI layers*

**Hub**

A hub is the simplest connecting device, operating at the Physical layer (Layer 1) of the OSI model. It works as a multi-port repeater: whatever data it receives on one port, it broadcasts to every other connected port, regardless of the intended destination. Hubs have no intelligence, cannot filter traffic, and all connected devices share the same collision domain, which reduces efficiency as the number of devices increases. They are largely obsolete today, replaced by switches.

**Switch**

A switch operates mainly at the Data Link layer (Layer 2) and is a more intelligent version of a hub. It learns and maintains a MAC address table of devices connected to each port, and forwards incoming frames only to the port where the destination device is located, instead of broadcasting to all ports. This reduces unnecessary traffic, prevents collisions between ports, and allows multiple simultaneous conversations, greatly improving network performance.

**Router**

A router operates at the Network layer (Layer 3) and connects two or more different networks (e.g., a LAN to the Internet). It examines the destination IP address of each packet and uses a routing table to determine the best path to forward the packet toward its destination across networks. Routers also perform functions such as Network Address Translation (NAT), traffic filtering, and can connect networks using different technologies.

#### Q8. Explain types of communication networks: Point-to-Point, Multipoint, Broadcast — with advantages and disadvantages.

Based on how a transmission line is shared between devices, communication networks (physical connection types) are classified as follows.

**1. Point-to-Point**

A dedicated link exists between exactly two devices, and the entire capacity of the link is reserved for those two devices. Example: two computers connected directly by a single cable, or a leased telephone line between two offices.

- Advantage: High security and dedicated bandwidth since the link is not shared.
- Advantage: Simple to set up and troubleshoot.
- Disadvantage: Not scalable — connecting many devices needs many separate links (expensive).
- Disadvantage: Wastage of resources if the link is idle much of the time.

**2. Multipoint (Multidrop)**

More than two devices share the same link; the capacity of the channel is shared, either spatially (each device uses it at a different physical point) or temporally (devices take turns). Example: several terminals connected to a single mainframe over a shared line.

- Advantage: More economical since fewer links are required to connect multiple devices.
- Advantage: Efficient utilisation of the transmission medium.
- Disadvantage: Reduced effective bandwidth per device as more devices join.
- Disadvantage: Possibility of data collisions if access is not properly controlled.

**3. Broadcast**

A single sender transmits data to all devices on the network simultaneously; every connected device receives the same data whether or not it is the intended recipient. Example: radio and television transmission, or a message sent to a broadcast address on a LAN.

- Advantage: Very efficient for distributing the same information to many recipients at once.
- Advantage: Simple addressing — no need to know each recipient individually.
- Disadvantage: Wastes bandwidth, since devices that don't need the data still receive it.
- Disadvantage: Lower security, as any device on the network can capture the broadcast data.

#### Q9. Case study — College campus (Administrative block, Computer labs, Library).

Consider a college campus with three main locations — the Administrative block, Computer labs, and the Library — that need to be networked together for file sharing, internet access, and centralised control.

**(a) Suitable network type: Client–Server**

A Client–Server network is more suitable than Peer-to-Peer for a college campus. Centralised servers can host student records, library catalogues, and academic resources, enforce security policies, manage user accounts and permissions, and provide reliable backups — all of which are difficult to achieve consistently in a peer-to-peer setup with dozens or hundreds of independent machines.

**(b) Suitable topology: Extended Star / Tree Topology**

A Tree topology (built from multiple Star-configured LANs) is ideal here. Each block (Administrative, Labs, Library) can have its own Star network with a local switch, and these local switches are then connected to a central backbone switch/router in a hierarchical (tree) structure. This is chosen because it combines the manageability and fault isolation of Star topology within each block with the scalability of Tree topology across the whole campus — a fault in the Library's local network, for example, does not bring down the Administrative block.

**(c) Networking devices used**

- Switches — one in each block (Admin, Labs, Library) to connect local computers within that block.
- Router — to connect the campus network to the Internet/ISP and to route traffic between the three blocks and outside networks.

**(d) Transmission media and signal type**

Fibre-optic cable is recommended as the backbone medium connecting the three blocks (Admin, Labs, Library) since it offers high bandwidth, long-distance reach without much attenuation, and immunity to electromagnetic interference — suitable for a campus-wide backbone. Within each block, twisted-pair (UTP/Ethernet) cable or Wi-Fi (wireless) can be used to connect individual computers to the local switch, since distances are short. The signal type used is digital signalling throughout, as modern computer networks transmit data in digital (binary) form rather than analog.

#### Q10. Explain the need for the OSI Reference Model.

In the early days of networking, different manufacturers built hardware and software using their own proprietary standards, which meant that equipment from one vendor often could not communicate with equipment from another. The Open Systems Interconnection (OSI) Reference Model was developed by the International Organization for Standardization (ISO) in 1984 to solve this problem by providing a common, vendor-neutral framework for network communication.

**Why the OSI model is needed**

- Standardisation: It defines universal standards so that hardware and software from different vendors can interoperate.
- Modularity: It breaks the complex task of network communication into seven smaller, manageable layers, each with a well-defined function.
- Simplifies troubleshooting: Because each layer has a specific job, faults can be isolated to a particular layer, making diagnosis faster.
- Independent development: Each layer can be developed, upgraded, or replaced independently as long as the interface with adjacent layers is preserved (e.g., changing a physical cable type does not require changing application software).
- Ease of learning and teaching: It provides a structured, conceptual way to understand how data moves from an application on one computer to an application on another.
- Encourages interoperability: It allows different types of network hardware and protocols to work together in a predictable manner.

In short, the OSI model acts as a reference blueprint — not a protocol itself — against which real protocol suites (such as TCP/IP) can be compared, understood, and taught.

#### Q11. Differentiate between TCP and UDP.

TCP (Transmission Control Protocol) and UDP (User Datagram Protocol) are the two main transport-layer protocols used to send data between applications over an IP network, but they differ significantly in how they operate.

| **Aspect** | **TCP** | **UDP** |
| --- | --- | --- |
| Connection type | Connection-oriented (handshake required) | Connectionless (no handshake) |
| Reliability | Reliable — guarantees delivery, uses acknowledgements | Unreliable — no guarantee of delivery |
| Ordering | Ensures data arrives in the correct order | No ordering guarantee |
| Error checking/recovery | Extensive error checking and retransmission of lost data | Basic error checking only; no retransmission |
| Speed | Slower due to overhead of acknowledgements and control | Faster, with minimal overhead |
| Header size | Larger (20–60 bytes) | Smaller (8 bytes) |
| Flow/congestion control | Yes | No |
| Use cases | Web browsing (HTTP/HTTPS), email, file transfer (FTP) | Video/audio streaming, online gaming, DNS, VoIP |

In summary, TCP prioritises reliability and correctness at the cost of speed, making it suitable for applications where data integrity matters (like transferring a file), while UDP prioritises speed and low latency at the cost of reliability, making it suitable for real-time applications where occasional data loss is acceptable (like a live video call).

#### Q12. Explain the OSI Reference Model with a neat diagram.

![](Assignment%201/efae6c78cb122a9a055de4cf59b4afc828ab35a5.png)

*Fig 12.1 — The seven layers of the OSI Reference Model*

The OSI model organises network communication into seven layers, each responsible for a specific part of the process, from the physical transmission of bits to the application that the user interacts with. Data passed by the sender's application travels down through each layer (each adding its own header/trailer — a process called encapsulation), and at the receiver, it travels back up through the layers (decapsulation) until it reaches the destination application.

**Layer 1 — Physical**

Deals with the actual transmission of raw bits (0s and 1s) over the physical medium — cables, connectors, voltages, and signalling. Concerned with hardware such as hubs, cables, and NICs.

**Layer 2 — Data Link**

Provides node-to-node data transfer, organises bits into frames, performs error detection, and uses MAC addresses for physical addressing. Switches operate at this layer.

**Layer 3 — Network**

Responsible for logical addressing (IP addresses) and routing of packets across different networks to find the best path from source to destination. Routers operate at this layer.

**Layer 4 — Transport**

Ensures complete, reliable data transfer between end systems, handling segmentation, flow control, and error recovery. TCP and UDP operate at this layer.

**Layer 5 — Session**

Establishes, manages, and terminates sessions (dialogues) between two communicating applications, including synchronisation and checkpointing for long transfers.

**Layer 6 — Presentation**

Translates, encrypts/decrypts, and compresses data so that the application layer can interpret it correctly, regardless of differences in data representation between systems.

**Layer 7 — Application**

The layer closest to the end user, providing network services directly to applications — protocols like HTTP, FTP, SMTP, and DNS operate here.

#### Q13. Describe the TCP/IP Reference Model with a neat diagram and explain each layer in detail.

![](Assignment%201/decd555f5d23dc3ffb4a046d864ecd565f771f69.png)

*Fig 13.1 — The four layers of the TCP/IP Reference Model*

The TCP/IP model is the practical, protocol-based framework that actually powers the Internet today. Developed by the U.S. Department of Defense before the OSI model, it condenses communication into four layers rather than seven.

**1. Network Access (Link) Layer**

Combines the functions of the OSI Physical and Data Link layers. It is responsible for the physical transmission of data over the network hardware, including framing, physical/MAC addressing, and error detection at the hardware level. Ethernet and Wi-Fi (802.11) operate at this layer.

**2. Internet Layer**

Corresponds to the OSI Network layer. It handles logical addressing (IP addresses) and routing of packets from the source host to the destination host across possibly many intermediate networks. The main protocol here is IP (Internet Protocol); ICMP (used by 'ping') and ARP also operate at this layer.

**3. Transport Layer**

Corresponds to the OSI Transport layer, providing end-to-end communication services for applications. TCP offers reliable, connection-oriented delivery, while UDP offers fast, connectionless delivery, as explained in Q11.

**4. Application Layer**

Combines the functions of the OSI Session, Presentation, and Application layers into one. It provides protocols that applications use directly to communicate over the network, such as HTTP/HTTPS (web), FTP (file transfer), SMTP/IMAP/POP3 (email), and DNS (name resolution).

Because the TCP/IP model has fewer, broader layers, it is considered more practical for implementation, while the OSI model remains valuable as a detailed teaching and reference tool.

#### Q14. Compare OSI and TCP/IP models with a suitable table.

![](Assignment%201/b3f14ffe5b3ca03fb67ebad003b79718eb9bbc7d.png)

*Fig 14.1 — Layer-wise mapping between the OSI and TCP/IP models*

| **Aspect** | **OSI Model** | **TCP/IP Model** |
| --- | --- | --- |
| Number of layers | 7 layers | 4 layers |
| Developed by | ISO (International Organization for Standardization) | U.S. Department of Defense (DARPA) |
| Nature | Conceptual/reference model | Implementation-based, practical model actually used on the Internet |
| Approach | Layer functions defined before protocols | Protocols were developed first, then layers described around them |
| Layers included | Physical, Data Link, Network, Transport, Session, Presentation, Application | Network Access, Internet, Transport, Application |
| Reliability | Guarantees reliable delivery at the Transport layer only | Transport layer offers both reliable (TCP) and unreliable (UDP) options |
| Usage today | Used mainly as a teaching/reference model | Used as the actual protocol suite of the Internet |

#### Q15. Explain Physical, Logical, and Port addressing in detail with examples.

![](Assignment%201/42ecd8c02c858d5c3969c5621e481a178ab1c02f.png)

*Fig 15.1 — Physical, logical, and port addressing operating at different layers*

Different layers of the network model use different types of addresses to correctly identify a device, a network, and finally a specific application/process, so that data reaches exactly the intended destination.

**1. Physical Address (MAC Address)**

Operates at the Data Link layer. It is a unique, hardware-burned-in address assigned to the Network Interface Card (NIC) of a device, used for communication within the same local network (link). It is a 48-bit address, usually written as six pairs of hexadecimal digits.

**Example:** 00:1A:2B:3C:4D:5E — used by a switch to decide which port to forward an Ethernet frame to.

**2. Logical Address (IP Address)**

Operates at the Network layer. It is a software-assigned address that identifies a device's location on a network and across different networks, allowing routers to determine the best path to deliver data from source to destination. IPv4 addresses are 32-bit (e.g., four decimal numbers), while IPv6 addresses are 128-bit.

**Example:** 192.168.1.10 (IPv4) identifies a specific host on a specific network, regardless of which physical link it currently uses.

**3. Port Address**

Operates at the Transport layer. Since a single computer can run many applications/processes simultaneously (a browser, an email client, a chat app), the port number identifies exactly which process on the destination host should receive the incoming data. Port numbers range from 0 to 65535.

**Example:** Port 80 (HTTP) or 443 (HTTPS) for web traffic, Port 25 for SMTP email, Port 53 for DNS — so a web request and an email arriving at the same IP address are correctly delivered to the browser and the email client respectively.

Together, these three levels of addressing work like a postal system: the IP address is like the city and street (getting the letter to the right building), the MAC address is like identifying the right door on the local street, and the port number is like the specific apartment/flat number inside the building (making sure it reaches the right resident/application).

#### Q16. Discuss the role of addressing in end-to-end communication.

End-to-end communication means that data originating from an application on a source host is correctly delivered to the matching application on a destination host, potentially crossing many intermediate networks and devices along the way. Addressing is what makes this precise, multi-hop delivery possible; without it, data would have no way of being routed correctly or identified at the destination.

**How addressing enables end-to-end communication**

1. Identification: Physical (MAC), logical (IP), and port addresses uniquely identify the NIC, the host, and the specific application/process respectively, so data is never ambiguous about its destination.
2. Routing across networks: Logical (IP) addressing allows routers to make forwarding decisions, choosing paths across multiple intermediate networks to move data from the source network to the destination network, even though the two hosts may never be on the same physical link.
3. Local delivery: Once data reaches the destination network, physical (MAC) addressing ensures it is delivered to the correct device on that local link (e.g., via a switch).
4. Process-level delivery: Port addressing ensures that, once data arrives at the correct host, it is handed to the correct application/process, so multiple applications can use the network simultaneously without interference.
5. Reassembly and session continuity: Combined with sequence numbers and connection tracking (e.g., in TCP), addressing allows data broken into multiple packets to be correctly reassembled and matched to the right ongoing session at the endpoints.

In essence, addressing forms a layered chain — from the local hardware link, through the global logical network, down to the specific process on the destination machine — and it is this chain that allows a message typed on one computer to travel through many intermediate routers and switches and still arrive correctly at exactly the right application on exactly the right computer, anywhere in the world.