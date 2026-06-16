# Computer Networks Fundamentals

## Introduction to Computer Networks

A Computer Network is a collection of interconnected devices such as computers, servers, smartphones, routers, and switches that communicate and share data with one another.

### Advantages of Computer Networks

* Resource Sharing
* Data Sharing
* Communication and Collaboration
* Internet Access
* Centralized Management

---

## Networking Devices
### Router

A Router is a networking device that connects different networks and forwards data packets between them.

#### Functions

* Connects local networks to the Internet
* Determines the best path for data transmission
* Routes packets between networks
* Often provides DHCP services

#### Example

When you search for Google on your laptop, the router forwards your request to the Internet through your ISP.

---

### Switch

A Switch is a networking device that connects devices within the same network.

#### Functions

* Transfers data between devices
* Uses MAC addresses to identify destination devices
* Reduces network collisions
* Improves network efficiency

#### Example

In a computer lab, all computers communicate through a switch.

---

## Data Units in Networking

As data moves through different layers of the OSI model, its name changes.

### Segment

A Segment is the data unit at the Transport Layer.

#### Contains

* Source Port Number
* Destination Port Number
* User Data

#### Example

A TCP segment carrying a web request from a browser to a server.

---

### Packet

A Packet is the data unit at the Network Layer.

#### Contains

* Source IP Address
* Destination IP Address
* Payload

#### Example

A packet traveling from your computer to Google's server.

---

## Addressing

### IP Address

An IP (Internet Protocol) Address is a logical address used to uniquely identify a device on a network.

#### Types of IP Addresses

##### IPv4

Example:
192.168.1.10

##### IPv6

Example:
2001:db8::1

#### Purpose

* Identifies devices logically
* Enables communication across networks
* Used by routers for routing

---

### MAC Address

A MAC (Media Access Control) Address is a unique physical address assigned to a Network Interface Card (NIC).

#### Example

00:1A:2B:3C:4D:5E

#### Purpose

* Identifies devices within a local network
* Used by switches for forwarding frames

#### Difference Between IP and MAC Address

| IP Address      | MAC Address       |
| --------------- | ----------------- |
| Logical Address | Physical Address  |
| Can Change      | Usually Permanent |
| Used by Routers | Used by Switches  |
| Layer 3         | Layer 2           |

---

## Flow of Data on Google/Internet

