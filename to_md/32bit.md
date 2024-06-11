# Running Autoplot on a 32 bit Java

Java's write-once run-anywhere mantra breaks down when you need lots of
memory, as is often the case with Autoplot. The problem is even when a
machine has lots of physical memory, a 32 bit JVM can only access 1GB of
memory.

Making the problem worse is on some platforms the Java process is only
allocated 256MB of memory, so this limit is encountered all the more
quickly.

With more and more machines having 64 bit memory, why is this a problem?
Oracle doesn't do much to encourage use of the 64 bit JVM, and it's easy
to have 32 bit Java installed without realizing it. If you have control
over which Java platform is used, make sure the 64 bit JVM is installed.

## Running Autoplot with 64 bits

Even if your browser is a 32 bit browser, 64 bit Java can still be
launched from it. TODO: instructions for different platforms.

The 64 bit JVM is available from Oracle's website:
<http://www.oracle.com/technetwork/java/javase/downloads/index.html>.
The JDK or JRE is needed. (JDK is used if you will be developing new
Java applications, and the JRE will only run existing applications with
Webstart or in Jar files.) Proceed following links, but on the downloads
page, be sure to get an "x64" version and not a "x86" version.
