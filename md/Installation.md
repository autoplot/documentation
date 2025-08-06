# Installation

Autoplot can be found at <https://autoplot.org/latest/>. The "Start
Autoplot" link brings up a download page for the latest release. The
software is available separately for each type of computer. A
"single-jar" version is available for those who already have Java on
their machines. Development releases with new features and bug fixes are
made about once a week. Though each release is tested using a suite of
automatic tests, these development releases may contain new bugs which
could interfere use, and should not be used in production environments.
Production-quality releases have been more thoroughly tested, and are
made monthly.

WebStart has been deprecated by Oracle and other methods should be used.

On Macs, a .dmg file which contains the Autoplot release and a bundled
version of the Java Runtime Environment is used. This 98Mb download is
signed and should run on any newer Mac. (The Install4J software used to
build each release supports both Intel and M1 Macs.)

Windows machines can use the "exe" release. For now you will need to
acknowledge the untrusted signature and "run anyway" to use it. Trust is
based on the number of people running it, and Microsoft does not trust
the certificate at this time.

On Linux machines, the single-jar release can be used as well. We've
prepended a bash launch script at its beginning so that if the
downloaded jar's executable bit is set, it can be launched like any
other executable file. There are also .rpm and .dmg releases which are
available, but the .rpm version has not been thoroughly tested.

Autoplot will run on 32 bit Java 8, but memory will be limited to 1GB.  This
is  done by using the single-jar release.

## Failsafe Installation

### Windows

Download <https://autoplot.org/jnlp/latest/autoplot.jar> to your desktop
and then double click it. Autoplot should launch if you have Java
installed.

Some versions of Java will run with limited memory (e.g. 192MB instead
of 1GB), so check that this will be sufficient; if not, start using the
command line using:

```
java -Xmx4G -jar autoplot.jar
```
### Linux and OS-X

On the command line, download Autoplot using either wget or curl:

`wget -N https://autoplot.org/jnlp/latest/autoplot.jar`
`curl -O https://autoplot.org/jnlp/latest/autoplot.jar`

and then start it with

```
java -jar autoplot.jar  
```
Note that IcedTea/OpenJDK versions of Java may work, but we recommend
using Oracle's version of Java
[2 https://www.java.com/en/download/manual.jsp](https://www.java.com/en/download/manual.jsp).

To launch Autoplot with more memory, use

```
java -Xmx16G -jar autoplot.jar
```
### 32bit JVMs

A 32 bit JVM can be used, but it must be run with 1GB of memory or less.
A 64 bit JVM is recommended.
