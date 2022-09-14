Hacking and Networks
====================

Practical Ethical Hacking
-------------------------

The following blog posts are notes that I have taken while I was working
through
`TCM Sec Academy's <https://tcm-sec.com/so-you-want-to-be-a-hacker-2021-edition>`_
"Practical Ethical Hacking" course. The list has the same struture as the course,
but the notes reflect my own preferences. I have left out or shortened stuff
that I knew already, and I may add additional information from other sources
over time. Just reading my notes is surely no substitute for taking the course.

The first half of the course is available free of charge on
`youtube <https://www.youtube.com/watch?v=OghyFX9YMi8&list=PLtsY6_AbwdOR9EhsVR1zSnzXNr1dlnPMK>`_.

**Notekeeping**

* `Taking Notes
  <https://aojanzen.github.io/blog/html/2022/05/28/takingnotes.html>`_

**Networking Refresher**

* `Networking Refresher
  <https://aojanzen.github.io/blog/html/2022/05/21/networkingrefresher.html>`_

**Introduction to Linux**

* `Introduction to Linux
  <https://aojanzen.github.io/blog/html/2022/05/22/introductiontolinux.html>`_
* `Scripting with bash
  <https://aojanzen.github.io/blog/html/2022/05/25/scriptingwithbash.html>`_

**Introduction to Python**

* `Introduction to Python
  <https://aojanzen.github.io/blog/html/2022/05/28/introductionpython.html>`_

**The Hacker Methodology**

* `The Five Stages of Ethical Hacking
  <https://aojanzen.github.io/blog/html/2022/05/28/fivestagesofethicalhacking.html>`_

**Information Gathering (Reconnaissance)**

* `An Overview of Passive Recon(naissance)
  <https://aojanzen.github.io/blog/html/2022/05/28/passivereconnaissanceoverview.html>`_
* `Identifying Our Target
  <https://aojanzen.github.io/blog/html/2022/05/28/identifyingourtarget.html>`_
* `Discovering Email Adresses
  <https://aojanzen.github.io/blog/html/2022/05/28/discoveringemailadresses.html>`_
* `Gathering Breached Credentials with Breach-Parse
  <https://aojanzen.github.io/blog/html/2022/05/29/gatheringbreachedcredentials.html>`_
* `Hunting Breached Credentials with DeHashed
  <https://aojanzen.github.io/blog/html/2022/05/30/huntingbreachedpasswordswithdehashed.html>`_
* `Hunting Subdomains (Parts 1 and 2)
  <https://aojanzen.github.io/blog/html/2022/06/01/huntingsubdomains.html>`_
* `Identifying Website Technologies
  <https://aojanzen.github.io/blog/html/2022/06/01/identifyingwebsitetechnologies.html>`_
* `Information Gathering with Burp Suite
  <https://aojanzen.github.io/blog/html/2022/06/02/informationgatheringwithburpsuite.html>`_
* `Google Fu <https://aojanzen.github.io/blog/html/2022/06/02/googlefu.html>`_
* `Utilizing Social Media
  <https://aojanzen.github.io/blog/html/2022/06/03/utilizingsocialmedia.html>`_

**Scanning & Enumeration**

* `Installing Kioptrix
  <https://aojanzen.github.io/blog/html/2022/06/03/installingkioptrix.html>`_
* `Scanning with Nmap <https://aojanzen.github.io/blog/html/2022/06/03/scanningwithnmap.html>`_
* `Enumerating HTTP and HTTPS
  <https://aojanzen.github.io/blog/html/2022/06/04/enumeratinghttpandhttps.html>`_
* `Enumerating SMB
  <https://aojanzen.github.io/blog/html/2022/06/05/enumeratingsmb.html>`_
* `Enumerating SSH
  <https://aojanzen.github.io/blog/html/2022/06/09/enumeratingssh.html>`_
* `Researching Potential Vulnerabilities
  <https://aojanzen.github.io/blog/html/2022/06/06/researchingpotentialvulnerabilities.html>`_

