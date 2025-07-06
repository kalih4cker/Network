# Network

[CompTIA Network+](https://www.youtube.com/playlist?list=PLG49S3nxzAnl_tQe3kvnmeMid0mjF8Le8)

# OSI Model

-Open Systems Interconnection Reference Model

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/0ffce008-802c-4487-8685-2b507e4fe76a/6dbffc91-fc9b-4ba1-a60d-d22c7777ed94/image.png)

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/0ffce008-802c-4487-8685-2b507e4fe76a/7aec4ef9-feed-475d-a096-5d029aa56be1/image.png)

## **Physical Layer (Layer 1)**

**Definition:**

The Physical Layer is the foundation of the OSI model, concerned with the physical hardware used for data transmission. This includes actual cables, radio frequencies, and optical signals that send data as electrical or light signals.

**Technical Details & Protocols:**

- **Protocols:** While no standard protocols operate specifically at this layer, standards like **IEEE 802.3** (Ethernet), **IEEE 802.11** (Wi-Fi), and **Bluetooth** outline specifications for physical connections.
- **Transmission Modes:** Data can be transmitted via unshielded twisted pair (UTP), coaxial cables, or fiber optics. Radio waves are used in wireless communication.
- **Modulation & Signaling:** Techniques like **Amplitude Modulation (AM)** and **Frequency Modulation (FM)** control how signals are transmitted.

**Troubleshooting Techniques:**

- Run a **loopback test**, replace damaged cables, and check **punch-down connections** in network racks.

## **Data Link Layer (Layer 2)**

**Definition:**

The Data Link Layer provides reliable transmission by structuring data into frames and handling error detection and correction within the same local network. It’s often called the **Switching Layer** since switches function here to direct traffic within a network.

**Technical Details & Protocols:**

- **Protocols:** **Ethernet (IEEE 802.3)**, **Wi-Fi (IEEE 802.11)**, **PPP (Point-to-Point Protocol)**, **HDLC (High-Level Data Link Control)**, and **Frame Relay**.
- **Error Handling:** Uses **Cyclic Redundancy Check (CRC)** to detect errors in frames.
- **MAC Addresses:** Unique identifiers assigned to each network interface, allowing devices on the same network to communicate directly.

**Example Devices:**

- **Switches** and **bridges** work here to forward frames based on MAC addresses.

## **Network Layer (Layer 3)**

**Definition:**

The Network Layer is responsible for path determination and logical addressing, enabling data to travel across multiple networks. Routers function at this layer to forward packets based on IP addresses.

**Technical Details & Protocols:**

- **Protocols:** **IP (Internet Protocol)**, including **IPv4** and **IPv6**; **ICMP (Internet Control Message Protocol)** for sending error messages; **IGMP (Internet Group Management Protocol)** for managing group memberships in multicast communication.
- **Routing Protocols:** Protocols like **OSPF (Open Shortest Path First)**, **BGP (Border Gateway Protocol)**, and **RIP (Routing Information Protocol)** help routers determine the most efficient paths.
- **Packet Fragmentation:** Large packets are divided into smaller pieces to accommodate network limitations, ensuring compatibility across various networks.

**Example Devices:**

- **Routers** and **Layer 3 switches** that make forwarding decisions based on IP addresses.

## **Transport Layer (Layer 4)**

**Definition:**

The Transport Layer is responsible for end-to-end communication, ensuring complete data transfer. It manages error checking, flow control, and data reassembly.

**Technical Details & Protocols:**

- **Protocols:** **TCP (Transmission Control Protocol)** for reliable, connection-oriented communication, and **UDP (User Datagram Protocol)** for faster, connectionless communication.
- **Flow Control & Congestion Control:** Uses mechanisms like **Sliding Window Protocol** for TCP to regulate the amount of data sent.
- **Port Numbers:** Each application is assigned a unique port number (e.g., HTTP on port 80, HTTPS on port 443), which helps route data to the correct application on the receiving device.

**Example Applications:**

- TCP is often used for applications requiring reliability, like web browsing (HTTP/HTTPS) and email (SMTP). UDP is common in streaming or gaming where speed is prioritized over reliability.

## **Session Layer (Layer 5)**

**Definition:**

The Session Layer manages sessions between applications on different devices, maintaining and controlling the dialogue and synchronizing data streams. It ensures that the session remains active and can restart in case of interruptions.

**Technical Details & Protocols:**

- **Protocols:** **RPC (Remote Procedure Call)**, **PPTP (Point-to-Point Tunneling Protocol)**, **NetBIOS** for Windows networking.
- **Session Control:** Coordinates session management, including setting up, managing, and tearing down sessions.
- **Checkpoints and Synchronization:** Allows data transfer to resume at a specific checkpoint after an interruption.

**Example Applications:**

- This layer is essential for applications like remote desktops or virtual private networks (VPNs) that require a stable connection.

## **Presentation Layer (Layer 6)**

**Definition:**

The Presentation Layer formats and translates data so that the Application Layer can interpret it. This includes data encryption and compression, making data transmission efficient and secure.

**Technical Details & Protocols:**

- **Protocols:** **SSL (Secure Sockets Layer)** and **TLS (Transport Layer Security)** for encryption; **MIME (Multipurpose Internet Mail Extensions)** for encoding multimedia in email.
- **Data Formatting & Character Encoding:** Converts data formats such as **JPEG, GIF, BMP** for images and text formats like **ASCII** and **UTF-8**.
- **Encryption & Compression:** Encrypts data for security (e.g., HTTPS for secure web browsing) and compresses data to reduce transmission size.

