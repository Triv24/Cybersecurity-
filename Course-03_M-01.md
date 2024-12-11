## Network components, devices, and diagrams :

### Network devices : 
- Network devices maintain information and services for users of a network.
- These devices connect over wired and wireless connections.
- After establishing a connection to the network, the devices send data packets.
- The data packets provide information about the source and the destination of the data.
- This is how the information is sent and received via different devices on a network. 

- The network is the overall infrastructure that allows devices to communicate with each other.
- Network devices are specialized vehicles like **routers** and **switches** that manage what is being sent and received over the network.
- Additionally, devices like computers and phones connect to the network via network devices. 

![image](https://github.com/user-attachments/assets/9caf3e8e-1cc6-40d8-9bee-eb5a26540096)

> A router connects to the internet through a modem, which is provided by your internet service provider (ISP).

- The firewall is a security device that monitors incoming and outgoing traffic on your network.
- The router then directs traffic to the devices on your home network, which can include computers, laptops, smartphones, tablets, printers, and other devices.
- You can imagine here that the server is a file server. A
- ll devices on this network can access the files in this server.
- This diagram also includes a switch which is an optional device that can be used to connect more devices to your network by providing additional ports and Ethernet connections.
- Additionally, there are 2 routers connected to the switch here for load balancing purposes which will improve the performance of the network. 

### Devices and desktop computers :
- Most internet users are familiar with everyday devices, such as personal computers, laptops, mobile phones, and tablets. Each device and desktop computer has a unique MAC address and IP address, which identify it on the network. They also have a network interface that sends and receives data packets. These devices can connect to the network via a hard wire or a wireless connection.

### Firewalls :
- A firewall is a network security device that monitors traffic to or from your network.
- It is like your first line of defense. Firewalls can also restrict specific incoming and outgoing network traffic.
- The organization configures the security rules of the firewall.
- Firewalls often reside between the secured and controlled internal network and the untrusted network resources outside the organization, such as the internet.
- Remember, though, firewalls are just one line of defense in the cybersecurity landscape.

### Servers : 
- Servers provide information and services for devices like computers, smart home devices, and smartphones on the network.
- The devices that connect to a server are called clients.
- The following graphic outlines this model, which is called the client-server model.
- In this model, clients send requests to the server for information and services.
- The server performs the requests for the clients.
- Common examples include :
    1. DNS servers that perform domain name lookups for internet sites
    2. file servers that store and retrieve files from a database
    3. corporate mail servers that organize mail for a company. 

![image](https://github.com/user-attachments/assets/133e4df3-3766-44a2-a899-119932d132b8)

### Hubs and switches :
- Hubs and switches both direct traffic on a local network. A hub is a device that provides a common point of connection for all devices directly connected to it. Hubs additionally repeat all information out to all ports. From a security perspective, this makes hubs vulnerable to eavesdropping. For this reason, hubs are not used as often on modern networks; most organizations use switches instead. Hubs are more commonly used for a limited network setup like a home office. 

- Switches are the preferred choice for most networks. A switch forwards packets between devices directly connected to it. They analyze the destination address of each data packet and send it to the intended device. Switches maintain a MAC address table that matches MAC addresses of devices on the network to port numbers on the switch and forwards incoming data packets according to the destination MAC address.Overall, switches improve performance and security.
> Switches are a part of the data link layer in the TCP/IP model.

### Routers :
- Routers connect networks and direct traffic, based on the IP address of the destination network. Routers allow devices on different networks to communicate with each other. In the TCP/IP model, routers are a part of the network layer. The IP address of the destination network is contained in the IP header. The router reads the IP header information and forwards the packet to the next router on the path to the destination. This continues until the packet reaches the destination network. Routers can also include a firewall feature that allows or blocks incoming traffic based on information in the transmission. This stops malicious traffic from entering the private network and damaging the local area network.

### Modems and wireless access points
- Modems usually connect your home or office with an internet service provider (ISP). ISPs provide internet connectivity via telephone lines or coaxial cables. Modems receive transmissions or digital signals from the internet and translate them into analog signals that can travel through the physical connection provided by your ISP. Usually, modems connect to a router that takes the decoded transmissions and sends them on to the local network.

> Note: Enterprise networks used by large organizations to connect their users and devices often use other broadband technologies to handle high-volume traffic, instead of using a modem. 

![image](https://github.com/user-attachments/assets/71417c14-4463-4751-8e94-1e2d875ab72e)

### Wireless access point :

- A wireless access point sends and receives digital signals over radio waves creating a wireless network.
- Devices with wireless adapters connect to the access point using Wi-Fi.
- Wi-Fi refers to a set of standards that are used by network devices to communicate wirelessly.
- Wireless access points and the devices connected to them use Wi-Fi protocols to send data through radio waves where they are sent to routers and switches and directed along the path to their final destination.

![image](https://github.com/user-attachments/assets/41ac39f6-7dfc-4496-963d-82bccc306eaf)

### Using network diagrams as a security analyst :
- Network diagrams allow network administrators and security personnel to imagine the architecture and design of their organization’s private network.

- Network diagrams are maps that show the devices on the network and how they connect.
- Network diagrams use small representative graphics to portray each network device and dotted lines to show how each device connects to the other.
- By studying network diagrams, security analysts develop and refine their strategies for securing network architectures.

![image](https://github.com/user-attachments/assets/e190391a-0e85-441b-aef1-0eb2a0b5e9f4)

## Cloud Computing :

### Computing processes in the cloud :

- Traditional networks are called on-premise networks, which means that all of the devices used for network operations are kept at a physical location owned by the company, like in an office building, for example.
- Cloud computing, however, refers to the practice of using remote servers, applications, and network services that are hosted on the internet instead of at a physical location owned by the company.

- A cloud service provider (CSP) is a company that offers cloud computing services.
- These companies own large data centers in locations around the globe that house millions of servers.
- Data centers provide technology services, such as storage, and compute at such a large scale that they can sell their services to other companies for a fee.
- Companies can pay for the storage and services they need and consume them through the CSP’s **Application Programming Interface (API)** or web console.

### CSPs provide three main categories of services :

1. Software as a service (SaaS) : 
    - refers to software suites operated by the CSP that a company can use remotely without hosting the software.

2. Infrastructure as a service (IaaS) :
   - refers to the use of virtual computer components offered by the CSP.
   - These include virtual containers and storage that are configured remotely through the CSP’s API or web console.
   - Cloud-compute and storage services can be used to operate existing applications and other technology workloads without significant modifications.
   - Existing applications can be modified to take advantage of the availability, performance, and security features that are unique to cloud provider services.

3. Platform as a service (PaaS) :
   - refers to tools that application developers can use to design custom applications for their company.
   - Custom applications are designed and accessed in the cloud and used for a company’s specific business needs.

![image](https://github.com/user-attachments/assets/4758433f-6d26-4839-aa3a-0e2ca140f1d8)

### Hybrid cloud environments :
- When organizations use a CSP’s services in addition to their on-premise computers, networks, and storage, it is referred to as a hybrid cloud environment.
- When organizations use more than one CSP, it is called a multi-cloud environment.
- The vast majority of organizations use hybrid cloud environments to reduce costs and maintain control over network resources.

### Software-defined networks :
- CSPs offer networking tools similar to the physical devices that you have learned about in this section of the course.
- Next, you’ll review  software-defined networking in the cloud.
- Software-defined networks (SDNs) are made up of virtual network devices and services.
- Just like CSPs provide virtual computers, many SDNs also provide virtual switches, routers, firewalls, and more.
- Most modern network hardware devices also support network virtualization and software-defined networking.
- This means that physical switches and routers use software to perform packet routing.
- In the case of cloud networking, the SDN tools are hosted on servers located at the CSP’s data center.

### Benefits of cloud computing and software-defined networks :

1. Reliability :
- Reliability in cloud computing is based on how available cloud services and resources are, how secure connections are, and how often the services are effectively running.
- Cloud computing allows employees and customers to access the resources they need consistently and with minimal interruption. 

2. Cost :
- Traditionally, companies have had to provide their own network infrastructure, at least for internet connections.
- This meant there could be potentially significant upfront costs for companies.
- However, because CSPs have such large data centers, they are able to offer virtual devices and services at a fraction of the cost required for companies to install, patch, upgrade, and manage the components and software themselves.

3. Scalability :
- Another challenge that companies face with traditional computing is scalability.
- When organizations experience an increase in their business needs, they might be forced to buy more equipment and software to keep up.
- But what if business decreases shortly after? They might no longer have the business to justify the cost incurred by the upgraded components.
- CSPs reduce this risk by making it easy to consume services in an elastic utility model as needed.
- This means that companies only pay for what they need when they need it.

```
// Changes can be made quickly through the CSPs, APIs, or web console—much more quickly
// than if network technicians had to purchase their own hardware and set it up.
// For example, if a company needs to protect against a threat to their network,
// web application firewalls (WAFs), intrusion detection/protection systems (IDS/IPS),
// or L3/L4 firewalls can be configured quickly whenever necessary,
// leading to better network performance and security.
```

## TCP/IP Model :

### 4 Layers of TCP/IP model :

1. Network access layer
2. Internet Layer
3. Transport layer
4. Application layer

![image](https://github.com/user-attachments/assets/9ef424de-b84b-4e28-bae2-9f9c7ef2c43d)

### The TCP/IP model :
- The TCP/IP model is a framework used to visualize how data is organized and transmitted across a network.
- This model helps network engineers and network security analysts conceptualize processes on the network and communicate where disruptions or security threats occur.
- The TCP/IP model has four layers:
    1. The network access layer,
    2. internet layer,
    3. transport layer, and
    4. application layer.
- When troubleshooting issues on the network, security professionals can analyze which layers were impacted by an attack based on what processes were involved in an incident. 

![image](https://github.com/user-attachments/assets/7ac359ad-2ecb-4032-8199-345b6ed7386a)

**1. Network access layer** 
- The network access layer, sometimes called the data link layer, deals with the creation of data packets and their transmission across a network.
- This layer corresponds to the physical hardware involved in network transmission.
- Hubs, modems, cables, and wiring are all considered part of this layer.
- **The address resolution protocol (ARP)** is part of the network access layer.
- Since MAC addresses are used to identify hosts on the same physical network, ARP is needed to map IP addresses to MAC addresses for local network communication.

**2. Internet layer**
- The internet layer, sometimes referred to as the network layer, is responsible for ensuring the delivery to the destination host, which potentially resides on a different network.
- It ensures IP addresses are attached to data packets to indicate the location of the sender and receiver.
- The internet layer also determines which protocol is responsible for delivering the data packets and ensures the delivery to the destination host.

- Here are some of the common protocols that operate at the internet layer:

**Internet Protocol (IP)** : 
- IP sends the data packets to the correct destination and relies on the Transmission Control Protocol/User Datagram Protocol (TCP/UDP) to deliver them to the corresponding service.
- IP packets allow communication between two networks.
- They are routed from the sending network to the receiving network.
- TCP in particular retransmits any data that is lost or corrupt.

**Internet Control Message Protocol (ICMP)** : 
- The ICMP shares error information and status updates of data packets.
- This is useful for detecting and troubleshooting network errors.
- The ICMP reports information about packets that were dropped or that disappeared in transit, issues with network connectivity, and packets redirected to other routers.

**3. Transport layer**
- The transport layer is responsible for delivering data between two systems or networks and includes protocols to control the flow of traffic across a network.
- TCP and UDP are the two transport protocols that occur at this layer. 

    - **Transmission Control Protocol** 
      - The Transmission Control Protocol (TCP) is an internet communication protocol that allows two devices to form a connection and stream data.
      - It ensures that data is reliably transmitted to the destination service.
      - TCP contains the port number of the intended destination service, which resides in the TCP header of a TCP/IP packet.

    - **User Datagram Protocol** 
      - The User Datagram Protocol (UDP) is a connectionless protocol that does not establish a connection between devices before transmissions.
      - It is used by applications that are not concerned with the reliability of the transmission.
      - Data sent over UDP is not tracked as extensively as data sent using TCP.
      - Because UDP does not establish network connections, it is used mostly for performance sensitive applications that operate in real time, such as video streaming.

**4. Application layer**
- The application layer in the TCP/IP model is similar to the application, presentation, and session layers of the OSI model.
- The application layer is responsible for making network requests or responding to requests.
- This layer defines which internet services and applications any user can access.
- Protocols in the application layer determine how the data packets will interact with receiving devices.

- Some common protocols used on this layer are: 
    - Hypertext transfer protocol (HTTP)
    - Simple mail transfer protocol (SMTP)
    - Secure shell (SSH)
    - File transfer protocol (FTP)
    - Domain name system (DNS)

> Application layer protocols rely on underlying layers to transfer the data across the network.

![image](https://github.com/user-attachments/assets/9a590638-8817-4339-9ab8-bb43f0f230c2)

## OSI Model :

- The OSI model is a standardized concept that describes the seven layers computers use to communicate and send data over the network.
- Network and security professionals often use this model to communicate with each other about potential sources of problems or security threats when they occur.

![image](https://github.com/user-attachments/assets/6c4f2f53-7bdd-4250-b7e9-33433b565e10)

**1. Layer 7: Application layer**

- The application layer includes processes that directly involve the everyday user.
- This layer includes all of the networking protocols that software applications use to connect a user to the internet.
- This characteristic is the identifying feature of the application layer—user connection to the internet via applications and requests.

- An example of a type of communication that happens at the application layer is using a web browser.
- The internet browser uses HTTP or HTTPS to send and receive information from the website server.
- The email application uses simple mail transfer protocol (SMTP) to send and receive email information.
- Also, web browsers use the domain name system (DNS) protocol to translate website domain names into IP addresses which identify the web server that hosts the information for the website. 

**2. Layer 6: Presentation layer**

- Functions at the presentation layer involve data translation and encryption for the network.
- This layer adds to and replaces data with formats that can be understood by applications (layer 7) on both sending and receiving systems.
- Formats at the user end may be different from those of the receiving system.
- Processes at the presentation layer require the use of a standardized format.

- Some formatting functions that occur at layer 6 include :
    - encryption,
    - compression, and
    - confirmation
  that the character code set can be interpreted on the receiving system.
- One example of encryption that takes place at this layer is **SSL**, which encrypts data between web servers and browsers as part of websites with HTTPS.

**3. Layer 5: Session layer**

- A session describes when a connection is established between two devices.
- An open session allows the devices to communicate with each other.
- Session layer protocols keep the session open while data is being transferred and terminate the session once the transmission is complete. 

- The session layer is also responsible for activities such as :
    - authentication
    - reconnection
    - setting checkpoints during a data transfer.
    - 
- If a session is interrupted, checkpoints ensure that the transmission picks up at the last session checkpoint when the connection resumes.
- Sessions include a request and response between applications.
- Functions in the session layer respond to requests for service from processes in the presentation layer (layer 6) and send requests for services to the transport layer (layer 4).

**4. Layer 4: Transport layer**

- The transport layer is responsible for delivering data between devices.
- This layer also handles :
  - the speed of data transfer,
  - flow of the transfer, and
  - breaking data down into smaller segments to make them easier to transport.
    
- Segmentation is the process of dividing up a large data transmission into smaller pieces that can be processed by the receiving system.
- These segments need to be reassembled at their destination so they can be processed at the session layer (layer 5).
- The speed and rate of the transmission also has to match the connection speed of the destination system.
- TCP and UDP are transport layer protocols. 

**5. Layer 3: Network layer**

- The network layer oversees receiving the frames from the data link layer (layer 2) and delivers them to the intended destination.
- The intended destination can be found based on the address that resides in the frame of the data packets.
- Data packets allow communication between two networks.
- These packets include IP addresses that tell routers where to send them.
- They are routed from the sending network to the receiving network. 

**6. Layer 2: Data link layer**

- The data link layer organizes sending and receiving data packets within a single network.
- The data link layer is home to switches on the local network and network interface cards on local devices.

- Protocols like network control protocol (NCP), high-level data link control (HDLC), and synchronous data link control protocol (SDLC) are used at the data link layer.

**7. Layer 1: Physical layer** 

- As the name suggests, the physical layer corresponds to the physical hardware involved in network transmission.
- Hubs, modems, and the cables and wiring that connect them are all considered part of the physical layer.
- To travel across an ethernet or coaxial cable, a data packet needs to be translated into a stream of 0s and 1s.
- The stream of 0s and 1s are sent across the physical wiring and cables, received, and then passed on to higher levels of the OSI model.