**Vulnerability Scanning with Nessus**

* `Scanning with Nessus
  <https://aojanzen.github.io/blog/html/2022/06/09/scanningwithnessus.html>`_

**Exploitation Basics**

* `Reverse Shell vs Bind Shell
  <https://aojanzen.github.io/blog/html/2022/06/08/reverservsbindshell.html>`_
* `Staged vs Non-Staged Payloads
  <https://aojanzen.github.io/blog/html/2022/06/09/stagedvsnon_stagedpayloads.html>`_
* `Gaining Root with Metasploit
  <https://aojanzen.github.io/blog/html/2022/06/10/gainingrootwithmetasploit.html>`_
* `Manual Exploitation
  <https://aojanzen.github.io/blog/html/2022/06/11/manualexploitation.html>`_
* `Brute Force Attacks
  <https://aojanzen.github.io/blog/html/2022/06/12/bruteforceattacks.html>`_
* `Credential Stuffing and Password Spraying
  <https://aojanzen.github.io/blog/html/2022/06/15/credentialstuffingandpasswordspraying.html>`_


Other
-----

**SQL Injection**

* https://www.geeksforgeeks.org/authentication-bypass-using-sql-injection-on-login-page/
* https://www.hackingarticles.in/beginner-guide-sql-injection-part-1/
* https://www.tutorialspoint.com/sqlite/sqlite_injection.htm
* https://www.ptsecurity.com/ww-en/analytics/knowledge-base/how-to-prevent-sql-injection-attacks/
* https://www.exploit-db.com/papers/17934
* https://portswigger.net/web-security/reference/obfuscating-attacks-using-encodings
* https://websec.ca/kb/sql_injection
* https://bobby-tables.com/


**Reverse Engineering**

* https://www.codementor.io/@packt/reverse-engineering-a-linux-executable-hello-world-rjceryk5d


**Python Vulnerabilities**

* https://www.geeksforgeeks.org/vulnerability-input-function-python-2-x/
* https://intx0x80.blogspot.com/2017/05/python-input-vulnerability_25.html
* https://medium.com/swlh/hacking-python-applications-5d4cd541b3f1
* https://itnext.io/common-python-security-problems-ffedbae7b11c

..
    Computer Networks
    -----------------

    **TCM Security, Network refresher:**

    * IP addresses: ifconfig (inet vs inet6 addresses for IP V4 [decimal notation,
    4 bytes/32 bits] and IP V6 [hexadecimal notation, 128 bits]), we are running
    out of IP V4 addresses, but NAT (Network Address Translation) helps to find
    an IP address for each computer through use of private IP addresses
    (class C: 192.168.x.x., class A: 10.x.x.x., class B:
    172.16.x.x...172.31.0.0), IP routing is on layer 3 of the OSI model

    * MAC address (Media Access Control): 6 bytes, network interface cards and
    switches communicate on layer 2 via MAC addresses; first 3 bytes identify
    network card manufacturer (ifconfig: Hardware address, manufacturer can be
    identified online)

    * Transport layer (OSI layer 4): TCP, transmission control protocol, connection
    oriented for reliability; UDP: user datagram protocol, connectionless protocol
    for fast connection with less emphasis on reliability; TCP is scanned more
    often (SYNi > SYN-ACK > ACK); ports: http (port 80), https (port 443);
    example: use wireshark to capture 3-way handshake

    * Common ports and protocols via TCP: port 21 FTP, port 22 SSH (encrypted),
    port 23 Telnet, port 25 SMTP, port 53 DNS (resolving names to ip addresses),
    port 80 HTTP, port 443 HTTPS (encrypted), port 110 POP3, port 143 IMAP and --
    most often used when scanning -- ports 139 and 445 SMB (Windows file shares);
    protocols via UDP: port 53 DNS, ports 67/68 DHCP, port 69 TFTP (trivial FTP),
    port 161 SNMP
