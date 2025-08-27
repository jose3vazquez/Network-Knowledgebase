# Category 01: Networking Concepts (60 Facts)

### OSI & TCP/IP Models
1. The **OSI model** has 7 layers: Physical, Data Link, Network, Transport, Session, Presentation, Application (Domain 1.1).  
2. The **TCP/IP model** has 4 layers: Network Interface, Internet, Transport, Application (Domain 1.1).  
3. The **Network layer (OSI)** handles logical addressing (IP) and routing (Domain 1.1).  
4. The **Data Link layer** provides MAC addressing and error detection via Ethernet or Wi-Fi (Domain 1.1).  
5. The **Transport layer** ensures reliable delivery (TCP) or fast delivery without reliability (UDP) (Domain 1.1).  
6. **Encapsulation** wraps data with headers/trailers as it moves down OSI layers (Domain 1.1).  
7. **De-encapsulation** strips headers/trailers as data moves up the stack (Domain 1.1).  
8. TCP/IP is often mapped to OSI: Application = App/Presentation/Session, Transport = Transport, Internet = Network, Network Access = Data Link/Physical (Domain 1.1).  

### IP Addressing
9. **IPv4 addresses** are 32-bit, shown as four octets (e.g., 192.168.1.1) (Domain 1.2).  
10. **IPv6 addresses** are 128-bit, written in hex groups (e.g., 2001:db8::1) (Domain 1.2).  
11. **Private IPv4 ranges**: 10.0.0.0/8, 172.16.0.0–172.31.255.255, 192.168.0.0/16 (Domain 1.2).  
12. **APIPA (Automatic Private IP Addressing)** assigns 169.254.x.x if DHCP fails (Domain 1.2).  
13. **CIDR notation** (e.g., /24) defines how many bits in the subnet mask are network bits (Domain 1.2).  
14. A **default gateway** forwards packets to destinations outside the local network (Domain 1.2).  
15. **Loopback addresses**: 127.0.0.1 (IPv4), ::1 (IPv6) used for self-testing (Domain 1.2).  
16. IPv6 includes **link-local addresses** (fe80::/10) for local communication (Domain 1.2).  
17. IPv6 supports **auto-configuration** using SLAAC (Stateless Address Autoconfiguration) (Domain 1.2).  
18. IPv6 uses **128-bit hexadecimal addressing** with colons; shorthand allows omission of leading zeros (Domain 1.2).  

### Subnetting & Routing
19. A **subnet mask** divides an IP into network and host portions (Domain 1.3).  
20. **Subnetting** allows splitting a network into smaller networks for efficiency (Domain 1.3).  
21. A **broadcast address** (e.g., 192.168.1.255 in /24) sends to all devices in the subnet (Domain 1.3).  
22. **Default route (0.0.0.0/0)** sends traffic for unknown destinations to a gateway (Domain 1.3).  
23. **Routing tables** store network paths and next hops (Domain 1.3).  
24. **Static routing** requires manual entry of routes (Domain 1.3).  
25. **Dynamic routing** protocols like RIP, OSPF, and EIGRP discover routes automatically (Domain 1.3).  
26. **OSPF (Open Shortest Path First)** is a link-state routing protocol using cost as metric (Domain 1.3).  
27. **BGP (Border Gateway Protocol)** is used on the internet to exchange routes between ISPs (Domain 1.3).  
28. **Default VLAN (1)** exists on most switches; best practice is to change or disable it (Domain 1.3).  

### Protocols & Ports
29. **HTTP (80)** and **HTTPS (443)** provide web traffic; HTTPS encrypts with TLS (Domain 1.4).  
30. **FTP (20/21)** transfers files; replaced by **SFTP** (22) or **FTPS** (990) for security (Domain 1.4).  
31. **SMTP (25, 587, 465)** sends emails; **IMAP (143/993)** and **POP3 (110/995)** receive emails (Domain 1.4).  
32. **DNS (53)** resolves hostnames to IP addresses (Domain 1.4).  
33. **DHCP (67/68)** dynamically assigns IPs to clients (Domain 1.4).  
34. **SSH (22)** provides encrypted remote access; replaces insecure **Telnet (23)** (Domain 1.4).  
35. **SNMP (161/162)** manages network devices; v3 adds encryption/authentication (Domain 1.4).  
36. **RDP (3389)** allows remote desktop connections to Windows machines (Domain 1.4).  
37. **LDAP (389/636)** provides directory services for authentication; LDAPS is secure (Domain 1.4).  
38. **NTP (123)** synchronizes time between devices (Domain 1.4).  

### Switching & VLANs
39. A **switch** operates at Layer 2 (MAC addresses); can also support Layer 3 routing (Domain 1.5).  
40. **MAC address tables** store port-to-device mappings in switches (Domain 1.5).  
41. **Collision domains** are isolated per switch port; hubs share one collision domain (Domain 1.5).  
42. **Broadcast domains** are separated by routers or VLANs (Domain 1.5).  
43. **Trunking (802.1Q)** carries multiple VLANs across a single link (Domain 1.5).  
44. **Port mirroring** copies traffic to a monitoring port for analysis (Domain 1.5).  
45. **PoE (Power over Ethernet)** delivers power and data over Ethernet cables (Domain 1.5).  
46. **STP (Spanning Tree Protocol)** prevents loops in switch topologies (Domain 1.5).  

### Wireless Networking
47. **802.11a** = 5 GHz, 54 Mbps; **802.11b** = 2.4 GHz, 11 Mbps (Domain 1.6).  
48. **802.11g** = 2.4 GHz, 54 Mbps; **802.11n** = 2.4/5 GHz, up to 600 Mbps (Domain 1.6).  
49. **802.11ac** = 5 GHz, multi-Gbps with MU-MIMO; **802.11ax (Wi-Fi 6)** = 2.4/5/6 GHz, high efficiency (Domain 1.6).  
50. **WPA2** uses AES encryption; **WPA3** improves key exchange security (Domain 1.6).  
51. **SSID (Service Set Identifier)** is the network name of a Wi-Fi network (Domain 1.6).  
52. **Channel overlap** on 2.4 GHz (1, 6, 11 non-overlapping) can cause interference (Domain 1.6).  
53. **Site surveys** measure wireless coverage and interference (Domain 1.6).  
54. **Antenna placement** (directional vs omnidirectional) affects Wi-Fi coverage (Domain 1.6).  

### Network Services & Concepts
55. **NAT (Network Address Translation)** maps private IPs to public IPs for internet access (Domain 1.7).  
56. **PAT (Port Address Translation)** allows many private IPs to share one public IP (Domain 1.7).  
57. **VPN (Virtual Private Network)** encrypts traffic between remote clients and networks (Domain 1.7).  
58. **Proxy servers** forward traffic requests, often for filtering or caching (Domain 1.7).  
59. **Content filtering** blocks restricted sites or services by policy (Domain 1.7).  
60. **QoS (Quality of Service)** prioritizes traffic like VoIP or video to reduce latency (Domain 1.7).  
