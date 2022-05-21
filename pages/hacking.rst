Hacking and Networks
====================

Hacking
-------

https://tcm-sec.com/so-you-want-to-be-a-hacker-2021-edition


**SQL Injection**

https://www.geeksforgeeks.org/authentication-bypass-using-sql-injection-on-login-page/

https://www.hackingarticles.in/beginner-guide-sql-injection-part-1/

https://www.tutorialspoint.com/sqlite/sqlite_injection.htm

https://www.ptsecurity.com/ww-en/analytics/knowledge-base/how-to-prevent-sql-injection-attacks/

https://www.exploit-db.com/papers/17934

https://portswigger.net/web-security/reference/obfuscating-attacks-using-encodings

https://websec.ca/kb/sql_injection

https://bobby-tables.com/


**Reverse Engineering**

https://www.codementor.io/@packt/reverse-engineering-a-linux-executable-hello-world-rjceryk5d


**Python Vulnerabilities**

https://www.geeksforgeeks.org/vulnerability-input-function-python-2-x/

https://intx0x80.blogspot.com/2017/05/python-input-vulnerability_25.html

https://medium.com/swlh/hacking-python-applications-5d4cd541b3f1

https://itnext.io/common-python-security-problems-ffedbae7b11c


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
