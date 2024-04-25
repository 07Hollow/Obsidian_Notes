---
title: "3 Protocols and Models"
tags: TCP/IP, OSI-Model
date: 2024-04-24
---

> **About:** In this chapter you will learn about the protocols what are used to establish a communication between devices. In addition we will deal with the OSI model and it's layers


- [[#3.1.1 Video Devices in a bubble|3.1.1 Video Devices in a bubble]]
- [[#3.1.2 Communications Fundamentals|3.1.2 Communications Fundamentals]]
- [[#3.1.3 Communication Protocols|3.1.3 Communication Protocols]]
- [[#3.1.4 Rule Establishment|3.1.4 Rule Establishment]]
- [[#3.1.5 Network Protocols are Requirement|3.1.5 Network Protocols are Requirement]]
- [[#3.1.6 Message Encoding|3.1.6 Message Encoding]]
- [[#3.1.7 Message Formatting and Encapsulation|3.1.7 Message Formatting and Encapsulation]]
- [[#3.1.8 Message Size|3.1.8 Message Size]]
- [[#3.1.9 Message Timing|3.1.9 Message Timing]]
- [[#3.1.10 Message Delivery Options|3.1.10 Message Delivery Options]]
- [[#3.1.11 A Note About the Node Icon|3.1.11 A Note About the Node Icon]]
- [[#3.2.1 Network Protocol Overview|3.2.1 Network Protocol Overview]]
- [[#3.2.2 Network Protocol Functions|3.2.2 Network Protocol Functions]]
- [[#3.2.2 Protocol Interaction|3.2.2 Protocol Interaction]]
- [[#3.3.1 Network Protocol Suits|3.3.1 Network Protocol Suits]]
- [[#3.3.2 Evolution of Protocol Suits|3.3.2 Evolution of Protocol Suits]]
- [[#3.3.3 TCP/IP Protocol Example|3.3.3 TCP/IP Protocol Example]]
- [[#3.3.4 TCP/IP Protocol Suite|3.3.4 TCP/IP Protocol Suite]]
		- [[#Application Layer|Application Layer]]
		- [[#Transport layer|Transport layer]]
		- [[#Internet Layer|Internet Layer]]
		- [[#Network Access Layer|Network Access Layer]]
- [[#3.3.5 TCP/IP Communication Process|3.3.5 TCP/IP Communication Process]]
- [[#3.4.1 Open Standards|3.4.1 Open Standards]]
- [[#3.4.2 Internet Standards|3.4.2 Internet Standards]]
- [[#3.4.3 Electronic and Communications Standards|3.4.3 Electronic and Communications Standards]]
- [[#3.5.1 The Benefits of using a Layered Model|3.5.1 The Benefits of using a Layered Model]]
- [[#3.5.2 OSI Reference Model|3.5.2 OSI Reference Model]]
- [[#3.5.3 The TCP/IP Protocol Model|3.5.3 The TCP/IP Protocol Model]]
- [[#3.5.4 OSI and TCP/IP Model Comparison|3.5.4 OSI and TCP/IP Model Comparison]]
- [[#3.6.1 Segmenting Messages|3.6.1 Segmenting Messages]]
- [[#3.6.2 Sequencing|3.6.2 Sequencing]]
- [[#3.6.3 Protocol Data Units (PDU)|3.6.3 Protocol Data Units (PDU)]]
- [[#3.6.4 Encapsulation Example|3.6.4 Encapsulation Example]]
- [[#3.6.5 De-encapsulation Example|3.6.5 De-encapsulation Example]]
- [[#3.7.1 Addresses|3.7.1 Addresses]]
- [[#3.7.2 Layer 3 Logical Address|3.7.2 Layer 3 Logical Address]]
- [[#3.7.3 Devices on the same Network|3.7.3 Devices on the same Network]]
- [[#3.7.4 Role of the data link layer Addresses: Same IP Network|3.7.4 Role of the data link layer Addresses: Same IP Network]]
- [[#3.7.6 Role of the Network Layer Address|3.7.6 Role of the Network Layer Address]]
- [[#3.7.7 Role of the Data Link Layer Addresses: Different IP Networks|3.7.7 Role of the Data Link Layer Addresses: Different IP Networks]]
- [[#3.7.8. Data Link Access|3.7.8. Data Link Access]]

# 3.1 The Rules 

## 3.1.1 Video Devices in a bubble

Video

## 3.1.2 Communications Fundamentals

Simply having a wired or wireless physical connection between end devices is not enough to enable communication. For communication to occur, devices must know “how” to communicate.

Elements of Communication Methods: 
- **Message source (sender)** - Message sources are people, or electronic devices, that need to send a message to other individuals or devices.
- **Message Destination (receiver)** - The destination receives the message and interprets it.
- **Channel** - This consists of the media that provides the pathway over which the message travels from source to destination.

## 3.1.3 Communication Protocols 

Sending a message, whether by face-to-face communication or over a network, is governed by rules called protocols. These protocols are specific to the type of communication method being used.

## 3.1.4 Rule Establishment 

Protocols must account for the following requirements to successfully deliver a message that is understood by the receiver:

- An identified sender and receiver
- Common language and grammar
- Speed and timing of delivery
- Confirmation or acknowledgment requirements

## 3.1.5 Network Protocols are Requirement 

The protocols that are used in network communications share many of these fundamental traits. In addition to identifying the source and destination, computer and network protocols define the details of how a message is transmitted across a network. Common computer protocols include the following requirements:

- Message encoding
- Message formatting and encapsulation
- Message size
- Message timing
- Message delivery options

## 3.1.6 Message Encoding 

One of the first steps to sending a message is encoding. Encoding is the process of converting information into another acceptable form, for transmission. Decoding reverses this process to interpret the information.

## 3.1.7 Message Formatting and Encapsulation

When a message is sent from source to destination, it must use a specific format or structure. Message formats depend on the type of message and the channel that is used to deliver the message.

Internet Protocol (IP) is a protocol with a similar function to the envelope example. In the figure, the fields of the Internet Protocol version 6 (IPv6) packet identify the source of the packet and its destination. IP is responsible for sending a message from the message source to destination over one or more networks.

![[Message_Formatting_and_Encapsulation.png]]

## 3.1.8 Message Size

The rules that govern the size of the pieces, or frames, communicated across the network are very strict. They can also be different, depending on the channel used. Frames that are too long or too short are not delivered.

The size restrictions of frames require the source host to break a long message into individual pieces that meet both the minimum and maximum size requirements. The long message will be sent in separate frames, with each frame containing a piece of the original message. Each frame will also have its own addressing information. At the receiving host, the individual pieces of the message are reconstructed into the original message.

## 3.1.9 Message Timing 

Message timing includes the following:

- **Flow Control -** This is the process of managing the rate of data transmission. Flow control defines how much information can be sent and the speed at which it can be delivered. For example, if one person speaks too quickly, it may be difficult for the receiver to hear and understand the message. In network communication, there are network protocols used by the source and destination devices to negotiate and manage the flow of information.
- **Response Timeout -** If a person asks a question and does not hear a response within an acceptable amount of time, the person assumes that no answer is coming and reacts accordingly. The person may repeat the question or instead, may go on with the conversation. Hosts on the network use network protocols that specify how long to wait for responses and what action to take if a response timeout occurs.
- **Access method -** This determines when someone can send a message. Likewise, when a device wants to transmit on a wireless LAN, it is necessary for the WLAN network interface card (NIC) to determine whether the wireless medium is available.

## 3.1.10 Message Delivery Options 

Three types of data communications include:
- **Unicast** - Information is being transmitted to a single end device.
- **Multicast** - Information is being transmitted to a one or more end devices.
- **Broadcast** - Information is being transmitted to all end devices.

## 3.1.11 A Note About the Node Icon 

Nodes are typically represented as a circle.

![[A_Note_About_the_Node_Icon.png]]

# 3.2 Protocols 

## 3.2.1 Network Protocol Overview 

The table lists the various types of protocols that are needed to enable communications across one or more networks.

|**Protocol Type**|**Description**|
|---|---|
|**Network Communications Protocols**|Protocols enable two or more devices to communicate over one or more networks. The Ethernet family of technologies involves a variety of protocols such as IP, Transmission Control Protocol (TCP), HyperText Transfer Protocol (HTTP), and many more.|
|**Network Security Protocols**|Protocols secure data to provide authentication, data integrity, and data encryption. Examples of secure protocols include Secure Shell (SSH), Secure Sockets Layer (SSL), and Transport Layer Security (TLS).|
|**Routing Protocols**|Protocols enable routers to exchange route information, compare path information, and then to select the best path to the destination network. Examples of routing protocols include Open Shortest Path First (OSPF) and Border Gateway Protocol (BGP).|
|**Service Discovery Protocols**|Protocols are used for the automatic detection of devices or services. Examples of service discovery protocols include Dynamic Host Configuration Protocol (DHCP) which discovers services for IP address allocation, and Domain Name System (DNS) which is used to perform name-to-IP address translation.|

## 3.2.2 Network Protocol Functions

How does the computer send a message, across several network devices, to the server?

![[Network_Protocol_Functions.png]]

Computers and network devices use agreed-upon protocols to communicate. The table lists the functions of these protocols.

|**Function**|**Description**|
|---|---|
|**Addressing**|This identifies the sender and the intended receiver of the message using a defined addressing scheme. Examples of protocols that provide addressing include Ethernet, IPv4, and IPv6.|
|**Reliability**|This function provides guaranteed delivery mechanisms in case messages are lost or corrupted in transit. TCP provides guaranteed delivery.|
|**Flow control**|This function ensures that data flows at an efficient rate between two communicating devices. TCP provides flow control services.|
|**Sequencing**|This function uniquely labels each transmitted segment of data. The receiving device uses the sequencing information to reassemble the information correctly. This is useful if the data segments are lost, delayed or received out-of-order. TCP provides sequencing services.|
|**Error Detection**|This function is used to determine if data became corrupted during transmission. Various protocols that provide error detection include Ethernet, IPv4, IPv6, and TCP.|
|**Application Interface**|This function contains information used for process-to-process communications between network applications. For example, when accessing a web page, HTTP or HTTPS protocols are used to communicate between the client and server web processes.|

## 3.2.2 Protocol Interaction 

A message sent over a computer network typically requires the use of several protocols, each one with its own functions and format

![[Protocol_Interaction.png]]

- **Hypertext Transfer Protocol (HTTP):** Governs the way web server and web clients interact. HTTP defines the content and formatting of the request and response the are exchanged between client and server.
- **Transmission Control Protocol (TCP):** Manages individual conversation. TCP is responsible for guaranteeing the reliable delivery of the information and managing the flow control between devices.
- **Internet Protocol (IP):** Responsible for delivering messages from the sender to the receiver. IP is used by Routers to forward the messages across multiple networks.
- **Ethernet**: Responsible for the delivery of messages from one NIC to another NIC on the same Ethernet local Area Network

# 3.3 Protocol Suits

## 3.3.1 Network Protocol Suits

A protocol suite is a group of inter-related protocols necessary to perform a communication function.

A protocol stack shows how the individual protocols within a suite are implemented. The protocols are viewed in terms of layers, with each higher-level service depending on the functionality defined by the protocols shown in the lower levels. The lower layers of the stack are concerned with moving data over the network and providing services to the upper layers, which are focused on the content of the message being sent.

![[Network_Protocol_Suits.png]]

## 3.3.2 Evolution of Protocol Suits 

During the evolution of network communications and the internet there were several competing protocol suites, as shown in the figure.

![[Evolution_of_Protocol_Suites.png]]

- **Internet Protocol Suite or TCP/IP:** Most common and relevant protocol suite used today. The TCP/IP protocol suite is an open standard protocol suite maintained by the internet Engineering Task Force (IEFT). 
- **Open Systems Interconnection (OSI) protocols:** Developed by ISO and ITU. The OSI reference model categorizes the functions of its protocols. 
- **AppleTalk:** Apple tried to replace TCP/IP (didn't work)
- **Novell NetWare:** Novell adopted TCP/IP to replace IPX

## 3.3.3 TCP/IP Protocol Example 

TCP/IP protocols are available for the application, transport, and internet layers. There are no TCP/IP protocols in the network access layer. The most common network access layer LAN protocols are Ethernet and WLAN (wireless LAN) protocols. Network access layer protocols are responsible for delivering the IP packet over the physical medium.

The figure shows an example of the three TCP/IP protocols used to send packets between the web browser of a host and the web server. HTTP, TCP, and IP are the TCP/IP protocols used. At the network access layer, Ethernet is used in the example. However, this could also be a wireless standard such as WLAN or cellular service.

The figure shows the TCP/IP protocols used to send packets between the web browser of a host and a web server. A network topology shows a host connected to the Internet cloud with a connection to a Web server. An envelope representing a packet is shown flowing between the Internet and the server. Radiating from the packet is information on the protocols used at each layer. From top to bottom: application layer and hypertext transfer protocol (HTTP); transport layer and transmission control protocol (TCP); internet layer and internet protocol (IP); and network access layer and Ethernet.

![[TCP_IP_Protocol_Example.png]]

## 3.3.4 TCP/IP Protocol Suite 

![[TCP_IP_Protocol_Suite.png]]

TCP/IP is the protocol suite used by the internet and the networks of today. TCP/IP has two important aspects for vendors and manufactures:
- **Open standard protocol suite:** This means its freely available to the public and can be used by any vendor on their hardware or in their software-
- **Standards based protocol suite:** This means it has been endorsed by the networking industry and approved by a standards organization. This ensures that products from different manufactures can interoperate successfully.

#### Application Layer

Name System

- **DNS** - Domain Name System. Translates domain names such as cisco.com, into IP addresses.

Host Config

- **DHCPv4** - Dynamic Host Configuration Protocol for IPv4. A DHCPv4 server dynamically assigns IPv4 addressing information to DHCPv4 clients at start-up and allows the addresses to be re-used when no longer needed.
- **DHCPv6** - Dynamic Host Configuration Protocol for IPv6. DHCPv6 is similar to DHCPv4. A DHCPv6 server dynamically assigns IPv6 addressing information to DHCPv6 clients at start-up.
- **SLAAC** - Stateless Address Autoconfiguration. A method that allows a device to obtain its IPv6 addressing information without using a DHCPv6 server.

Email

- **SMTP** - Simple Mail Transfer Protocol. Enables clients to send email to a mail server and enables servers to send email to other servers.
- **POP3** - Post Office Protocol version 3. Enables clients to retrieve email from a mail server and download the email to the client's local mail application.
- **IMAP** - Internet Message Access Protocol. Enables clients to access email stored on a mail server as well as maintaining email on the server.

File Transfer

- **FTP** - File Transfer Protocol. Sets the rules that enable a user on one host to access and transfer files to and from another host over a network. FTP is a reliable, connection-oriented, and acknowledged file delivery protocol.
- **SFTP** - SSH File Transfer Protocol. As an extension to Secure Shell (SSH) protocol, SFTP can be used to establish a secure file transfer session in which the file transfer is encrypted. SSH is a method for secure remote login that is typically used for accessing the command line of a device.
- **TFTP** - Trivial File Transfer Protocol. A simple, connectionless file transfer protocol with best-effort, unacknowledged file delivery. It uses less overhead than FTP.

Web and Web Service

- **HTTP** - Hypertext Transfer Protocol. A set of rules for exchanging text, graphic images, sound, video, and other multimedia files on the World Wide Web.
- **HTTPS** - HTTP Secure. A secure form of HTTP that encrypts the data that is exchanged over the World Wide Web.
- **REST** - Representational State Transfer. A web service that uses application programming interfaces (APIs) and HTTP requests to create web applications.

#### Transport layer

Connection-Oriented

- **TCP** - Transmission Control Protocol. Enables reliable communication between processes running on separate hosts and provides reliable, acknowledged transmissions that confirm successful delivery.

Connectionless

- **UDP** - User Datagram Protocol. Enables a process running on one host to send packets to a process running on another host. However, UDP does not confirm successful datagram transmission.

#### Internet Layer

Internet Protocol

- **IPv4** - Internet Protocol version 4. Receives message segments from the transport layer, packages messages into packets, and addresses packets for end-to-end delivery over a network. IPv4 uses a 32-bit address.
- **IPv6** - IP version 6. Similar to IPv4 but uses a 128-bit address.
- **NAT** - Network Address Translation. Translates IPv4 addresses from a private network into globally unique public IPv4 addresses.

Messaging

- **ICMPv4** - Internet Control Message Protocol for IPv4. Provides feedback from a destination host to a source host about errors in packet delivery.
- **ICMPv6** - ICMP for IPv6. Similar functionality to ICMPv4 but is used for IPv6 packets.
- **ICMPv6 ND** - ICMPv6 Neighbor Discovery. Includes four protocol messages that are used for address resolution and duplicate address detection.

Routing Protocols

- **OSPF** - Open Shortest Path First. Link-state routing protocol that uses a hierarchical design based on areas. OSPF is an open standard interior routing protocol.
- **EIGRP** - EIGRP - Enhanced Interior Gateway Routing Protocol. An open standard routing protocol developed by Cisco that uses a composite metric based on bandwidth, delay, load and reliability.
- **BGP** - Border Gateway Protocol. An open standard exterior gateway routing protocol used between Internet Service Providers (ISPs). BGP is also commonly used between ISPs and their large private clients to exchange routing information.

#### Network Access Layer

Address Resolution

- **ARP** - Address Resolution Protocol. Provides dynamic address mapping between an IPv4 address and a hardware address.
    
    **Note**: You may see other documentation state that ARP operates at the Internet Layer (OSI Layer 3). However, in this course we state that ARP operates at the Network Access layer (OSI Layer 2) because it's primary purpose is the discover the MAC address of the destination. A MAC address is a Layer 2 address.
    

Data Link Protocols

- **Ethernet** - Defines the rules for wiring and signaling standards of the network access layer.
- **WLAN** - Wireless Local Area Network. Defines the rules for wireless signaling across the 2.4 GHz and 5 GHz radio frequencies.

## 3.3.5 TCP/IP Communication Process 

Video 

# 3.4 Standards Organizations 

## 3.4.1 Open Standards

Standards Organizations are:
- IEEE
- IETF
- iana (Internet Assigned Numbers Authority)
- ICANN
- ITU
- TIA

## 3.4.2 Internet Standards 

Various organizations have different responsibilities for promoting and creating standards for the internet and TCP/IP protocol.

The figure displays standards organizations involved with the development and support of the internet.

![[Internet_Standards.png]]

**Internet Society (ISCO):** Responsible for promoting the open development and evolution of internet use throughout the world.
**Internet Architecture Board (IAB):** Responsible for the overall management and development of internet standards.
**Internet Engineering Task Force (IETF):** Develops, updates, and maintains internet and TCP/IP technologies. 
**Internet Research Task Force (IRTF):** Focused on long-term research related to internet and TCP/IP protocols such as Anti-Spam Research Group (ASRG), CFRG, P2PRG.

The next figure displays standards organizations involved with the development and support of TCP/IP and include IANA and ICANN.

![[Internet_Standards 1.png]]

- **Internet Corporation for Assigned Names and Numbers (ICANN):** ICANN coordinates IP address allocation, the management of domain names, and assignment of other information used in TCP/IP protocols. 
- **Internet Assigned Numbers Authority:** Responsible for overseeing an managing IP address allocation, domain name management, and protocol identifiers for ICANN. 

## 3.4.3 Electronic and Communications Standards

Other standards organizations have responsibilities for promoting and creating the electronic and communication standards used to deliver the IP packets as electronic signals over a wired or wireless medium.

These standard organizations include the following:

- **Institute of Electrical and Electronics Engineers** (**IEEE**, pronounced “I-triple-E”) - Organization of electrical engineering and electronics dedicated to advancing technological innovation and creating standards in a wide area of industries including power and energy, healthcare, telecommunications, and networking. Important IEEE networking standards include 802.3 Ethernet and 802.11 WLAN standard. Search the internet for other IEEE network standards.
- **Electronic Industries Alliance (EIA)** - Organization is best known for its standards relating to electrical wiring, connectors, and the 19-inch racks used to mount networking equipment.
- **Telecommunications Industry Association (TIA)** - Organization responsible for developing communication standards in a variety of areas including radio equipment, cellular towers, Voice over IP (VoIP) devices, satellite communications, and more.
- **International Telecommunications Union-Telecommunication Standardization Sector (ITU-T)** - One of the largest and oldest communication standards organizations. The ITU-T defines standards for video compression, Internet Protocol Television (IPTV), and broadband communications, such as a digital subscriber line (DSL).

# 3.5 Reference Models

## 3.5.1 The Benefits of using a Layered Model 

These are the benefits of using a layered model to describe network protocols and operations:

- Assisting in protocol design because protocols that operate at a specific layer have defined information that they act upon and a defined interface to the layers above and below
- Fostering competition because products from different vendors can work together
- Preventing technology or capability changes in one layer from affecting other layers above and below
- Providing a common language to describe networking functions and capabilities

As shown in the figure, there are two layered models that are used to describe network operations:

- Open System Interconnection (OSI) Reference Model
- TCP/IP Reference Model

![[The_Benefits_of_using_a_Layered_Model.png]]

## 3.5.2 OSI Reference Model

|**OSI Model Layer**|**Description**|
|---|---|
|**7 - Application**|The application layer contains protocols used for process-to-process communications.|
|**6 - Presentation**|The presentation layer provides for common representation of the data transferred between application layer services.|
|**5 - Session**|The session layer provides services to the presentation layer to organize its dialogue and to manage data exchange.|
|**4 - Transport**|The transport layer defines services to segment, transfer, and reassemble the data for individual communications between the end devices.|
|**3 - Network**|The network layer provides services to exchange the individual pieces of data over the network between identified end devices.|
|**2 - Data Link**|The data link layer protocols describe methods for exchanging data frames between devices over a common media|
|**1 - Physical**|The physical layer protocols describe the mechanical, electrical, functional, and procedural means to activate, maintain, and de-activate physical connections for a bit transmission to and from a network device.|

**Note**: Whereas the TCP/IP model layers are referred to only by name, the seven OSI model layers are more often referred to by number rather than by name. For instance, the physical layer is referred to as Layer 1 of the OSI model, data link layer is Layer2, and so on.

## 3.5.3 The TCP/IP Protocol Model 

|**TCP/IP Model Layer**|**Description**|
|---|---|
|**4 - Application**|Represents data to the user, plus encoding and dialog control.|
|**3 - Transport**|Supports communication between various devices across diverse networks.|
|**2 - Internet**|Determines the best path through the network.|
|**1 - Network Access**|Controls the hardware devices and media that make up the network.|

The definitions of the standard and the TCP/IP protocols are discussed in a public forum and defined in a publicly available set of IETF RFCs. An RFC is authored by networking engineers and sent to other IETF members for comments.

## 3.5.4 OSI and TCP/IP Model Comparison 

The protocols that make up the TCP/IP protocol suite can also be described in terms of the OSI reference model. In the OSI model, the network access layer and the application layer of the TCP/IP model are further divided to describe discrete functions that must occur at these layers.

At the network access layer, the TCP/IP protocol suite does not specify which protocols to use when transmitting over a physical medium; it only describes the handoff from the internet layer to the physical network protocols. OSI Layers 1 and 2 discuss the necessary procedures to access the media and the physical means to send data over a network.

![[OSI_and_TCP_IP_Model_Comparison.png]]

- **OSI Layer 3:** Maps directly to the TCP/IP internet layer. This layer is used to describes protocols that address and route messages through the network.
- **OSI Layer 4:** Maps directly to the TCP/IP transport layer. This layer describes general services and functions that provide ordered and reliable delivery of data between source and destination host
- The TCP/IP application layer includes several protocols that provide specific functionality to a variety of end user application. 
- Both the TCP/IP and OSI model are commonly used when referring to protocols at various layers. Because the OSI model separates the data link layer from the physical layer. 

# 3.6 Data Encapsulation 

## 3.6.1 Segmenting Messages 

In theory, a single communication, such as a video or an email message with many large attachments, could be sent across a network from a source to a destination as one massive, uninterrupted stream of bits. However, this would create problems for other devices needing to use the same communication channels or links.

A better approach is to divide the data into smaller, more manageable pieces to send over the network. Segmentation is the process of dividing a stream of data into smaller units for transmissions over the network. Segmentation is necessary because data networks use the TCP/IP protocol suite send data in individual IP packets. Each packet is sent separately, similar to sending a long letter as a series of individual postcards. Packets containing segments for the same destination can be sent over different paths.

This leads to segmenting messages having two primary benefits:

- **Increases speed** - Because a large data stream is segmented into packets, large amounts of data can be sent over the network without tying up a communications link. This allows many different conversations to be interleaved on the network called multiplexing.
- **Increases efficiency** -If a single segment is fails to reach its destination due to a failure in the network or network congestion, only that segment needs to be retransmitted instead of resending the entire data stream.

## 3.6.2 Sequencing 

![[Sequencing.png]]

## 3.6.3 Protocol Data Units (PDU)

**Note**: Although the UDP PDU is called datagram, IP packets are sometimes also referred to as IP datagrams.
The form that a piece of data takes at any layer is called a protocol data unit (PDU). 
During encapsulation, each succeeding layer encapsulates the PDU that it receives from the layer above in accordance with the protocol being used. At each stage of the process, a PDU has a different name to reflect its new functions. Although there is no universal naming convention for PDUs, in this course, the PDUs are named according to the protocols of the TCP/IP suite. The PDUs for each form of data are shown in the figure.

![[Protocol_Data_Units.png]]

- **Data:** The general term for the PDU used at the application layer 
- **Segment:** Transport layer PDU
- **Packet:** Network layer PDU 
- **Frame:** Data link layer PDU
- **Bits:** Physical layer PDU used when physically transmitting data over the medium

**Note:** If the Transport header is TCP, then a segment. If the Transport header is UDP then it is a datagram. 
## 3.6.4 Encapsulation Example 

Video

## 3.6.5 De-encapsulation Example

Video

# 3.7 Data Access

## 3.7.1 Addresses

The network and data link layers are responsible for delivering the data from the source device to the destination device. As shown in the figure, protocols at both layers contain a source and destination address, but their addresses have different purposes:

- **Network layer source and destination addresses** - Responsible for delivering the IP packet from the original source to the final destination, which may be on the same network or a remote network.
- **Data link layer source and destination addresses** - Responsible for delivering the data link frame from one network interface card (NIC) to another NIC on the same network.

![[Addresses.png]]

## 3.7.2 Layer 3 Logical Address

An IP address is the network layer, or Layer 3, logical address used to deliver the IP packet from the original source to the final destination, as shown in the figure.

The IP packet contains two IP addresses:

- **Source IP address** - The IP address of the sending device, which is the original source of the packet.
- **Destination IP address** - The IP address of the receiving device, which is the final destination of the packet.

An IP address contains two parts:

- **Network portion (IPv4) or Prefix (IPv6)** - The left-most part of the address that indicates the network in which the IP address is a member. All devices on the same network will have the same network portion of the address.
- **Host portion (IPv4) or Interface ID (IPv6)** - The remaining part of the address that identifies a specific device on the network. This portion is unique for each device or interface on the network.

**Note**: The subnet mask (IPv4) or prefix-length (IPv6) is used to identify the network portion of an IP address from the host portion.

## 3.7.3 Devices on the same Network                                                                     

In this example we have a client computer, PC1, communicating with an FTP server on the same IP network.

- **Source IPv4 address** - The IPv4 address of the sending device, the client computer PC1: 192.168.1.110.
- **Destination IPv4 address** - The IPv4 address of the receiving device, FTP server: 192.168.1.9.

![[Devices_on_the_same_Network.png]]


## 3.7.4 Role of the data link layer Addresses: Same IP Network

When the sender and receiver of the IP packet are on the same network, the data link frame is sent directly to the receiving device. On an Ethernet network, the data link addresses are known as Ethernet Media Access Control (MAC) addresses.

MAC addresses are physically embedded on the Ethernet NIC.

- **Source MAC address** - This is the data link address, or the Ethernet MAC address, of the device that sends the data link frame with the encapsulated IP packet. The MAC address of the Ethernet NIC of PC1 is AA-AA-AA-AA-AA-AA, written in hexadecimal notation.
- **Destination MAC address** - When the receiving device is on the same network as the sending device, this is the data link address of the receiving device. In this example, the destination MAC address is the MAC address of the FTP server: CC-CC-CC-CC-CC-CC, written in hexadecimal notation.

The frame with the encapsulated IP packet can now be transmitted from PC1 directly to the FTP server.

## 3.7.6 Role of the Network Layer Address

When the sender of the packet is on a different network from the receiver, the source and destination IP addresses will represent hosts on different networks. This will be indicated by the network portion of the IP address of the destination host.

- **Source IPv4 address** - The IPv4 address of the sending device, the client computer PC1: 192.168.1.110.
- **Destination IPv4 address** - The IPv4 address of the receiving device, the server, Web Server: 172.16.1.99.

## 3.7.7 Role of the Data Link Layer Addresses: Different IP Networks

When the sender and receiver of the IP packet are on different networks, the Ethernet data link frame cannot be sent directly to the destination host because the host is not directly reachable in the network of the sender. The Ethernet frame must be sent to another device known as the router or default gateway. In our example, the default gateway is R1. R1 has an Ethernet data link address that is on the same network as PC1. This allows PC1 to reach the router directly 

- **Source MAC address** - The Ethernet MAC address of the sending device, PC1. The MAC address of the Ethernet interface of PC1 is AA-AA-AA-AA-AA-AA.
- **Destination MAC address** - When the receiving device, the destination IP address, is on a different network from the sending device, the sending device uses the Ethernet MAC address of the default gateway or router. In this example, the destination MAC address is the MAC address of the R1 Ethernet interface, 11-11-11-11-11-11. This is the interface that is attached to the same network as PC1, as shown in the figure.

![[Role_of_the_Data_Link_Layer_Addresses_Different_IP_Networks.png]]

The Ethernet frame with the encapsulated IP packet can now be transmitted to R1. R1 forwards the packet to the destination, Web Server. This may mean that R1 forwards the packet to another router or directly to Web Server if the destination is on a network connected to R1.

It is important that the IP address of the default gateway be configured on each host on the local network. All packets to a destination on remote networks are sent to the default gateway. Ethernet MAC addresses and the default gateway are discussed in more detail in other modules.

## 3.7.8. Data Link Access 

The data link Layer 2 physical address has a different role. The purpose of the data link address is to deliver the data link frame from one network interface to another network interface on the same network.

Before an IP packet can be sent over a wired or wireless network, it must be encapsulated in a data link frame, so it can be transmitted over the physical medium.

The Layer 2, data link protocol is only used to deliver the packet from NIC-to-NIC on the same network. The router removes the Layer 2 information as it is received on one NIC and adds new data link information before forwarding out the exit NIC on its way towards the final destination.

The IP packet is encapsulated in a data link frame that contains the following data link information:

- **Source data link address** - The physical address of the NIC that is sending the data link frame.
- **Destination data link address** - The physical address of the NIC that is receiving the data link frame. This address is either the next hop router or the address of the final destination device.
