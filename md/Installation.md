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

The .exe installer will put Autoplot on your system, replacing any old 
versions which were already installed.  Download the .exe and run it,
and you will need to accept the security warning for software where
a developer fee has not been paid to Microsoft.  Otherwise it should 
install like other software.

# Macs
The .dmg installer should be downloaded and launched, which will open a window 
where Autoplot should be dragged into the applications folder.  When run,
it will warn that the software was downloaded from the web and you will need
to confirm the operation.  

# .rpm 
On Redhat-based systems, superuser (root) can download and install the .rpm.  When superuser access is
not available, then the following can be used to install it anywhere:
```
rpm2cpio ~/Downloads/autoplot_linux_2024_12.rpm | cpio -idv --directory=~/local/opt/autoplot-dev/
```

# .deb
On Ubuntu-based systems, superuser (root) can download and install the .deb, as with the RPM.
The command gdebi is used to install when root access is not available.

### Single-Jar release
A "single jar" is created as well and is often the easiest method for running Autoplot.  On the 
command line, download Autoplot using either wget or curl:

`wget -N https://autoplot.org/jnlp/latest/autoplot.jar`
`curl -O https://autoplot.org/jnlp/latest/autoplot.jar`

and then start it with

```
java -jar autoplot.jar  
```
Java 8 or newer is required.  Note that the third-party code to read PDS4 uses a library which was removed
from Java 11, and will not work.  This will be addressed soon.

To launch Autoplot with more memory, use

```
java -Xmx16G -jar autoplot.jar
```
### 32bit JVMs

A 32 bit JVM can be used, but it must be run with 1GB of memory or less.  A 64 bit JVM is recommended.
Note the single-jar release must be used with a 32-bit Java 8 (or newer) runtime.
