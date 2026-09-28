# 📅 Day 06 - LAN, TCP/UDP, Ports & Network Applications

**Category:** Networking Fundamentals  
**Status:** Completed  
**Environment:** Cisco Packet Tracer / Kali Linux / Windows

---

## 🎯 Objective

Understand Local Area Networks (LANs), transport-layer protocols, port numbers, sockets, application-layer services, DNS, web communication, email protocols, remote-access protocols, and common network troubleshooting commands.

---

## ⚙️ Recovery / Process

### 1. Local Area Network (LAN)

LAN stands for **Local Area Network**.

A LAN connects devices and networks within a limited geographical area and is generally managed under a common administrative authority.

Examples include:

- Home networks
- Office networks
- School networks
- Small business networks

Devices within a LAN can communicate with each other using Layer 2 and Layer 3 networking.

---

## 2. ARP and MAC Address Discovery

**ARP — Address Resolution Protocol**

ARP is used by IPv4 devices to discover the MAC address associated with a known IPv4 address on the local network.

An ARP Request is sent as a broadcast using the Ethernet broadcast MAC address:

```text
FF:FF:FF:FF:FF:FF

**## DHCP Troubleshooting Commands**
```

DHCP can automatically provide network configuration to a host.

On Windows, the following commands can be used to manage and troubleshoot DHCP configuration.

Release an IPv4 address
ipconfig /release

This releases the current DHCP-assigned IPv4 configuration.

Request a new IPv4 address
ipconfig /renew

This requests or renews the DHCP configuration from the DHCP server.

Display complete configuration
ipconfig /all

This displays information such as:

IPv4 address
IPv6 address
Subnet mask
Default gateway
DNS servers
DHCP information
Physical/MAC address

Transport Layer — TCP and UDP

The Transport Layer is responsible for communication between applications running on network devices.

Two major transport-layer protocols are:

TCP
UDP
5. TCP — Transmission Control Protocol

TCP is a connection-oriented and reliable transport protocol.

TCP provides mechanisms such as:

Sequencing
Acknowledgments
Retransmission
Flow control
Reliable delivery

TCP uses port numbers to identify the applications involved in communication.

TCP Three-Way Handshake

TCP establishes a connection using a three-way handshake:

Client                    Server

   SYN  -------------------->
        <---------------- SYN-ACK
   ACK  -------------------->

After the handshake, data can be exchanged reliably.

TCP also uses sequence numbers so that transmitted data can be tracked and reassembled in the correct order.

## UDP — User Datagram Protocol

UDP is a connectionless transport protocol.

Unlike TCP, UDP does not establish a connection using a three-way handshake.

UDP does not provide TCP-style:

Guaranteed delivery
Sequencing
Retransmission
Connection establishment

Because of its lower overhead, UDP is useful for applications where speed and low latency are important.

Examples include:

Streaming
Voice communication
Video communication
Online gaming
DNS queries

The application decides whether UDP's characteristics are appropriate for the communication.

**## Port Numbers**

Port numbers operate at the Transport Layer and identify the application or service involved in network communication.

Ports range from:

0 – 65535

IANA (Internet Assigned Numbers Authority) coordinates the assignment of port numbers.

Port Categories
Well-Known Ports
0 – 1023

Used by commonly recognized network services.

Examples:

22    SSH
25    SMTP
53    DNS
80    HTTP
443   HTTPS
21    FTP
23    Telnet

**Registered Ports**
1024 – 49151

Used for applications and services registered with IANA.

Dynamic / Private Ports
49152 – 65535

These are commonly used as temporary source ports by client applications.

**## Sockets**

A socket represents an endpoint of network communication.

A socket can be understood using:

IP Address + Port Number + Transport Protocol

For example:

192.168.1.10:443/TCP

This identifies a TCP communication endpoint on port 443.

For a complete connection, the source and destination endpoints together identify the communication flow.

**## Netstat**

netstat is a network troubleshooting and diagnostic command.

It can display information such as:

Active connections
Listening ports
Network statistics
Routing information, depending on options and operating system

Example:

netstat -an

This can help identify which ports are listening or which connections are currently active.

**## Application Layer Services**

The Application Layer provides network services directly to applications and users.

A server is a host running software that provides services or resources to other hosts.

A client is a host or application that requests those services.

Basic model:

Client
   |
   | Request
   ↓
Server
   |
   | Response
   ↓
Client

**## URI, URN and URL**

Web resources can be identified using a URI — Uniform Resource Identifier.

## URI

A URI identifies a resource.

URN — Uniform Resource Name

A URN identifies a resource by name within a particular namespace.

URL — Uniform Resource Locator

A URL identifies a resource and provides information about where it can be accessed.

Example:

https://example.com/index.html

A URL can specify components such as:

Protocol/scheme
Host/domain
Port
Path
Query
Fragment

Common schemes include:

HTTP
HTTPS
FTP
SSH

DNS

## Domain Name System

Resolves domain names to IP addresses and provides other DNS information.

Common port:

53
SSH

## Secure Shell

Provides encrypted remote access to systems.

Default port:

22

SSH is preferred over Telnet for remote administration because SSH encrypts the communication.

Example:

ssh username@192.168.1.10
Telnet

Telnet provides remote terminal access but does not encrypt the communication by default.

Default port:

23

Because credentials and other information can be transmitted in plaintext, Telnet has largely been replaced by SSH for secure remote administration.

## SMTP

Simple Mail Transfer Protocol

SMTP is used primarily to send and relay email.

Common ports include:

25
587
465

The exact port depends on the SMTP service and security configuration.

## POP3

Post Office Protocol version 3

Used by email clients to retrieve messages from a mail server.

POP3 commonly downloads messages to the client and traditionally does not maintain the same server-side mailbox synchronization model as IMAP.

Common ports:

110
995 (POP3 over TLS)
IMAP

## Internet Message Access Protocol

Allows email clients to access and synchronize messages stored on a mail server.

Unlike traditional POP3 usage, IMAP is designed to keep messages on the server and synchronize mailbox state across clients.

Common ports:

143
993 (IMAP over TLS)
DHCP

## Dynamic Host Configuration Protocol

Automatically provides network configuration such as:

IP address
Subnet mask
Default gateway
DNS server information
HTTP

## Hypertext Transfer Protocol

Used by web clients and web servers to exchange web resources.

Default port:

80
HTTPS

## Hypertext Transfer Protocol Secure

HTTP communication protected using TLS.

Default port:

443

## FTP

## File Transfer Protocol

Used to transfer files between systems.

FTP traditionally uses:

21 — Control connection
20 — Data connection in active mode

FTP itself does not provide encryption.

## HTML

HTML stands for:

HyperText Markup Language

HTML provides the structure of web pages.

It defines elements such as:

Headings
Paragraphs
Links
Images
Forms
Page structure

The browser interprets the HTML and renders the page for the user.

## Remote Access — SSH vs Telnet
Telnet
Client
   |
   | Telnet
   ↓
Remote Server

Telnet provides remote access but sends communication without encryption.

## SSH
Client
   |
   | Encrypted SSH connection
   ↓
Remote Server

SSH provides secure, encrypted remote administration.

Example:

ssh username@192.168.1.100
17. Email Communication

A simplified email flow is:

Email Client
     |
     | SMTP
     ↓
Local Mail Server
     |
     | SMTP
     ↓
Recipient Mail Server
     |
     | IMAP / POP3
     ↓
Recipient Email Client

## SMTP is primarily responsible for sending and relaying email.

POP3 and IMAP are primarily used for retrieving/accessing email.

## Network Troubleshooting Commands

Several commands were introduced for diagnosing network problems.

IP Configuration
ipconfig
ipconfig /all
ipconfig /release
ipconfig /renew
Connectivity Testing
ping 8.8.8.8

Tests basic IP connectivity.

## DNS Testing
nslookup example.com

Tests DNS resolution.

Active Connections
netstat -an

Displays active connections and listening ports.

Route Tracing

Windows:

tracert example.com

Linux:

traceroute example.com