**Example Applications:**

- Secure communication protocols (e.g., HTTPS) rely on this layer for data encryption and decryption.

## **Application Layer (Layer 7)**

**Definition:**

The Application Layer is the top layer, providing network services directly to user applications. It enables applications to access the network and is responsible for network-based applications like email, file transfer, and web browsing.

**Technical Details & Protocols:**

- **Protocols:** **HTTP (Hypertext Transfer Protocol)** and **HTTPS** for web browsing, **FTP (File Transfer Protocol)** for file sharing, **SMTP (Simple Mail Transfer Protocol)** for email, **DNS (Domain Name System)** for translating domain names to IP addresses.
- **User Interface:** Applications provide a user-friendly interface for interacting with network services.
- **Network Services:** Provides services that are directly accessible by end-users and applications, such as file transfer, email, and remote login.

**Example Applications:**

- Web browsers (e.g., Chrome, Firefox) for HTTP/HTTPS, email clients (e.g., Outlook) for SMTP/POP3, and FTP clients for file transfers.

# Networking Devices

### **Router**

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/0ffce008-802c-4487-8685-2b507e4fe76a/4f4820fd-4f0d-4641-bec6-80d26b902de7/image.png)

- **Role**: Routes traffic between different IP subnets, ensuring data reaches the right network.
- **OSI Layer**: Operates at **Layer 3** (Network Layer) by using IP addresses to forward packets.
- **Key Function**: Routers connect different types of networks (e.g., LAN to WAN), allowing them to communicate with each other.
- **Example**:
    - A **home router** connects all devices in your house (computers, phones) to the internet, managing the traffic that comes in and out of your network.
    - In an **office environment**, a router connects multiple departments (each with its own subnet) to the main company network and the internet, helping data travel between departments while keeping them segmented.

### **Switch**

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/0ffce008-802c-4487-8685-2b507e4fe76a/05e3877a-b4c7-4d01-a6e8-bf06285a6411/image.png)

- **Role**: Forwards data between devices in the same network, ensuring they can communicate without congestion.
- **OSI Layer**: Operates at **Layer 2** (Data Link Layer), using **MAC addresses** to identify devices.
- **Key Function**: Switches manage data traffic within a network (LAN) and are more efficient than hubs because they only send data to the device it’s meant for, reducing unnecessary traffic.
- **Example**:
    - In a **corporate office**, a switch connects all computers, printers, and phones, allowing them to communicate with each other at high speeds. It ensures internal data doesn’t need to leave the network to reach other devices.

### **Firewall**

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/0ffce008-802c-4487-8685-2b507e4fe76a/5fb46c35-154c-43ee-8dd9-be595a3d7bca/image.png)

- **Role**: Filters network traffic based on security rules to protect the network from unauthorized access.
- **OSI Layer**: Primarily operates at **Layer 4** (Transport Layer) but can also function up to **Layer 7** (Application Layer) in advanced models.
- **Key Function**: Firewalls block or allow traffic based on pre-set rules, helping to keep malicious users or software from accessing the network. They can also manage traffic based on port numbers or specific applications.
- **Example**:
    - A **business firewall** could block access to websites or services that are deemed unsafe (like social media or file-sharing services) while allowing employees to access necessary tools like email and company websites.

### **Intrusion Detection System (IDS) / Intrusion Prevention System (IPS)**

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/0ffce008-802c-4487-8685-2b507e4fe76a/4fcd3bd8-5b5f-4257-98c1-92c96db49835/image.png)

- **Role**: IDS monitors network traffic for signs of suspicious activity, while IPS also actively blocks potential threats.
- **OSI Layer**: Operates primarily at **Layer 3** (Network Layer) and **Layer 4** (Transport Layer), with some advanced systems inspecting up to **Layer 7** (Application Layer).
- **Key Function**: IDS detects potential attacks and sends alerts, while IPS automatically takes action to stop the attack before it can cause damage.
- **Example**:
    - On an **e-commerce website**, IDS might detect a spike in traffic that suggests a potential DDoS (Denial of Service) attack. IPS could block the offending IP addresses before they impact the site’s performance.

### **Load Balancer**

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/0ffce008-802c-4487-8685-2b507e4fe76a/0b9bddfb-e0a9-4225-bde9-fc8be4193f17/image.png)

- **Role**: Distributes incoming network traffic across multiple servers to prevent any single server from becoming overwhelmed.
- **OSI Layer**: Works at **Layer 4** (Transport Layer) or **Layer 7** (Application Layer), depending on how it is configured.
- **Key Function**: Load balancers ensure that network services (like websites or applications) remain responsive and available even during high traffic periods by spreading the workload across multiple servers.
- **Example**:
    - **Streaming services** like Netflix use load balancers to ensure users are directed to a server with the least load, so the service remains fast and uninterrupted even during peak times.

### **Proxy Server**

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/0ffce008-802c-4487-8685-2b507e4fe76a/b4369c40-8833-42a6-9440-984b54b41281/image.png)

- **Role**: Acts as an intermediary between users and the internet, handling requests on behalf of the user.
- **OSI Layer**: Operates at **Layer 7** (Application Layer).
- **Key Function**: A proxy server can cache data (storing frequently accessed web pages), block unwanted content (e.g., websites or ads), and improve security by masking the user's real IP address.
- **Example**:
    - In a **school network**, a proxy might restrict students from accessing social media sites or filter out inappropriate content, while also caching educational websites to speed up access for all users.

