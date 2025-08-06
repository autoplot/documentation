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
