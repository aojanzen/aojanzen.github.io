picoCTF: unpackme.py
====================

Another challenge from picoCTF 2022, worth 200 points.

.. more::

This time we need to reverse-engineer a Python script.

    **Description:**

    Can you get the flag? Reverse engineer this Python program. (No further hints
    given.)

This is the Python program that has to be reverse engineered:

.. code:: python

    import base64
    from cryptography.fernet import Fernet

    payload = b'gAAAAABiMD1Dt87s50caSunQlHoZqPOwtGNaQXexN-gjKwZeuLEN_-v6UcFJHVXOT4B6DcD1SB7cnd6yTcHg9e9LZCAeJY2cJ0r0sfyGPRiH60F-WbkyUjlAdDywI8RPdTpDYLuBmpZ_Kun-kHyTzMjeKR6R26Z4JITUS8n7Dj9X--9eNLajH6UuYD4GkjRACpsidl_8z33DlB86u_xDCMMm7HFK2oJTs8HG1fBex6enQsu0frUAJbx56DxhRvWawAysDMtLE50vaohrzkVV7Yaz4ClilwgfjQ=='

    key_str = 'correctstaplecorrectstaplecorrec'
    key_base64 = base64.b64encode(key_str.encode())
    f = Fernet(key_base64)
    plain = f.decrypt(payload)
    exec(plain.decode())

This code imports the cryptography library ``Fernet`` from Python's standard
library. Fernet is a module that can be used to implement a symmetric
encryption:

https://www.geeksforgeeks.org/fernet-symmetric-encryption-using-cryptography-module-in-python/

Perhaps the variable ``key_str`` contains the secret key to decrypt the
``payload``, which looks like base64 encoded binary data.

The last line of the program executes a piece of code that is handed over as a
parameter, which is the result of ``plain.decode()``. If we can just see this
string before the ``exec()`` function is called, we may already be able to get
the flag.

To get access to the sought string, I have simply executed every line of the
short program in the Python interpreter. (For longer programs one would use a
debugger and just set a stop point before the ``exec`` command. Spyder could be
used in such a case.)

.. code:: python

    # Python 3.7.3 (default, Mar 27 2019, 22:11:17)
    # [GCC 7.3.0] :: Anaconda, Inc. on linux
    # Type "help", "copyright", "credits" or "license" for more information.
    # >>>
    # >>>
    # >>> import base64
    # >>> from cryptography.fernet import Fernet
    # >>>
    # >>> payload = b'gAAAAABiMD1Dt87s50caSunQlHoZqPOwtGNaQXexN-gjKwZeuLEN_-v6UcFJHVXOT4B6DcD1SB7cnd6yTcHg9e9LZCAeJY2cJ0r0sfyGPRiH60F-WbkyUjlAdDywI8RPdTpDYLuBmpZ_Kun-kHyTzMjeKR6R26Z4JITUS8n7Dj9X--9eNLajH6UuYD4GkjRACpsidl_8z33DlB86u_xDCMMm7HFK2oJTs8HG1fBex6enQsu0frUAJbx56DxhRvWawAysDMtLE50vaohrzkVV7Yaz4ClilwgfjQ=='
    # >>>
    # >>> key_str = 'correctstaplecorrectstaplecorrec'
    # >>>
    # >>> key_base64 = base64.b64encode(key_str.encode())
    # >>> f = Fernet(key_base64)
    # >>> f
    # <cryptography.fernet.Fernet object at 0x7ff1628fb9b0>
    # >>>
    # >>> plain = f.decrypt(payload)
    # >>> plain.decode()
    # "\npw = input('What\\'s the password? ')\n\nif pw == 'batteryhorse':\n  print('picoCTF{175_chr157m45_8aef58d2}')\nelse:\n  print('That password is incorrect.')\n\n"
    # >>>

Now we can already see the flag in the last output. If you execute the script
and enter ``batteryhorse`` as the password, you get the following flag:

``picoCTF{175_chr157m45_8aef58d2}``


.. author:: default
.. categories:: none
.. tags:: none
.. comments::
