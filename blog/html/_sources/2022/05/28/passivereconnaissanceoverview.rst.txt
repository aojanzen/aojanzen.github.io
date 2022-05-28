An overview of Passive Recon(naissance)
=======================================
The following physical and social information can be helpul:

* Location information: satellite images, drone recon, building layout (badge
  readers, break areas, security, fencing)
* Job information: employees (name, job title, phone number, manager, etc.),
  pictures (badge photos, desk photos, computer photos, etc.)

This type of OSINT will not be covered in depth in the "Practical Ethical
Hacking" course. Instead, the following aspects of web and host assessments
will be covered in more depth:

* Target validation: double-check if the website or IP address that the
  customer has provided is correct ("Darknet Diaries" `podcast episode
  <https://darknetdiaries.com/transcript/22/>`_ by Rob Fuller). Tools for this
  phase: WHOIS, nslookup, dnsrecon
* Finding subdomains on the target website. Tools: Google Fu, dig, Nmap,
  Sublist3r, Bluto, crt.sh, etc.
* Fingerprinting: find out what services are running on a website or host, what
  ports are open. Tools: Nmap, Wappalyzer, WhatWeb, BuiltWith, Netcat
* Data breaches: using data (login credentials) that has been leaked in earlier
  data thefts is by far the most common way of getting into networks. Tools:
  HaveIBeenPwned, Breach-Parse, WeLeakInfo

Passive reconnaissance means gathering information that is already available on
the internet, whereas active scanning begins with scanning of hosts. Today, in
external pentests it is most of the time not possible to just scan for
vulnerabilities and exploit one to get into a network, therefore scanning and
enumeration are extremely important, especially looking for breached data. The
better you are at information gathering, the more successful you are going to
be as a hacker.


.. author:: default
.. categories:: none
.. tags:: none
.. comments::