Suppose a user enters **[www.google.com](http://www.google.com)** in a browser.

### Step 1: Browser Creates Request

The browser generates an HTTP or HTTPS request.

### Step 2: DNS Lookup

DNS converts:

[www.google.com](http://www.google.com)

into an IP address such as:

142.250.193.78

### Step 3: Data Leaves the Computer

The request is encapsulated and sent to the network adapter.

### Step 4: Switch

The switch receives the frame and forwards it toward the router.

### Step 5: Router

The router forwards the packet to the ISP.

### Step 6: Internet Backbone

Multiple routers across the Internet forward the packet toward Google's servers.

### Step 7: Google Server

Google processes the request and prepares a response.

### Step 8: Response Returns

The response travels back through routers, ISP, router, switch, and finally reaches the user's computer.

---

## OSI Model

OSI (Open Systems Interconnection) is a seven-layer networking model developed to standardize communication between systems.

| Layer Number | Layer Name   |
| ------------ | ------------ |
| 7            | Application  |
| 6            | Presentation |
| 5            | Session      |
| 4            | Transport    |
| 3            | Network      |
| 2            | Data Link    |
| 1            | Physical     |

### Layer 7: Application Layer

Provides services directly to users and applications.

#### Examples

* HTTP
* HTTPS
* FTP
* DNS

#### Functions

* Web Browsing
* Email Services
* File Transfer

---

### Layer 6: Presentation Layer

Responsible for data formatting and translation.

#### Functions

* Encryption
* Decryption
* Compression
* Data Translation

#### Example

Converting plain text into encrypted text before transmission.

---

### Layer 5: Session Layer

Manages communication sessions between devices.

#### Functions

* Session Establishment
* Session Maintenance
* Session Termination

#### Example

Maintaining a user login session on a website.

---

### Layer 4: Transport Layer

Provides reliable end-to-end communication.

#### Protocols

* TCP
* UDP

#### Functions

* Segmentation
* Flow Control
* Error Recovery
* Reliability

#### Data Unit

Segment

---

### Layer 3: Network Layer

Responsible for routing packets between networks.

#### Protocol

* IP

#### Functions

* Logical Addressing
* Routing
* Path Determination

#### Device

Router

#### Data Unit

Packet

---

### Layer 2: Data Link Layer

Responsible for communication between devices on the same network.

#### Functions

* MAC Addressing
* Frame Transmission
* Error Detection

#### Device

Switch

#### Data Unit

Frame

---

### Layer 1: Physical Layer

Responsible for transmitting raw bits through a physical medium.

#### Examples

* Ethernet Cable
* Fiber Optic Cable
* Wi-Fi Signals

#### Data Unit

Bits

---

## Cryptography Basics

Cryptography is the science of securing information from unauthorized access.

### Symmetric Key Cryptography

Uses a single key for both encryption and decryption.

#### Process

Plain Text → Encryption Key → Cipher Text → Same Key → Plain Text

#### Advantages

* Fast
* Efficient
* Suitable for large amounts of data

#### Disadvantages

* Key sharing is difficult

#### Examples

* AES
* DES

---

### Asymmetric Key Cryptography

Uses two different keys.

#### Types of Keys

* Public Key
* Private Key

#### Process

Public Key → Encryption

Private Key → Decryption

#### Advantages

* Secure key exchange
* Better authentication

#### Disadvantages

* Slower than symmetric encryption

#### Examples

* RSA
* ECC

---

## Networking Protocols and Concepts

### MAC (Media Access Control)

MAC is responsible for identifying devices at the Data Link Layer.

#### Features

* Physical Hardware Addressing
* Local Network Communication
* Frame Delivery

---

### TCP (Transmission Control Protocol)

TCP is a connection-oriented protocol that guarantees reliable communication.

#### Features

* Reliable Delivery
* Error Checking
* Ordered Data Transmission
* Flow Control
* Acknowledgment Mechanism

#### Uses

* Web Browsing
* Online Banking
* Email Services

#### Working

1. Connection Establishment (Three-Way Handshake)
2. Data Transfer
3. Connection Termination

---

### UDP (User Datagram Protocol)

UDP is a connectionless protocol.

#### Features

* Faster than TCP
* No Connection Establishment
* No Delivery Guarantee
* Low Overhead

#### Uses

* Online Gaming
* Video Streaming
* VoIP Calls
* Live Broadcasting

---

### DNS (Domain Name System)

DNS converts domain names into IP addresses.

#### Example

google.com → 142.250.x.x

#### Importance

Humans can remember names more easily than numerical IP addresses.

---

### FTP (File Transfer Protocol)

FTP is used for transferring files between systems.

#### Operations

* Upload Files
* Download Files
* Manage Remote Files

#### Default Port

21

#### Drawbacks

* No Encryption
* Vulnerable to Attacks

---

### HTTP (HyperText Transfer Protocol)

HTTP is used for communication between web browsers and web servers.

#### Characteristics

* Stateless Protocol
* Application Layer Protocol

#### Default Port

80

#### Example

Loading a webpage in a browser.

---

### TLS (Transport Layer Security)

TLS provides security for data transmission over networks.

#### Features

* Encryption
* Authentication
* Data Integrity

#### Purpose

Protects data from eavesdropping and tampering during transmission.

---

### HTTPS (HyperText Transfer Protocol Secure)

HTTPS is HTTP combined with TLS security.

#### Features

* Encrypted Communication
* Secure Data Transfer
* Website Authentication

#### Default Port

443

#### Example

https://www.google.com

---

### PuTTY

PuTTY is a free terminal emulator and remote access tool.

#### Supports

* SSH
* Telnet
* Serial Connections

#### Uses

* Linux Server Administration
* Network Device Configuration
* Remote System Management

---

### SSH (Secure Shell)

SSH is a secure protocol for remote login and remote command execution.

#### Features

* Encrypted Communication
* Secure Authentication
* Safe Remote Access

#### Default Port

22

#### Uses

* Managing Linux Servers
* Remote Administration
* Secure File Transfer

#### Example Command

ssh username@server_ip

---

### TELNET

TELNET is a protocol used for remote login to another computer over a network.

#### Features

* Text-Based Communication
* Remote Access Capability
* No Encryption

