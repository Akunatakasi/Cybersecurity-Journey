📅 Cybersecurity Journey — ELF
Day 04: IPv6 Addressing, DHCPv4 & Network Migration

Category: Networking Fundamentals
Status: In Progress
Environment: Kali Linux / Cisco Packet Tracer

🎯 Objective

Understand the transition from IPv4 to IPv6, IPv6 addressing rules, IPv4 address assignment methods, and the DHCPv4 communication process.

1. IPv4 to IPv6 Migration

The transition from IPv4 to IPv6 is an ongoing process. IPv4 and IPv6 coexist as networks gradually adopt IPv6.

The IETF (Internet Engineering Task Force) has standardized several migration techniques to support this transition.

Migration Techniques
Technique	Description
Dual Stack	Allows IPv4 and IPv6 to operate simultaneously on the same network device or network.
Tunneling	Encapsulates IPv6 packets inside IPv4 packets to transport them across an IPv4 network.
Translation	Converts traffic between IPv4 and IPv6 using technologies such as NAT64.

Key Note: NAT64 enables communication between IPv6 and IPv4 networks, commonly allowing IPv6-only clients to access IPv4 servers.

2. IPv6 Addressing

IPv6 uses a 128-bit addressing system represented in hexadecimal notation.

Hexadecimal Number System

Hexadecimal uses 16 symbols:

0 1 2 3 4 5 6 7 8 9 A B C D E F

IPv6 addresses are written as eight groups of four hexadecimal digits, separated by colons.

IPv6 Address Shortening Rules

IPv6 addresses can be shortened using two primary rules:

Rule 1: Omit Leading Zeros

Leading zeros in an individual hexadecimal group can be omitted.

Example:

2001:0DB8:0000:0001

Becomes:

2001:DB8:0:1

Rule 2: Double Colon (::)

A consecutive sequence of zero-valued groups can be replaced with ::.

Example:

2001:0DB8:0000:0000:0000:0000:0000:0001

Becomes:

2001:DB8::1

Important: The double colon can only appear once in an IPv6 address because using it more than once would make the number of omitted groups ambiguous.

3. Static IPv4 Addressing

Static IPv4 addressing occurs when a network administrator manually configures the IP address information on a host.

The configuration typically includes:

Component	Purpose
IPv4 Address	Identifies the host on an IP network.
Subnet Mask	Identifies the network portion and host portion of the IPv4 address.
Default Gateway	Provides a path for traffic destined for other networks.

Advantages:

Provides greater administrative control over IP address assignments.
Useful for devices that require predictable IP addresses.

Disadvantage:

Manual configuration can be time-consuming, particularly on large networks.
4. Dynamic IPv4 Addressing (DHCPv4)

Dynamic Host Configuration Protocol for IPv4 (DHCPv4) automatically assigns IPv4 configuration information to hosts.

DHCP can provide:

IPv4 address
Subnet mask
Default gateway
DNS server information and other network configuration options

DHCP reduces the need for manual IP configuration and helps administrators manage network resources efficiently.

5. DHCPv4 Operation — DORA Process

DHCPv4 uses a four-step process commonly known as DORA.

Step	Message	Description
1	DHCP Discover	The client broadcasts a message to locate available DHCP servers.
2	DHCP Offer	The DHCP server offers an available IP address and configuration information.
3	DHCP Request	The client broadcasts a request indicating which offer it has accepted.
4	DHCP Acknowledgment (ACK)	The server confirms the lease and finalizes the IP address assignment.

Key Notes:

The DHCP client uses its MAC address as part of the process of identifying itself at the network layer's underlying link layer.
DHCP Discover and DHCP Request are commonly broadcast during the initial address acquisition process.
The DHCP server provides a lease, meaning the client is permitted to use the assigned IP address for a specified period.

DORA = Discover → Offer → Request → Acknowledgment

6. Routers as Gateways — Next Topic

This is where we'll continue in the next session.

Topics to cover:

How routers function as default gateways
How hosts send traffic to destinations outside their local network
The relationship between IP addresses, subnet masks, and default gateways
Practical network configuration in Cisco Packet Tracer
🧠 Key Lessons
IPv4-to-IPv6 migration is ongoing, with both protocols coexisting during the transition.
Dual Stack, Tunneling, and Translation are important IPv4-to-IPv6 migration techniques.
IPv6 uses 128-bit addresses represented in hexadecimal notation.
IPv6 addresses can be shortened by omitting leading zeros and using double colons.
Static IPv4 addressing requires manual configuration.
DHCPv4 automates IPv4 address assignment using the DORA process.
Routers provide a pathway for communication between different networks.
📌 Progress Tracker
Topic	Status
IPv4 Addressing	Completed
IPv6 Addressing	Completed
IPv4-to-IPv6 Migration	Completed
Static IPv4 Addressing	Completed
DHCPv4 & DORA	Completed
Routers as Gateways	Next Session