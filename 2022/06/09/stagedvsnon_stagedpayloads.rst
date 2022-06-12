Staged vs Non-Staged Payloads
=============================
A **payload** is code that is sent to a target machine to exploit a vulnerability
and get a shell on that machine. There are different types of payloads: Windows
payloads, Linux payloads, Meterpreter payload, Python payload, etc. They can be
staged and non-staged.

.. more::

**Staged payloads:**

* Payload is sent in stages
* Can be less stable

Example: ``windows/meterpreter/reverse_tcp``

**Non-staged payloads:**

* Sends exploit shellcode all at once
* Is larger in size and will not always work

Example: ``windows/meterpreter_reverse_tcp``

If we are sure that we using the right kind of exploit, but it does not work
with one type of payload (staged or unstaged), we should always try the other
one as well.


.. author:: default
.. categories:: none
.. tags:: none
.. comments::
