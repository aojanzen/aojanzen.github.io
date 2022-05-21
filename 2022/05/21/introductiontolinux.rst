Introduction to Linux
=====================
The following notes are based on TCM Security's 'Practical Ethical Hacking'.
They refer to the Kali Linux operating system.

.. more::

Exploring Kali Linux
--------------------
Kali Linux is a Linux distribution specifically put together for ethical
hacking. It is based on Debian. The structure of the installed hacking tools is
ordered in the way a penetration test is typically conducted from information
gathering at the beginning to report writing at the end.


Sudo Overview
-------------
In earlier versions of Kali, there was an administrator account called "root",
which had all privileges, which again posed some security risks. Now a user
named "kali" with limited access rights is provided by default, which must use
a command called "sudo" (short for "super used do") to elevate the user rights
temporarily to execute a specific command.

**Example:** ``cat /etc/shadow`` will not work with normal access rights.
Instead, ``sudo cat /etc/shadow`` works, but has to be member of a sudo'ers
group and enter one's password.


.. image:: sudo.png
   :scale: 100%


``sudo su`` will permanently switch user (su) to root, but this is not
best security praxis and therefore not recommended for general work. One should
use ``sudo`` instead and just change to root if the situation requires. If one
opens a new tab from a terminal window with root, the user of the new tab will
be kali again.


Navigating the File System
--------------------------
In Linux you can -- just as in Windows -- use a GUI to navigate around the
filesystem, but as a pentester you will often work in a terminal window.

Linux is case sensitive, i.e. "folder", "Folder" and "FOLDER" are three
distinct names!


.. table:: Linux file system navigation
   :widths: auto

   =========================== ====================================================
    Command                                 Function
   =========================== ====================================================
    pwd                         Print working directory
    cd <dir>                    Change directory to <dir>
    cd ..                       Change to parent directory
    ls or ls <dir>              List contents of current directory or of <dir>
    mkdir <dir>                 Make a directory named <dir> in the current folder
    cp <source> <dest>          Copy file <source> to <dest>
    mv <source> <dest>          Move **or** rename file <source> to <dest>
    rm <file>                   Remove file <file>
   =========================== ====================================================


The TAB key can be used to complete file names. If the file name is not
unambiguous yet, hitting the TAB key twice will display a list with the
possible files that match what has been entered so far. The UP and DOWN arrow
keys can be used to navigate through the history of commands entered in the
terminal window, so that commands that are used several times do not have to be
typed in again and again.

One can reference folders beginning with the root directory (/). It is not
necessary to navigate to the respective directory first before, e.g. a ls
command is executed. The ~ is a shortcut for the current user's home folder.
Just entering ``cd`` without specifying a folder will change into the user's
home directory.

Hidden files and folders are displayed with ``ls -la``. Hidden
files and folders have names that begin with a period (e.g. ``.bashrc``).
















.. author:: default
.. categories:: none
.. tags:: none
.. comments::