### **Network Attached Storage (NAS) vs. Storage Area Network (SAN)**

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/0ffce008-802c-4487-8685-2b507e4fe76a/ee8834c3-e055-4541-84b4-a6a772511100/image.png)

- **NAS**:
    - **Role**: Provides file-level storage accessible over a network, allowing multiple users to store and access files.
    - **OSI Layer**: Operates at **Layer 7** (Application Layer), as it provides file access over the network.
    - **Example**: In a small business, a **NAS device** allows employees to access shared documents and backups over the network, making collaboration easy.
- **SAN**:
    - **Role**: Provides block-level storage, making it appear like a local drive to the server, with high performance for critical applications.
    - **OSI Layer**: Operates primarily at **Layer 2** (Data Link Layer) and **Layer 3** (Network Layer).
    - **Example**: A **bank** might use a **SAN** to store transaction records, providing fast, direct access to the data by the database servers for quick processing.

### **Access Point (AP)**

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/0ffce008-802c-4487-8685-2b507e4fe76a/e8923170-aafd-4f05-b544-7cb87e2e3f75/image.png)

- **Role**: Provides wireless connectivity for devices, extending a wired network to wireless devices.
- **OSI Layer**: Operates at **Layer 2** (Data Link Layer), bridging wireless devices with the wired LAN.
- **Key Function**: APs allow devices like laptops, smartphones, and tablets to access the network wirelessly by broadcasting an SSID (Service Set Identifier).
- **Example**:
    - In a **hotel**, access points are spread throughout the building, allowing guests to connect to the internet from their rooms. All APs are connected back to a central router that manages internet access.

## IP (Internet Protocol)

1. **What is an IP Address Really?**
    - An **IP address** is a unique number assigned to each device that connects to a network, allowing it to send and receive data. It acts like the digital equivalent of your home address. Just like the postal system uses your address to deliver packages, the internet uses IP addresses to deliver data to and from your device.
2. **Structure of an IP Address:**
    - An **IPv4 address** is composed of four groups of numbers, separated by periods (dots). Each group is called an **octet**, and each octet can be a number from **0 to 255**. This is why it’s called an "8-bit" address in each octet, because each group can hold 8 bits (binary digits).
    
    **Example of an IPv4 address:**
    
    - `192.168.1.1`
    - Let’s break it down:
        - **192** is the first octet (8 bits, in decimal range 0-255).
        - **168** is the second octet.
        - **1** is the third octet.
        - **1** is the fourth octet.
        
        So, the total length of an IPv4 address is 32 bits (4 octets × 8 bits). This gives us around 4.3 billion unique addresses, which are becoming scarce as more and more devices connect to the internet.
        
3. **IPv6: The Future of IP Addresses**
    - **IPv6** was created to solve the limitations of IPv4, especially the shortage of available addresses.
    - An IPv6 address is **128 bits long**, and is written as 8 groups of 4 hexadecimal numbers (0-9, A-F), separated by colons.
    
    **Example of an IPv6 address:**
    
    - `2001:0db8:85a3:0000:0000:8a2e:0370:7334`
        - This is much longer than an IPv4 address. Let’s break it down:
        - **2001:0db8** is the first group.
        - **85a3** is the second group.
        - The rest of the address follows similarly.
        
        The **big difference** is that IPv6 can provide a virtually unlimited number of addresses, ensuring we won't run out anytime soon. This is because there are **340 undecillion** possible combinations in IPv6.
        

### **Public vs. Private IP Addresses:**

1. **Public IP Address**:
    - A **Public IP Address** is a unique address that identifies your device or network on the global internet. It’s like the address of your house that can be accessed by anyone on the street (the internet).
    - **Example**: When you visit a website, your public IP address is the one that gets associated with the data request.
    - These are provided by your **Internet Service Provider (ISP)**.
2. **Private IP Address**:
    - Private IP addresses are used within a local network (like your home or office) and are not routable on the internet.
    - These addresses are used for devices like laptops, phones, and printers, and all of them connect to the internet through a router, which has a **public IP**.
    - **Example ranges** for private IPs:
        - `192.168.x.x`
        - `10.x.x.x`
        - `172.16.x.x - 172.31.x.x`
    - These addresses allow devices to communicate with each other locally.
    
    **Example Setup**:
    
    - Your **home router** could have a public IP address (e.g., `58.50.123.100`) assigned by your ISP, but the devices within your home network (like your phone or laptop) might have private IPs, like `192.168.1.2`, `192.168.1.3`, etc.

### **Dynamic vs. Static IP Addresses:**

1. **Dynamic IP Address**:
    - This IP is temporary and assigned by the **DHCP** server (Dynamic Host Configuration Protocol), which is usually run by your ISP or your router at home.
    - Dynamic IPs change every time you reconnect to the internet, and they are **assigned from a pool** of available IP addresses. This is the most common type of IP address.
    - **Example**: Your home router may have a dynamic public IP assigned by your ISP, which changes from time to time.
2. **Static IP Address**:
    - A static IP is a fixed address that does not change. It is **permanently assigned** to your device or server.
    - This type of IP is used for devices or services that need to be accessible all the time, such as **web servers** or **email servers**.
    - **Example**: If you are running a website, you may want a static IP address so that the server is always accessible at the same address.

