Enumerating SSH
===============
The ``nmap`` scan has revealed that SSH (``OpenSSH 2.9p2``) runs on the open
port 22. If our scan does not show a software version, we can try to figure it
out by connecting to the open port with ``ssh``.

.. more::

The ``ssh`` version is already so old that we encounter some problems. We have
to chose a key exchange method and a cipher manually. TCM has picked
``-oKex=diffie-hellman-group1-sha1`` and ``-c aes128-cbc``. The latter is not
available in my setup, therefore I have chosen ``-c ssh-rsa``. This did not
work either. TCM states in his video that the purpose of the exercise was to
check if a "banner" is displayed when we try to log into the SSH service, which
was not the case on the Kioptrix machine.


.. author:: default
.. categories:: none
.. tags:: none
.. comments::
