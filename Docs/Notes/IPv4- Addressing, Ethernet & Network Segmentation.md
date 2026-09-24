# 📅 Day 04 - IPv4 Addressing, Ethernet & Network Segmentation
**Problem**
Continued networking fundamentals from TCP/IP and the OSI model, focusing on how data is transmitted, encapsulated, addressed, and delivered across networks.

**Process**

1. Reviewed the three main transmission media:

   * Copper
   * Fiber (glass/plastic)
   * Wireless

2. Studied **Ethernet** as a common LAN technology and the role of the **NIC (Network Interface Card)**.

3. Learned that every Ethernet NIC has a unique **MAC address** used for Layer 2 communication.

4. Learned **encapsulation** — placing data inside another protocol format before transmission.

5. Learned **decapsulation** — removing those protocol layers when data is received.

6. Studied the Ethernet frame structure:

   * Preamble
   * Destination MAC address
   * Source MAC address
   * Type/Length
   * Data
   * Frame Check Sequence (FCS)

7. Moved into **IPv4 addressing**:

   * IPv4 uses 32 bits.
   * The address is divided into four 8-bit **octets**.
   * IPv4 has a hierarchical **network + host** structure.
   * The subnet mask identifies the network portion of an address.

8. Reviewed IPv4 communication types:

   * **Unicast** — one host to one host.
   * **Broadcast** — one host to all devices on the local network.
   * **Multicast** — one host to a selected group of subscribed hosts.

9. Studied **private and public IPv4 addresses** and **NAT (Network Address Translation)**.

10. Reviewed special IPv4 addresses:

* **Loopback:** `127.0.0.0/8` — commonly `127.0.0.1`
* **Link-local/APIPA:** `169.254.0.0/16` — self-assigned when a host cannot obtain an address from DHCP.

11. Reviewed legacy IPv4 address classes:

* **Class A:** `0.0.0.0/8 – 127.0.0.0/8`
* **Class B:** `128.0.0.0/16 – 191.255.0.0/16`
* **Class C:** `192.0.0.0/24 – 223.255.255.0/24`

12. Learned about **CIDR (Classless Inter-Domain Routing)**, introduced in the 1990s to replace the limitations of classful addressing and allocate IP addresses more efficiently.

13. Reviewed **IANA (Internet Assigned Numbers Authority)** and the **Regional Internet Registries (RIRs)**:

* ARIN — American Registry for Internet Numbers
* AFRINIC — African Network Information Centre
* LACNIC — Latin America and Caribbean Internet Addresses Registry
* APNIC — Asia Pacific Network Information Centre
* RIPE NCC — Réseaux IP Européens Network Coordination Centre

14. Introduced **ARP (Address Resolution Protocol)**, which is used to discover the MAC address associated with an IPv4 address on a local network.

15. Learned that ARP broadcasts remain within the local network segment. **Routers do not forward ARP broadcasts**, while switches forward them within the local broadcast domain.

16. Began studying **network segmentation and subnetting** — dividing a network into smaller logical networks.

**Commands**

```bash
ip a
ip route
arp -a
```

**Lesson**

* Ethernet operates at the LAN/data-link level and uses MAC addresses.
* IPv4 provides logical addressing and uses 32-bit addresses.
* Encapsulation prepares data for transmission; decapsulation reverses the process.
* MAC addresses identify interfaces locally, while IP addresses provide logical network addressing.
* Subnet masks determine the network and host portions of an IPv4 address.
* ARP maps IPv4 addresses to MAC addresses on a local network.
* Routers separate broadcast domains.
* CIDR replaced traditional class-based addressing for more efficient IP allocation.
* **RFC** stands for **Request for Comments** and is the publication system used to document Internet standards, protocols, and technical specifications.