### **How IP Addresses Work in Communication:**

1. **Sending Data**:
    - When you request something online, like visiting a website, your device sends a request (a packet of data) to the website's server using the server's IP address. The packet will have the website's IP as the destination and your device’s IP as the source.
2. **Routing Data**:
    - The data doesn’t go directly to the destination in a straight line. Instead, it passes through several **routers** along the way. These routers use the IP address to figure out the best path to reach the destination.
    - Routers examine the destination IP address, decide where to send the data next, and pass it along.
3. **Network Address Translation (NAT)**:
    - Most home or office networks use **NAT** to translate private IP addresses into a single public IP address. This allows multiple devices to share the same public IP when accessing the internet.
    - **Example**: Your router assigns private IPs to each device in your house (like `192.168.1.2` for your laptop, `192.168.1.3` for your phone). But when these devices access the internet, they all use the router’s public IP (e.g., `58.50.123.100`).

### **Subnetting: Breaking Down IP Networks**

- Subnetting is the process of dividing an IP network into smaller parts or **subnets**. It helps to organize and efficiently allocate IP addresses. Each subnet has its own network address, which helps improve network performance and security.
- **Subnet Mask**: It’s a 32-bit address used to divide an IP address into two parts: the network part and the host part. For example, a common subnet mask for IPv4 is `255.255.255.0`.
    
    **Example**:
    
    - **IP Address**: `192.168.1.10`
    - **Subnet Mask**: `255.255.255.0`
    - In this case, the first three octets (`192.168.1`) are used for the network part, and the last octet (`10`) is used to identify the specific device in that network.
    
    ### **Classes of IP Addresses:**
    
    - **Class A:** Range from 1.0.0.0 to 126.255.255.255. The first octet defines the network, leaving three octets for hosts. Suitable for very large networks.
    - **Class B:** Range from 128.0.0.0 to 191.255.255.255. The first two octets define the network, leaving two octets for hosts. Used for medium to large networks.
    - **Class C:** Range from 192.0.0.0 to 223.255.255.255. The first three octets define the network, leaving one octet for hosts. Ideal for small networks.
    - **Class D:** Range from 224.0.0.0 to 239.255.255.255. Used for multicast groups.
    - **Class E:** Range from 240.0.0.0 to 255.255.255.255. Reserved for experimental use.

### **Subnetting IP Addresses**

Subnetting is the process of dividing a larger network into smaller subnetworks, or subnets. This practice helps in efficient network management, improved security, and better use of IP address space. Here's a detailed explanation:

1. **Purpose of Subnetting:**
    - Reduce network traffic by creating smaller broadcast domains
    - Improve network security by isolating parts of the network
    - Allow for more efficient use of IP addresses
    - Enable better network management and troubleshooting
2. **How Subnetting Works:**
    - Subnetting uses the host portion of an IP address to create additional network bits
    - This is done by "borrowing" bits from the host portion and adding them to the network portion
    - The subnet mask determines which parts of the IP address belong to the network and which to the host
3. **Subnet Mask:**
    - A 32-bit number that masks an IP address, dividing it into network and host portions
    - Represented in dotted decimal (e.g., 255.255.255.0) or CIDR notation (/24)
    - Example: 192.168.1.0 with subnet mask 255.255.255.0 (/24) means the first 24 bits are for the network, last 8 for hosts
4. **Subnetting Process:**
    - Determine the number of subnets needed
    - Calculate the number of host addresses required per subnet
    - Choose an appropriate subnet mask to accommodate these requirements
    - Divide the original network into subnets based on the new subnet mask
5. **Example of Subnetting:**Let's subnet the network 192.168.1.0/24 into four equal subnets:
    - Original network: 192.168.1.0/24 (subnet mask: 255.255.255.0)
    - To create 4 subnets, we need to borrow 2 bits from the host portion (2^2 = 4)
    - New subnet mask: 255.255.255.192 (/26)
    - Resulting subnets:
        - 192.168.1.0/26 (0-63)
        - 192.168.1.64/26 (64-127)
        - 192.168.1.128/26 (128-191)
        - 192.168.1.192/26 (192-255)
6. **Benefits of Subnetting:**
    - Reduced network congestion
    - Improved network performance
    - Enhanced security through network segmentation
    - More efficient use of IP address space
    - Easier network management and troubleshooting

# Ports

Ports are essential components in networking that allow multiple services to run on a single device. They act as virtual endpoints for communication between applications and the network.

### **What are Ports?**

- Ports are 16-bit numbers (0-65535) that identify specific processes or services on a computer.
- They work in conjunction with IP addresses to direct network traffic to the correct application on a device.

### **Types of Ports**

1. **Well-Known Ports (0-1023)**:
    - Reserved for common services and protocols.
    - **Examples**:
        - Port 80: HTTP (web browsing)
        - Port 443: HTTPS (secure web browsing)
        - Port 25: SMTP (email sending)
2. **Registered Ports (1024-49151)**:
    - Used by specific applications or protocols that are not as common as well-known ports.
    - **Examples**:
        - Port 3306: MySQL database
        - Port 5432: PostgreSQL database
3. **Dynamic/Private Ports (49152-65535)**:
    - Used for temporary connections or custom applications.
    - These are often assigned dynamically by the operating system.

### **How Ports Work in Networking**

