Hunting Breached Credentials with DeHashed
==========================================
TCM demonstrates a `website <https://dehashed.com/>`_ called ``DeHashed.com``,
which is only available as a paid service and can only be paid in
cryptocurrency.

.. more::

TCM points out that the material taught in the "Practical Ethical Hacking"
can change in the details, e.g. a website might not be available any more, but
the course is about the methodology in general, not about particular tools. One
can usually find a replacement if one service is not available any more.

``DeHashed.com`` also provides access to leaked user credentials, but it is
more powerful than ``breach-parse``, and the database is updated regularly.

The website allows the user to search for many different parameters, e.g. email
address, username, IP, name, postal address, phone number, or conduct a domain
scan. Credentials found for an email address can be cross checked with other
search results to extend the usability, e.g. if two users with a similar
username and identical passwords are found for two domains, one might have
found a work and a private email address with the same password. That is just
one example how one can exploit patterns to extend the chances that one can break
into the target in some way. Google search for a password might also reveal
additional insight.

When a search like this is conducted, one has to write detailed documentation
for the customer so that the procedure that allowed the pentester to get access to
the target system can be repeated by the customer.

``DeHashed.com`` also shows hash values for passwords, which one can look for
on another `webpage <https://hashes.org>`_ called ``hashes.org`` where one can
look up hash values to find the password that they relate to. However, the site
is down at the moment (2022-05-30).

In general, the message of this video is that one should look for additional
clues to cross-link credentials to other stuff that one can find on the
internet or in databases.

.. author:: default
.. categories:: none
.. tags:: none
.. comments::
