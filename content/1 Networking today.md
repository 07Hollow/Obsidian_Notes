---
title: "1 Networking today"
tags: empty
date: YYYY-MM-DD
---

> **About:** Introduction to the CCNA


- [[#1.1.1 Network connect us|1.1.1 Network connect us]]
- [[#1.1.2 video|1.1.2 video]]
- [[#1.1.3 Nou boundaries|1.1.3 Nou boundaries]]
- [[#1.2.1 Host Roles|1.2.1 Host Roles]]
- [[#1.2.2 Peer-to-Peer|1.2.2 Peer-to-Peer]]
- [[#1.2.3 End devices|1.2.3 End devices]]
- [[#1.2.4 Intermediary Devices|1.2.4 Intermediary Devices]]
- [[#1.2.5 Network media|1.2.5 Network media]]
	- [[#1.2.5 Network media#1.3.1 Network representations|1.3.1 Network representations]]
	- [[#1.2.5 Network media#1.3.2 Topology Diagramms|1.3.2 Topology Diagramms]]
- [[#1.4.1 Networks of Many Sizes|1.4.1 Networks of Many Sizes]]
- [[#1.4.2 LANs and WANs|1.4.2 LANs and WANs]]
- [[#1.4.3 Internet|1.4.3 Internet]]
- [[#1.4.4 Intranet and Extranet|1.4.4 Intranet and Extranet]]
- [[#1.5.1 Internet Access Technologies|1.5.1 Internet Access Technologies]]
- [[#1.5.2 Home and Small Access Office Internet Connections|1.5.2 Home and Small Access Office Internet Connections]]
- [[#1.5.3 Businesses Internet Connnections|1.5.3 Businesses Internet Connnections]]
- [[#1.5.4 The Converging Network|1.5.4 The Converging Network]]
- [[#1.6.1 Reliable Networks|1.6.1 Reliable Networks]]
- [[#1.6.2 Fault Tolerance|1.6.2 Fault Tolerance]]
- [[#1.6.3 Scalability|1.6.3 Scalability]]
- [[#1.6.4 Quality of Service (QoS)|1.6.4 Quality of Service (QoS)]]
- [[#1.6.5 Network Security|1.6.5 Network Security]]
- [[#1.7.1 Recent Trends|1.7.1 Recent Trends]]
- [[#1.7.2 Bring your own Device (BYOD)|1.7.2 Bring your own Device (BYOD)]]
- [[#1.7.3 Online Collaboration|1.7.3 Online Collaboration]]
- [[#1.7.4 Video Communication|1.7.4 Video Communication]]
- [[#1.7.5 ## Video - Cisco Webex for Huddles|1.7.5 ## Video - Cisco Webex for Huddles]]
- [[#1.7.6 Cloud Computing|1.7.6 Cloud Computing]]
	- [[#1.7.6 Cloud Computing#Cloud Types|Cloud Types]]
- [[#1.7.7 Technology Trends in the Home|1.7.7 Technology Trends in the Home]]
- [[#1.7.8 Powerline Network|1.7.8 Powerline Network]]
- [[#1.7.9 Wireless Broadband|1.7.9 Wireless Broadband]]
- [[#1.8.1 Security Threats|1.8.1 Security Threats]]
- [[#1.8.2 Security Solutions|1.8.2 Security Solutions]]


# 1.1 Networks affect our lives
## 1.1.1 Network connect us
- Among all of the essentials for human existence, the need to interact with others ranks just below our need to sustain life
- Communication is almost as important to us as our reliance on air, water, food, and shelter
- through the use of networks, we are connected like never before
## 1.1.2 video
skip

## 1.1.3 Nou boundaries 
- Advancements in networking technologies are perhaps the most significant changes in the world today
- national borders, geographic distances, and physical limitations become less relevant
- cloud lets us store documents and pictures and access them anywhere, anytime
- Global communities allow for social interaction that is independent of location or time zone

# 1.2 Network components 
## 1.2.1 Host Roles
- If you want to be a part of a global online community, your computer, tablet, or smart phone must first be connected to a network
- network must be connected to the internet
- All computers that are connected to a network and participate directly in network communication are classified as hosts
	- Host can be devices or clients
	- hosts specifically refers to devices on the network that are assigned a number for communication purposes
		- This number identifies the host within a particular network
			- this number is called IP (Internet Protocol)
				- IP address identifies the host and the network to which the host is attached.
- Servers are computers with software that allow them to provide information, like email or web pages, to other end devices on the network
	-  Each service requires separate server software
- Clients have software for requesting and displaying the information obtained from the server

|Type|Description|
|---|---|
|Email|The email server runs email server software. Clients use mail client software, such as Microsoft Outlook, to access email on the server.|
|Web|The web server runs web server software. Clients use browser software, such as Windows Internet Explorer, to access web pages on the server.|
|File|The file server stores corporate and user files in a central location. The client devices access these files with client software such as the Windows File Explorer.|

## 1.2.2 Peer-to-Peer
- Client and server software usually run on separate computers, but it is also possible for one computer to be used for both roles at the same time
	- This is called Peer-to-Peer
- Advantages:
	- easy to setup
	- less complex
	- lower cost
- disadvantages:
	- not as secure
	- not scalable 
	- no centralized administration
## 1.2.3 End devices 
- When an end device initiates communication, it uses the address of the destination end device to specify where to deliver the message.
- An end device is either the source or destination of a message transmitted over the network

## 1.2.4 Intermediary Devices
- They can connect multiple individual networks to form an internetwork
- These intermediary devices provide connectivity and ensure that data flows across the network
- Intermediary devices use the destination end device address, in conjunction with information about the network interconnections, to determine the path that messages should take through the network. Examples of the more common intermediary devices and a list of functions are shown in the figure.

![[intermediary_devices.png]]

here are some functions:
- regenerate and retransmit communication signals 
- maintain information about what pathway exist through the network and interwork 
- notify other devices of error and communications failure 
- direct data along alternate pathways when there is link failure 
- classify and direct messages according to priorities 
- permit or deny the flow of data, based security settings
All Intermediary Devices perform the function of a repeater 

## 1.2.5 Network media 

Modern networks primarily use three types of media to interconnect devices:

- **Metal wires within cables** - Data is encoded into electrical impulses.
- **Glass or plastic fibers within cables (fiber-optic cable)** - Data is encoded into pulses of light.
- **Wireless transmission** - Data is encoded via modulation of specific frequencies of electromagnetic waves.

Four main criteria for choosing a network media: 
- max. distance carry a signal
- environment in which the media will bei installed 
- amount of data and at what speed must be transmitted
- cost of media installation 

# 1.3 Network Representations and Topologies
### 1.3.1 Network representations 
- show what their networks will look like
- easily see which components connect to other components
- A diagram provides an easy way to understand how devices connect in a large network. This type of “picture” of a network is known as a topology diagram.

In addition to these representations, specialized terminology is used to describe how each of these devices and media connect to each other:

- **Network Interface Card (NIC)** - A NIC physically connects the end device to the network.
- **Physical Port** - A connector or outlet on a networking device where the media connects to an end device or another networking device.
- **Interface** - Specialized ports on a networking device that connect to individual networks. Because routers connect networks, the ports on a router are referred to as network interfaces.

### 1.3.2 Topology Diagramms
**Physical Topology Diagrams**
-  illustrate the physical location of intermediary devices and cable installation, as shown in the figure. You can see that the rooms in which these devices are located are labeled in this physical topology

![[Physical_Topology_Diagrams.png]]

**Logical Topology Diagrams**
- illustrate devices, ports, and the addressing scheme of the network, as shown in the figure. You can see which end devices are connected to which intermediary devices and what media is being used

![[Logical_Topology_Diagrams.png]]


# 1.4 Common types of Networks

## 1.4.1 Networks of Many Sizes

- Simple home networks let you share resources, such as printers, documents, pictures, and music, among a few local end devices.
- Small office and home office (SOHO) networks allow people to work from home, or a remote office. Many self-employed workers use these types of networks to advertise and sell products, order supplies, and communicate with customers.
- Businesses and large organizations use networks to provide consolidation, storage, and access to information on network servers.
- The internet is the largest network in existence. In fact it means "network of networks"
- In small businesses and homes, many computers function as both the servers and clients on the network. This type of network is called a peer-to-peer network.

## 1.4.2 LANs and WANs

Network infrastructures vary greatly in terms of:
- Size of the area covered
- Number of users connected
- Number and types of services available
- Area of responsibility

most common types of network infrastructures are Local Area Networks (LANs), and Wide Area Networks (WANs).
- LAN: network infrastructure that provides access to users and end devices in a small geographical area
- network infrastructure that provides access to other networks over a wide geographical area, which is typically owned and managed by a larger corporation or a telecommunications service provider

A LAN is a network infrastructure that spans a small geographical area. LANs have specific characteristics:
- LANs interconnect end devices in a limited area such as a home, school, office building, or campus.
- A LAN is usually administered by a single organization or individual. Administrative control is enforced at the network level and governs the security and access control policies.
- LANs provide high-speed bandwidth to internal end devices and intermediary devices, as shown in the figure.

WANs are typically managed by service providers (SPs) or Internet Service Providers (ISPs).
WANs have specific characteristics:
- WANs interconnect LANs over wide geographical areas such as between cities, states, provinces, countries, or continents.
- WANs are usually administered by multiple service providers.
- WANs typically provide slower speed links between LANs.

## 1.4.3 Internet

- worldwide collection of interconnected networks (internetworks)
- Some of the LAN examples are connected to each other through a WAN connection
- WANs can connect through copper wires, fiber-optic cables, and wireless transmissions (not shown)

## 1.4.4 Intranet and Extranet

Intranet: private connection of LANs and WANs that belongs to an organization. An intranet is designed to be accessible only by the organization's members, employees, or others with authorization

Extranet:  provide secure and safe access to individuals who work for a different organization but require access to the organization’s data

# 1.5 Internet Connections

## 1.5.1 Internet Access Technologies

Home users, remote workers, and small offices typically require a connection to an ISP to access the internet. Connection options vary greatly between ISPs and geographical locations. However, popular choices include broadband cable, broadband digital subscriber line (DSL), wireless WANs, and mobile services.

SPs offer business-class interconnections. Popular business-class services include business DSL, leased lines, and Metro Ethernet.


## 1.5.2 Home and Small Access Office Internet Connections


![[Connection_small_offic_and_home_office.png]]

- **Cable** - Typically offered by cable television service providers, the internet data signal transmits on the same cable that delivers cable television. It provides a high bandwidth, high availability, and an always-on connection to the internet.
- **DSL** - Digital Subscriber Lines also provide high bandwidth, high availability, and an always-on connection to the internet. DSL runs over a telephone line. In general, small office and home office users connect using Asymmetrical DSL (ADSL), which means that the download speed is faster than the upload speed.
- **Cellular** - Cellular internet access uses a cell phone network to connect. Wherever you can get a cellular signal, you can get cellular internet access. Performance is limited by the capabilities of the phone and the cell tower to which it is connected.
- **Satellite** - The availability of satellite internet access is a benefit in those areas that would otherwise have no internet connectivity at all. Satellite dishes require a clear line of sight to the satellite.
- **Dial-up Telephone** - An inexpensive option that uses any phone line and a modem. The low bandwidth provided by a dial-up modem connection is not sufficient for large data transfer, although it is useful for mobile access while traveling.

The choice of connection varies depending on geographical location and service provider availability.

## 1.5.3 Businesses Internet Connnections

Corporate connection options differ from home user options. Businesses may require higher bandwidth, dedicated bandwidth, and managed services. Connection options that are available differ depending on the type of service providers located nearby.

The figure illustrates common connection options for businesses.

![[common_connection_options_for_businesses.png]]

- **Dedicated Leased Line** - Leased lines are reserved circuits within the service provider’s network that connect geographically separated offices for private voice and/or data networking. The circuits are rented at a monthly or yearly rate.
- **Metro Ethernet** - This is sometimes known as Ethernet WAN. In this module, we will refer to it as Metro Ethernet. Metro ethernets extend LAN access technology into the WAN. Ethernet is a LAN technology you will learn about in a later module.
- **Business DSL** - Business DSL is available in various formats. A popular choice is Symmetric Digital Subscriber Line (SDSL) which is similar to the consumer version of DSL but provides uploads and downloads at the same high speeds.
- **Satellite** - Satellite service can provide a connection when a wired solution is not available.

The choice of connection varies depending on geographical location and service provider availability.

## 1.5.4 The Converging Network

**Traditional Separate Networks**
separate networks could not communicate with each other. Each network used different technologies to carry the communication signal. Each network had its own set of rules and standards to ensure successful communication. Multiple services ran on multiple networks.

![[Traditional_Separate_Networks.png]]

**Converged Networks**
Today, the separate data, telephone, and video networks converge. Unlike dedicated networks, converged networks are capable of delivering data, voice, and video between many different types of devices over the same network infrastructure. This network infrastructure uses the same set of rules, agreements, and implementation standards. Converged data networks carry multiple services on one network.

![[Converged_Networks.png]]

# 1.6 Network Architecture 

## 1.6.1 Reliable Networks

The role of the network has changed from a data-only network to a system that enables the connections of people, devices, and information in a media-rich, converged network environment. For networks to function efficiently and grow in this type of environment, the network must be built upon a standard network architecture.

Networks also support a wide range of applications and services. They must operate over many different types of cables and devices, which make up the physical infrastructure. The term network architecture, in this context, refers to the technologies that support the infrastructure and the programmed services and rules, or protocols, that move data across the network.

As networks evolve, we have learned that there are four basic characteristics that network architects must address to meet user expectations:

- Fault Tolerance
- Scalability
- Quality of Service (QoS)
- Security

## 1.6.2 Fault Tolerance

A fault tolerant network is one that limits the number of affected devices during a failure. It is built to allow quick recovery when such a failure occurs. These networks depend on multiple paths between the source and destination of a message. If one path fails, the messages are instantly sent over a different link. Having multiple paths to a destination is known as redundancy.

Implementing a packet-switched network is one way that reliable networks provide redundancy. Packet switching splits traffic into packets that are routed over a shared network. A single message, such as an email or a video stream, is broken into multiple message blocks, called packets. Each packet has the necessary addressing information of the source and destination of the message. The routers within the network switch the packets based on the condition of the network at that moment. This means that all the packets in a single message could take very different paths to the same destination. In the figure, the user is unaware and unaffected by the router that is dynamically changing the route when a link fails.

![[Fault_Tolerance.png]]

## 1.6.3 Scalability

A scalable network expands quickly to support new users and applications. It does this without degrading the performance of services that are being accessed by existing users.

![[scalability.png]]

## 1.6.4 Quality of Service (QoS)

Quality of Service (QoS) is an increasing requirement of networks today. New applications available to users over networks, such as voice and live video transmissions, create higher expectations for the quality of the delivered services.
As data, voice, and video content continue to converge onto the same network, QoS becomes a primary mechanism for managing congestion and ensuring reliable delivery of content to all users.
Congestion occurs when the demand for bandwidth exceeds the amount available. Network bandwidth is measured in the number of bits that can be transmitted in a single second, or bits per second (bps). When simultaneous communications are attempted across the network, the demand for network bandwidth can exceed its availability, creating network congestion.
When the volume of traffic is greater than what can be transported across the network, devices will hold the packets in memory until resources become available to transmit them.
With a QoS policy in place, the router can manage the flow of data and voice traffic, giving priority to voice communications if the network experiences congestion.The focus of QoS is to prioritize time-sensitive traffic. The type of traffic, not the content of the traffic, is what is important.

## 1.6.5 Network Security 

Network administrators must address two types of network security concerns: network infrastructure security and information security.

Securing the network infrastructure includes physically securing devices that provide network connectivity and preventing unauthorized access to the management software that resides on them.

![[Network_Security.png]]

Network administrators must also protect the information contained within the packets being transmitted over the network, and the information stored on network attached devices. In order to achieve the goals of network security, there are three primary requirements.

- **Confidentiality** - Data confidentiality means that only the intended and authorized recipients can access and read data.
- **Integrity** - Data integrity assures users that the information has not been altered in transmission, from origin to destination.
- **Availability** - Data availability assures users of timely and reliable access to data services for authorized users.


# 1.7 Network Trends

## 1.7.1 Recent Trends

There are several networking trends that affect organizations and consumers:

- Bring Your Own Device (BYOD)
- Online collaboration
- Video communications
- Cloud Computing
## 1.7.2 Bring your own Device (BYOD)

concept of any device, for any content, in any manner
BYOD means any device, with any ownership, used anywhere.
## 1.7.3 Online Collaboration

Collaboration is defined as “the act of working with another or others on a joint project.” With Tools like WebEx, Teams and more

## 1.7.4 Video Communication 

Video is used for communications, collaboration, and entertainment.
locally and globally

## 1.7.5 Video - Cisco Webex for Huddles

Video

## 1.7.6 Cloud Computing

access and store data
Applications such as word processing and photo editing can be accessed using the cloud.
For businesses, Cloud computing extends the capabilities of IT without requiring investment in new infrastructure, training new personnel, or licensing new software. These services are available on-demand and delivered economically to any device that is anywhere in the world without compromising security or function.
Cloud computing is possible because of data centers. Data centers are facilities used to house computer systems and associated components. A data center can occupy one room of a building, one or more floors, or an entire warehouse-sized building. Data centers are typically very expensive to build and maintain.
reduce the overall cost of ownership by leasing server and storage services from a larger data center organization in the cloud.
For security, reliability, and fault tolerance, cloud providers often store data in distributed data centers. Instead of storing all the data of a person or an organization in one data center, it is stored in multiple data centers in different locations.

There are four primary types of clouds: Public clouds, Private clouds, Hybrid clouds, and Community clouds, as shown in the table.
### Cloud Types

|Cloud Type|Description|
|---|---|
|**Public clouds**|Cloud-based applications and services offered in a public cloud are made available to the general population. Services may be free or are offered on a pay-per-use model, such as paying for online storage. The public cloud uses the internet to provide services.|
|**Private clouds**|Cloud-based applications and services offered in a private cloud are intended for a specific organization or entity, such as a government. A private cloud can be set up using the organization’s private network, though this can be expensive to build and maintain. A private cloud can also be managed by an outside organization with strict access security.|
|**Hybrid clouds**|A hybrid cloud is made up of two or more clouds (example: part private, part public), where each part remains a distinct object, but both are connected using a single architecture. Individuals on a hybrid cloud would be able to have degrees of access to various services based on user access rights.|
|**Community clouds**|A community cloud is created for exclusive use by specific entities or organizations. The differences between public clouds and community clouds are the functional needs that have been customized for the community. For example, healthcare organizations must remain compliant with policies and laws (e.g., HIPAA) that require special authentication and confidentiality. Community clouds are used by multiple organizations that have similar needs and concerns. Community clouds are similar to a public cloud environment, but with set levels of security, privacy, and even regulatory compliance of a private cloud.|

## 1.7.7 Technology Trends in the Home

newest home trends include ‘smart home technology’

![[Smart_home.png]]

## 1.7.8 Powerline Network 

Powerline networking for home networks uses existing electrical wiring to connect devices, as shown in the figure.

![[Powerline_Network.png]]

No data cables need to be installed, and there is little to no additional electricity used. Using the same wiring that delivers electricity, powerline networking sends information by sending data on certain frequencies.
Powerline networking is especially useful when wireless access points cannot reach all the devices in the home. Powerline networking is not a substitute for dedicated cabling in data networks. However, it is an alternative when data network cables or wireless communications are not possible or effective.

## 1.7.9 Wireless Broadband

In many areas where cable and DSL are not available, wireless may be used to connect to the internet.

**Wireless Internet Service Provider**
A Wireless Internet Service Provider (WISP) is an ISP that connects subscribers to a designated access point or hot spot using similar wireless technologies found in home wireless local area networks (WLANs). WISPs are more commonly found in rural environments where DSL or cable services are not available.
Although a separate transmission tower may be installed for the antenna, typically the antenna is attached to an existing elevated structure, such as a water tower or a radio tower. A small dish or antenna is installed on the subscriber’s roof in range of the WISP transmitter. The subscriber’s access unit is connected to the wired network inside the home. From the perspective of the home user, the setup is not much different than DSL or cable service. The main difference is that the connection from the home to the ISP is wireless instead of a physical cable.

**Wireless Broadband Service**

![[Wireless_Broadband_Service.png]]

 Same cellular technology as a smart phone. An antenna is installed outside the house providing either wireless or wired connectivity for devices in the home. In many areas, home wireless broadband is competing directly with DSL and cable services.

# 1.8 Network Security 

## 1.8.1 Security Threats 

There are several common external threats to networks:

- **Viruses, worms, and Trojan horses** - These contain malicious software or code running on a user device.
- **Spyware and adware** - These are types of software which are installed on a user’s device. The software then secretly collects information about the user.
- **Zero-day attacks** - Also called zero-hour attacks, these occur on the first day that a vulnerability becomes known.
- **Threat actor attacks** - A malicious person attacks user devices or network resources.
- **Denial of service attacks** - These attacks slow or crash applications and processes on a network device.
- **Data interception and theft** - This attack captures private information from an organization’s network.
- **Identity theft** - This attack steals the login credentials of a user in order to access private data.

## 1.8.2 Security Solutions 

These are the basic security components for a home or small office network:

- **Antivirus and antispyware** - These applications help to protect end devices from becoming infected with malicious software.
- **Firewall filtering** - Firewall filtering blocks unauthorized access into and out of the network. This may include a host-based firewall system that prevents unauthorized access to the end device, or a basic filtering service on the home router to prevent unauthorized access from the outside world into the network.

Larger networks and corporate networks use antivirus, antispyware, and firewall filtering, but they also have other security requirements:

- **Dedicated firewall systems** - These provide more advanced firewall capabilities that can filter large amounts of traffic with more granularity.
- **Access control lists (ACL)** - These further filter access and traffic forwarding based on IP addresses and applications.
- **Intrusion prevention systems (IPS)** - These identify fast-spreading threats, such as zero-day or zero-hour attacks.
- **Virtual private networks (VPN)** - These provide secure access into an organization for remote workers.