- **Connection Establishment**: When a client connects to a server, it uses a source port (usually dynamic) to connect to a destination port (usually well-known or registered) on the server.
- **Example**: When you browse a website, your computer might use source port 54321 to connect to the web server's destination port 80 (HTTP) or 443 (HTTPS).

### **Common Port Numbers and Their Uses**

- Port 21: FTP (File Transfer Protocol)
- Port 22: SSH (Secure Shell)
- Port 53: DNS (Domain Name System)
- Port 110: POP3 (Post Office Protocol version 3, for email retrieval)
- Port 143: IMAP (Internet Message Access Protocol, for email retrieval)

### **Port Security**

- Firewalls often control access based on port numbers, allowing or blocking traffic to specific ports.
- **Example**: A firewall might block incoming traffic on port 3389 (Remote Desktop Protocol) to prevent unauthorized remote access attempts.

### **Port Forwarding**

- Used to make services on a private network accessible from the internet.
- **Example**: If you're hosting a web server on your home network, you might set up port forwarding on your router to direct incoming traffic on port 80 to your server's local IP address.

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/0ffce008-802c-4487-8685-2b507e4fe76a/a2ac1f62-fb8d-4d43-834e-132157ef5dfd/image.png)

# Protocols

Networking protocols are essential rules that define how data is transmitted across networks. Each protocol serves a specific function in the data communication process. Below is a detailed explanation of the most common networking protocols, along with examples, along with the layer in which they operate:

- **Transmission Control Protocol (TCP)**
    - Ensures reliable, ordered, and error-checked delivery of data.
    - Establishes a connection using a three-way handshake (SYN, SYN-ACK, ACK).
    - Example: Downloading a file; TCP ensures all parts are received correctly.
    - Used by applications like web browsers and email clients.
- **User Datagram Protocol (UDP)**
    - Provides a connectionless communication method without guarantees of delivery or order.
    - Faster than TCP due to minimal overhead.
    - Example: Live video streaming or online gaming where speed is more critical than reliability.
    - Commonly used in applications like VoIP (Voice over IP) and DNS queries.
- **Internet Protocol (IP)**
    - Responsible for addressing packets and routing them across networks.
    - Each device is assigned a unique IP address (IPv4 or IPv6).
    - Example: Sending an email involves IP to route the message to the recipient’s server.
    - Supports both unicast (one-to-one) and multicast (one-to-many) communications.
- **Address Resolution Protocol (ARP)**
    - Resolves IP addresses to MAC addresses within a local network.
    - Operates at the link layer of the OSI model.
    - Example: A computer sending an ARP request to find the MAC address of another device with a known IP address.
    - Helps in building the local ARP cache for faster future lookups.
- **Hypertext Transfer Protocol (HTTP)**
    - Application layer protocol for transmitting hypertext documents on the web.
    - Stateless protocol; each request from a client is treated independently.
    - Example: Browsing a website; when you click a link, an HTTP request retrieves the new page.
    - Supports various methods like GET, POST, PUT, and DELETE for different types of operations.
- **Secure Hypertext Transfer Protocol (HTTPS)**
    - Secure version of HTTP that encrypts data exchanged between client and server.
    - Uses SSL/TLS protocols for encryption, ensuring confidentiality and integrity.
    - Example: Online shopping sites use HTTPS to protect credit card information during transactions.
    - Indicates secure connections with a padlock icon in web browsers.
- **Domain Name System (DNS)**
    - Translates human-readable domain names into machine-readable IP addresses.
    - Hierarchical system consisting of DNS servers that cache and resolve queries.
    - Example: Typing `www.example.com` in a browser triggers a DNS lookup to find its IP address.
    - Supports features like load balancing and failover through multiple records.
- **Dynamic Host Configuration Protocol (DHCP)**
    - Automatically assigns IP addresses to devices on a network from a defined range (scope).
    - Reduces manual configuration and potential IP conflicts.
    - Example: When you connect to Wi-Fi, DHCP assigns your device an IP address dynamically.
    - Can also provide other network configuration details such as subnet mask and default gateway.
- **Secure Shell (SSH)**
    - Provides secure remote access to systems over unsecured networks.
    - Encrypts all data exchanged between client and server, preventing eavesdropping.
    - Example: System administrators use SSH to manage servers securely from remote locations.
    - Supports secure file transfers via SCP (Secure Copy Protocol) or SFTP (SSH File Transfer Protocol).
- **Simple Network Management Protocol (SNMP)**
    - Used for monitoring and managing network devices such as routers, switches, and servers.
    - Allows administrators to collect performance data and configure devices remotely.
    - Example: An SNMP manager polls network devices for status updates or alerts on issues like high CPU usage.
    - Utilizes MIBs (Management Information Bases) to define the structure of the management data.
- **File Transfer Protocol (FTP)**
    - Standard network protocol used for transferring files between client and server over TCP/IP networks.
    - Supports both anonymous access and user authentication for secure transfers.
    - Example: Web developers use FTP clients like FileZilla to upload website files to hosting servers.
    - Can operate in active or passive mode depending on firewall configurations.
- **Routing Information Protocol (RIP)**
    - A distance-vector routing protocol that uses hop count as its routing metric.
    - Limited to a maximum of 15 hops; anything beyond is considered unreachable.
    - Example: RIP routers share their routing tables with neighboring routers every few seconds to update paths.
    - Suitable for smaller networks due to its simplicity but not ideal for larger or more complex environments.
