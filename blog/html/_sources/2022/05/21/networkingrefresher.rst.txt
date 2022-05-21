Networking Refresher
====================
The following notes are based on TCM Security’s ‘Practical Ethical Hacking’.
They provide a short refresher of the most important concepts of networks.

.. more::


IP Adresses
-----------
In Kali Linux ``ifconfig`` (Windows: ``ipconfig``), displays the settings of the
installed network adapters. ``inet`` shows the IPv4 address (used most frequently
today) in decimal format: 32 bits, separated into 4 bytes with 8 bits each, and
an ``inet6`` shows the IPv6 address using hexadecimal notation.

IPv4 with 32 bits offers 2**32 addresses in total, i.e. about 4.3 billion.
These addresses have all been used up for many years, therefore IPv6 was
invented, where the IPv6 addresses have 128 bits, which allows up to about
3.4E38 IP addresses. Nevertheless, everyone is still using IPv4 until today.

Network Address Translation (NAT) is the solution to address all network
devices with the help of **private** IP addresses. IP addresses that start with
10.x.x.x (class A, 16.6 Mio. IP addresses per subnet) or 192.168.x.x (class C,
255 IP addresses per subnet) are private IP addresses that do not get routed on
the public internet. All private IP addresses within one private subnet go out
to the public internet through one public IP address that is rented from the
Internet service provider (ISP).

IP belongs to level 3 of the OSI layer model. IP traffic is communicated via
routers.


MAC Addresses
-------------
Communication via MAC (media access control) happens on layer 2 of the OSI
layer model. Switches operate on this layer. The MAC address consists of 6 bytes
and is shown as "Hardware Address" or "ether" when you run ``ifconfig`` on Linux.
Anything that uses a network interface (network interface card [NIC], mobile
phone, etc.) has a MAC address. The first 3 bytes of the MAC address identify
the manufacturer of the NIC, the last 3 bytes denote the specific device, it
can be considered as a serial number given by the NIC manufacturer.


TCP, UDP and the 3-Way Handshake
--------------------------------
The transport layer is layer 4 of the OSI model. The Transmission Control
Protocol (TCP) is a connection-oriented protocol, whereas the User Datagram
Protocol (UDP) is connectionless. TCP is best suited when high reliability
is required, e.g. for HTTP(S), TCP, SSH connections. UDP is used for streaming,
DNS, voice over IP, etc.. For penetration testing, both types of connections
have to be scanned.

TCP establishes a connection between two network devices using a 3-way
handshake: (1) party A initializes the 3-way handshake by sending a SYN message
to party B, (2) party B returns a SYN-ACK message to party A, (3) party A
confirms the SYN-ACK with an ACK message. With the SYN package, party A informs
party B to which port it wants to connect. There are 65,000 ports that
are used for different protocols, e.g. HTTP, HTTPS, FTP, etc..

**Example:** Wireshark is used to capture web traffic and find a 3-way handshake
when a HTTPS connection is established (port 443).


Common Ports and Protocols
--------------------------
These port tables should be memorized so that you recognize which protocols are
being used when you scan a network.

.. table:: Common TCP ports
   :widths: auto

   ====== ===========================================================
    Port   Protocol
   ====== ===========================================================
      21   FTP (File Transfer Protocol)
      22   SSH (Secure Shell, encrypted remote login)
      23   Telnet (Remote Login, clear text)
      25   SMTP (Simple Mail Transfer Protocol)
      53   DNS (Domain Name System, resolves names to IP addresses)
      80   HTTP (Hypertext Transfer Protocol, not encrypted/secure)
     110   POP3 (email protocol)
     139   SMB (Samba, Windows file sharing)
     143   IMAP (email protocol)
     443   HTTPS (encrypted/secure HTTP)
     445   SMB (Samba, Windows file sharing, very frequent exploit)
   ====== ===========================================================


.. table:: Common UDP ports
   :widths: auto

   ====== =============================================================
    Port   Protocol
   ====== =============================================================
      53   DNS (Domain Name System)
      67   DHCP (Dynamic Host Control Protocol, IP address assignment)
      68   DHCP
      69   TFTP (Trivial FTP)
     161   SNMP (Simple Network Management Protocol)
   ====== =============================================================


The OSI Model
-------------
Mnemonic to memorize the layers of the OSI model: "Please do not throw sausage
pizza away!"

.. table:: OSI Layers
   :widths: auto

   ======= ==================================================
    Layer
   ======= ==================================================
      1     Physical layer (physical representation of bits)
      2     Data layer (MAC addresses, switches)
      3     Network layer (IP addresses, routing)
      4     Transport layer (TCP, UDP)
      5     Session layer (session management)
      6     Presentation layer (wmv, jpeg, mov)
      7     Application layer (HTTP, SMTP)
   ======= ==================================================

Troubleshooting should always start at layer 1 (physical) moving down through
the OSI stack until one finds the layer where the problem occurs.


Subnetting
----------
When you enter the ``ifconfig`` command, the output does not only show your
IPv4 address (``inet``), but also the subnet mask (``netmask``). Like the IPv4
address, the subnet mask consists of four bytes with 8 bits each. The positions
of the 1's and 0's in the subnet mask determine the IP address space that makes
up the subnet that the IP address belongs to. The bits are switched on from
leftmost to rightmost bit, the positions on the right side of the bit pattern
where the bits are 0 determine which IP addresses belong to the subnet. The
number of bits that set to one is called CIDR (Classless Inter-Domain Routing)
and is added as an abbreviated form of the subnet mask to the IP address of the
subnet (i.e. the lowest IP address that fulfills the pattern). A class C subnet
has a /24 CIDR and provides 256 IP addresses (hosts), 2 of which are used to
denote the network ID (1st address) and the broadcast address (last address).
It is commonly used for households and small businesses.

The goal of subnetting is to optimize the size of the subnet to provide sufficient
IP addresses for the intended number of hosts, but not unnecessarily wasting IP
address space, assuming that an organization can use a certain IP address
space.


.. author:: default
.. categories:: none
.. tags:: none
.. comments::


.. author:: default
.. categories:: none
.. tags:: none
.. comments::


