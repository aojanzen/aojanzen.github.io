picoCTF: Fresh Java
===================

Another CTF challenge from picoCTF 2022 for 200 points.

.. more::

The task here was to decompile a Java class file and interpret the source code:

    **Description:**

    Can you get the flag? Reverse engineer this
    `Java program <https://artifacts.picoctf.net/c/209/KeygenMe.class>`_.

    **Hints:**

    Use a decompiler for Java!


**Solution:**

There are online and offline decompilers that reproduce Java source code from a
class file. I have used this `online decompiler <http://www.javadecompilers.com>`_
for this task.

If you upload the provided class file and decompile it you get the following
output:

.. code:: Java

    import java.util.Scanner;

    // 
    // Decompiled by Procyon v0.5.36
    // 

    public class KeygenMe
    {
        public static void main(final String[] array) {
            final Scanner scanner = new Scanner(System.in);
            System.out.println("Enter key:");
            final String nextLine = scanner.nextLine();
            if (nextLine.length() != 34) {
                System.out.println("Invalid key");
                return;
            }
            if (nextLine.charAt(33) != '}') {
                System.out.println("Invalid key");
                return;
            }
            if (nextLine.charAt(32) != '0') {
                System.out.println("Invalid key");
                return;
            }
            if (nextLine.charAt(31) != 'f') {
                System.out.println("Invalid key");
                return;
            }
            if (nextLine.charAt(30) != '9') {
                System.out.println("Invalid key");
                return;
            }
            if (nextLine.charAt(29) != '5') {
                System.out.println("Invalid key");
                return;
            }
            if (nextLine.charAt(28) != 'c') {
                System.out.println("Invalid key");
                return;
            }
            if (nextLine.charAt(27) != '6') {
                System.out.println("Invalid key");
                return;
            }
            if (nextLine.charAt(26) != '2') {
                System.out.println("Invalid key");
                return;
            }
            if (nextLine.charAt(25) != '1') {
                System.out.println("Invalid key");
                return;
            }
            if (nextLine.charAt(24) != '_') {
                System.out.println("Invalid key");
                return;
            }
            if (nextLine.charAt(23) != 'd') {
                System.out.println("Invalid key");
                return;
            }
            if (nextLine.charAt(22) != '3') {
                System.out.println("Invalid key");
                return;
            }
            if (nextLine.charAt(21) != 'r') {
                System.out.println("Invalid key");
                return;
            }
            if (nextLine.charAt(20) != '1') {
                System.out.println("Invalid key");
                return;
            }
            if (nextLine.charAt(19) != 'u') {
                System.out.println("Invalid key");
                return;
            }
            if (nextLine.charAt(18) != 'q') {
                System.out.println("Invalid key");
                return;
            }
            if (nextLine.charAt(17) != '3') {
                System.out.println("Invalid key");
                return;
            }
            if (nextLine.charAt(16) != 'r') {
                System.out.println("Invalid key");
                return;
            }
            if (nextLine.charAt(15) != '_') {
                System.out.println("Invalid key");
                return;
            }
            if (nextLine.charAt(14) != 'g') {
                System.out.println("Invalid key");
                return;
            }
            if (nextLine.charAt(13) != 'n') {
                System.out.println("Invalid key");
                return;
            }
            if (nextLine.charAt(12) != '1') {
                System.out.println("Invalid key");
                return;
            }
            if (nextLine.charAt(11) != 'l') {
                System.out.println("Invalid key");
                return;
            }
            if (nextLine.charAt(10) != '0') {
                System.out.println("Invalid key");
                return;
            }
            if (nextLine.charAt(9) != '0') {
                System.out.println("Invalid key");
                return;
            }
            if (nextLine.charAt(8) != '7') {
                System.out.println("Invalid key");
                return;
            }
            if (nextLine.charAt(7) != '{') {
                System.out.println("Invalid key");
                return;
            }
            if (nextLine.charAt(6) != 'F') {
                System.out.println("Invalid key");
                return;
            }
            if (nextLine.charAt(5) != 'T') {
                System.out.println("Invalid key");
                return;
            }
            if (nextLine.charAt(4) != 'C') {
                System.out.println("Invalid key");
                return;
            }
            if (nextLine.charAt(3) != 'o') {
                System.out.println("Invalid key");
                return;
            }
            if (nextLine.charAt(2) != 'c') {
                System.out.println("Invalid key");
                return;
            }
            if (nextLine.charAt(1) != 'i') {
                System.out.println("Invalid key");
                return;
            }
            if (nextLine.charAt(0) != 'p') {
                System.out.println("Invalid key");
                return;
            }
            System.out.println("Valid key");
        }
    }

One can easily see that the Java code reads a key from the command line and
checks first the length of the entered key, followed by a backwards comparison
letter by letter to check if the entered string is the same as a sought
secret. That secret is our flag. You just have to go from the end of the
source code backwards to put the flag back together:

``picoCTF{700l1ng_r3qu1r3d_126c59f0}``


.. author:: default
.. categories:: none
.. tags:: none
.. comments::