- **Open Shortest Path First (OSPF)**
    - A link-state routing protocol that uses cost as its routing metric based on bandwidth.
    - Supports hierarchical network design with areas to optimize routing efficiency.
    - Example: OSPF routers exchange information about their link states to build a complete map of the network topology.
    - More scalable than RIP, making it suitable for larger enterprise networks.
- **Internet Protocol Security (IPsec)**
    - A suite of protocols designed to secure Internet Protocol communications through encryption and authentication.
    - Operates at the network layer, protecting and authenticating IP packets between participating devices.
    - Example: Used in VPNs to secure data transmitted over public networks like the internet.
    - Provides confidentiality, integrity, and authenticity through various modes such as transport mode and tunnel mode.
- **Transmission Control Protocol/Internet Protocol (TCP/IP)**
    - The fundamental suite of protocols that underpins internet communications, combining TCP and IP functionalities.
    - Enables diverse devices across different networks to communicate effectively using standardized protocols.
    - Forms the basis for most internet services, including web browsing, email, file transfer, etc.

# Network Topologies

Network topologies are fundamental structures for organizing and connecting devices within a network. Choosing an appropriate topology is essential for optimizing communication, efficiency, and scalability in various network environments, such as offices, campuses, or data centers.

Why Topology Matters: Network topology helps determine the physical layout of devices and impacts factors like performance, fault tolerance, and expansion flexibility. When planning a new network or a building layout, understanding different topologies allows for better design suited to an organization’s needs.

## Star / Hub and Spoke Topology

**Usage**: Common in both large and small networks.

**Structure**: All devices connect to a central device (like a hub, switch, or router), forming a structure that resembles a star or a hub with spokes.

- **Pros**:
    - **Simple to manage**: Any device can be easily added or removed with minimal disruption.
    - **Fault isolation**: If a peripheral device fails, it doesn’t affect the rest of the network. However, a failure in the central hub can cause a complete network outage.
    - **Scalability**: Easy to add more devices by connecting them to the central hub.
- **Cons**:
    - **Single point of failure**: If the hub fails, all connected devices lose communication.
    - **Higher costs**: Requires more cabling and a robust central device, especially in larger networks.

**Typical Usage Scenarios**: Office networks, small to medium-sized LANs, and large organizations with clear central communication points.

## Mesh Topology

**Usage**: Typically used in environments requiring high redundancy and fault tolerance.

**Structure**: Devices are interconnected with multiple links, creating redundant paths between nodes.

- **Types**:
    - **Fully Connected Mesh**: Every device is directly connected to every other device.
    - **Partially Connected Mesh**: Some devices are connected to multiple devices but not all. This offers redundancy without the extensive cabling required for a full mesh.
- **Pros**:
    - **High reliability**: Multiple paths prevent a single point of failure. If one path fails, data can reroute through an alternate path.
    - **Resilience**: Suitable for mission-critical networks where continuous uptime is required.
- **Cons**:
    - **Complex and costly**: Requires more cabling and is challenging to set up in large networks.
    - **Maintenance difficulties**: Complexity can increase troubleshooting times and maintenance costs.

**Typical Usage Scenarios**: WANs (like the internet), financial networks, and critical network environments requiring high fault tolerance.

## Hybrid Topology

**Usage**: Combines elements of multiple topologies to suit specific needs.

**Structure**: A mixture of two or more topologies, allowing flexibility and customization based on the environment’s requirements.

- **Pros**:
    - **Adaptability**: Can combine the best features of different topologies for a custom solution.
    - **Scalability and efficiency**: Allows the network to grow and adapt as organizational needs change.
- **Cons**:
    - **Complex to design**: Requires careful planning to ensure compatibility and efficient traffic flow.
    - **Costly**: Implementing multiple topologies can increase hardware and setup costs.

**Typical Usage Scenarios**: Large organizations with diverse requirements, campus networks, and data centers.

## Spine and Leaf Architecture

**Usage**: Predominantly used in modern data centers, especially for cloud and virtualization environments.

**Structure**: Consists of two layers – spine and leaf. Each leaf switch (access layer) connects to each spine switch (core layer), creating a non-blocking, low-latency fabric.

- **Pros**:
    - **High bandwidth**: Leaf-spine architecture allows for large amounts of data transfer without bottlenecks.
    - **Predictable performance**: Uniform path lengths help minimize latency and improve predictability.
    - **Scalability**: Easy to add additional spine or leaf switches to accommodate growth without disrupting the existing network.
- **Cons**:
    - **Initial setup costs**: The cost can be higher due to the need for numerous high-performance switches.
    - **Complex maintenance**: Requires skilled IT personnel to manage and optimize the infrastructure.

**Typical Usage Scenarios**: Data centers, cloud infrastructures, and large-scale environments requiring high availability and low-latency connections.

**Key Term**:

- **Top-of-Rack (ToR) Switching**: In spine-leaf architecture, each rack of servers connects to a leaf switch within the same rack, which then links to the spine switches. This minimizes cable lengths and latency.

## Bus Topology

**Usage**: Often used in small, simple networks and was commonly found in early LANs.

**Structure**: All devices are connected to a single central cable (the bus), with data transmitted in both directions across the bus. Each device "taps" into this main cable to communicate with other devices.

- **Pros**:
    - **Cost-effective**: Requires minimal cabling and fewer devices, making it inexpensive.
    - **Simple to set up**: Easy to configure for small networks.
