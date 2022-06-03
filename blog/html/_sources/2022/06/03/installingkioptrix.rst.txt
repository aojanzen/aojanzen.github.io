Installing Kioptrix
===================
This is the beginning of the "Scanning and Enumeration" section of "Practical
Ethical Hacking". We will use a vulnerable virtual machine called ``Kioptrix``.

.. more::

It is easy to find the virtual machine with ``Google``. Level 1 is available for
download on `VulnHub <https://www.vulnhub.com/entry/kioptrix-level-1-1,22/>`_.
VulnHub offers many more virtual machines that can be used to train pentesting.

The ``ova`` file can also be downloaded from `TCM Sec <https://tcm-sec.com/kioptrix>`_.
When the file has been downloaded, one just has to open it with VirtualBox or
VMWare. The NIC has to be set to ``NAT``, the memory should be set to at least
256 MB, 512 MB would be fine as well. Login credentials are username ``john``
and password ``TwoCows2``. Once we are logged in, the machine can run in the
background, and we will switch to our virtual Kali machine and try to penetrate
the Kioptrix machine.


.. author:: default
.. categories:: none
.. tags:: none
.. comments::