- **Cons**:
    - **Limited scalability**: As more devices are added, the network can slow down and become less reliable.
    - **Single point of failure**: If the main cable (bus) fails, the entire network can be disrupted.

**Typical Usage Scenarios**: Small LANs, test networks, and older network infrastructures.

## Ring Topology

**Usage**: Used in some specialized LAN setups and in early WANs.

**Structure**: Each device is connected to two other devices, forming a circular or "ring" structure. Data travels in one or both directions around the ring until it reaches its destination.

- **Types**:
    - **Unidirectional Ring**: Data travels in a single direction around the ring.
    - **Bidirectional Ring**: Data can travel in both directions, adding redundancy.
- **Pros**:
    - **Equal access**: Each device has the same opportunity to communicate, which can prevent data collisions.
    - **Fault tolerance (in bidirectional rings)**: With a bidirectional setup, a break in the ring won’t isolate devices.
- **Cons**:
    - **Difficult troubleshooting**: Isolating issues in the ring can be challenging.
    - **Scalability limits**: Adding or removing devices can disrupt the network.

**Typical Usage Scenarios**: Fiber Distributed Data Interface (FDDI) networks, some campus networks, and early telecommunications networks.

# IPv4

### **IP Address**

An IP address is a unique identifier for a device on a network. It allows devices to locate and communicate with each other. There are two versions of IP addresses: IPv4 and IPv6. IPv4 is the most commonly used and consists of four sets of numbers (0-255) separated by dots (e.g., 192.168.1.10). It work On OSI Layer 3 address

- **Example**:
    - **IPv4**: 192.168.1.10
    - **IPv6**: fe80::d4a8:64ff:fe74:d1f7

Each part of an IP address in IPv4 format represents different network segments, with the subnet mask and default gateway helping determine which part is the network ID and which part is the host ID.

### **Subnet Mask**

A subnet mask is used to divide an IP address into the network and host portions. It helps devices understand if an IP address belongs to the same local network or an external network.

- **Example**: For an IP address of 192.168.1.10, a common subnet mask is 255.255.255.0.
    - This subnet mask means that the first three sets of numbers (192.168.1) represent the network portion, and the last set (10) represents the host portion.
    - In binary form, 255.255.255.0 converts to `11111111.11111111.11111111.00000000`, where the `1`s correspond to the network portion and `0`s to the host portion.

With a subnet mask, the device determines if it should reach out within the local network or go through the gateway to communicate outside the network.

### **Default Gateway**

The default gateway is the IP address of a router on the local network that forwards traffic to other networks (such as the internet). If a device wants to communicate with an IP outside its local network, it sends the data to the default gateway, which then routes it accordingly.

- **Example**: If a network’s IP range is 192.168.1.1 - 192.168.1.255 with a subnet mask of 255.255.255.0, the default gateway could be 192.168.1.1.

This address is usually the first address in the subnet and is assigned to the router or networking device that connects the local network to other networks.

### **IP Address Classification**

IPv4 addresses are divided into five classes (A, B, C, D, and E), each serving different purposes:

1. **Class A**
    - **Range**: `0.0.0.0` to `127.255.255.255`
    - **Subnet Mask**: `255.0.0.0`
    - **Usage**: Large networks (e.g., large corporations)
    - **Network/Host Distribution**: 8 bits for the network, 24 bits for hosts
2. **Class B**
    - **Range**: `128.0.0.0` to `191.255.255.255`
    - **Subnet Mask**: `255.255.0.0`
    - **Usage**: Medium-sized networks (e.g., universities)
    - **Network/Host Distribution**: 16 bits for the network, 16 bits for hosts
3. **Class C**
    - **Range**: `192.0.0.0` to `223.255.255.255`
    - **Subnet Mask**: `255.255.255.0`
    - **Usage**: Small networks (e.g., small businesses)
    - **Network/Host Distribution**: 24 bits for the network, 8 bits for hosts
4. **Class D**
    - **Range**: `224.0.0.0` to `239.255.255.255`
    - **Usage**: Multicasting (sending data to multiple devices)
    - **Note**: Does not have a subnet mask, as it is used for group communication.
5. **Class E**
    - **Range**: `240.0.0.0` to `255.255.255.255`
    - **Usage**: Reserved for experimental purposes; not used in typical networking.

### **Loopback Address**

A loopback address is a special IP address used by a device to refer to itself. It allows for testing network interfaces and diagnosing network issues on the device itself without the need for physical network hardware. In IPv4, the loopback address range is `127.0.0.0` to `127.255.255.255`, with `127.0.0.1` being the most commonly used.

- **Example**: `127.0.0.1` (referred to as "localhost")
- **Usage**: Developers and network engineers use the loopback address to test software or network services on the same device, confirming that the TCP/IP stack is configured correctly.

## SDN (Software Defined Network)

**Software-Defined Networking (SDN)** is a modern approach to network management that aims to improve flexibility, scalability, and efficiency. It decouples the control plane (which decides where traffic is sent) from the data plane (which forwards traffic to its destination). This separation allows network administrators to manage network services through a centralized controller.

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/0ffce008-802c-4487-8685-2b507e4fe76a/5f233043-c86b-4042-a45b-b1020969f040/image.png)

SDN is nothing but virtualization of networking

- **Controller (Control Plane)**:
    - Acts as the brain of the network.
    - Centralized software that makes decisions about how traffic flows through the network.
    - Examples: Open Daylight, ONOS.
- **Data Plane**:
    - Comprises the physical or virtual switches and routers that forward the traffic based on instructions from the controller.
- **Application Plane**:
    - Includes applications and business logic that interact with the controller to define networking behavior, such as load balancing or firewall services.
- **Southbound Interface**:
    - Connects the controller to the data plane devices.
    - Protocols like OpenFlow are used to communicate between the controller and switches.
- **Northbound Interface**:
    - Connects the controller to applications or management systems, providing an abstraction of the network.

# IPv6 addressing

IPv6 (Internet Protocol version 6) is the most recent version of the Internet Protocol, designed to replace IPv4. It was developed to address the limitations of IPv4, particularly the exhaustion of available IP addresses.

### **Key Features of IPv6**

- **Larger Address Space**: IPv6 uses 128-bit addresses, providing approximately 340 undecillion (3.4 × 10^38) unique addresses.
- **Improved Packet Handling**: Simplified header structure for more efficient routing.
- **Built-in Security**: IPsec is integrated into IPv6, enhancing network security.
- **Better QoS (Quality of Service)**: Improved traffic prioritization capabilities.

### **IPv6 Address Structure**

An IPv6 address consists of eight groups of four hexadecimal digits, separated by colons.

- **Example**: 2001:0db8:85a3:0000:0000:8a2e:0370:7334

IPv6 addresses can be shortened by removing leading zeros in each group and replacing consecutive groups of zeros with a double colon (::).

- **Shortened Example**: 2001:db8:85a3::8a2e:370:7334

### **Types of IPv6 Addresses**

1. **Unicast**: Identifies a single network interface.
2. **Multicast**: Represents a group of interfaces.
3. **Anycast**: Assigned to multiple interfaces, with packets delivered to the nearest one.

### **IPv6 Subnetting**

IPv6 uses a simplified subnetting process compared to IPv4. The first 64 bits typically represent the network portion, while the last 64 bits are for the interface identifier

[Remote login ](https://www.notion.so/Remote-login-15e476499822808cbfaaca55d231dc8e?pvs=21)

# Remote Login

Remote login is a technology that allows an authorized user to login to other computer machines on same or remote network. Appears as if the user terminals were directly connected to that host computer. The user can do anything that the host has given permission for such as read, write and delete files. VPN provides access to a network remote login provides access to host within that network. VPN localize your computer, while remote login localizes you.

# Telnet

Network protocol that allows a user to communicate with a remote device

Virtual terminal protocol used mostly by network administrators to remotely access and manage devices

Uses TCP port 23 By default

Telnet client and server must be running

Uses: telnet [hostname] [port]

# SSH (Secured shell)

Network protocol like telnet with encryption 

uses public key and encryption to prevent eavesdropping

SSH client and server must be running

Usage: SSH Username@hostname Command

# VPN(virtual private network)

A **VPN (Virtual Private Network)** is a technology that creates a secure and encrypted connection over a public or private network, such as the internet. It allows users to send and receive data as if they were directly connected to a private network, ensuring **privacy**, **security**, and **anonymity** online.

### **How VPN Works:**

- A VPN encrypts your internet traffic and routes it through a secure server operated by the VPN provider.
- This hides your IP address and online activities from external parties, including hackers, ISPs (Internet Service Providers), or government surveillance.

The protocols used for VPN

-Internet protocol Security(IPsec)

-Point-to-point tunneling protocol (PPTP)

-Layer two tunneling protocol (L2TP)

-Secure socket tunneling protocol(SSTP)

-Secure Socket Layer(SSL)

# Proxies and Proxy server

-Proxy sever is an intermediary server between client and the internet

-Indirect network connection to other locations and services with your PC or mobile devices

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/0ffce008-802c-4487-8685-2b507e4fe76a/bdd22286-e596-44b6-b3d7-ef32958e79f6/image.png)

Applications

-Monitoring and Filtering

-Improving performance

-Translations and accessing services anonymously

-security 

# Ping

-Ping scan involves sending ICMP ECHO requests to a host. if the host is live, It will return an ICMP ECHO reply.

-This scan is useful for locating active devices or determining if ICMP is passing through a firewall.

# TCP 3-way handshake

The **three-way handshake** is a process used in TCP (Transmission Control Protocol) to establish a reliable connection between two devices (like a client and a server) before data transfer begins. Here’s a simple explanation with the flags involved:

### Steps of the Three-Way Handshake:

1. **SYN (Synchronize)**:
    - The client wants to start a connection, so it sends a packet with the **SYN** flag set.
    - This is like the client saying: *"Hey, I want to connect with you!"*
2. **SYN-ACK (Synchronize-Acknowledge)**:
    - The server receives the SYN packet and responds with a packet that has both **SYN** and **ACK** flags set.
    - The SYN flag means: *"Okay, I’m ready to connect too."*
    - The ACK flag means: *"I got your request."*
3. **ACK (Acknowledge)**:
    - The client sends a packet back with the **ACK** flag set to confirm it received the server’s SYN-ACK packet.
    - This is like the client saying: *"Great, I’m ready too. Let’s start talking!"*

For TCP Communication needs to work with a flag here is all TCP flag

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/0ffce008-802c-4487-8685-2b507e4fe76a/a6e8375f-c1ed-4de2-8d29-ed683a1fe3d1/image.png)
