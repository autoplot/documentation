Purpose: Give an overview of using Autoplot to do background processing.

Audience: Data managers and advanced Autoplot users looking to include
Autoplot in their processing chain.

# Introduction

Primarily Autoplot is an interactive plotting tool, allowing users to
view their data by adjusting ranges trivially and slicing data to view
high-rank data. From the beginning, lots of work has been done to
support batch processing in a headless environment. The trick is to make
an interactive tool behave nicely, and this document covers this.

Scripts modify application state, and then the waitUntilIdle method is
called to block the script until Autoplot finally implements the
application state.

# Java in Headless Mode

Java processes are run in headless mode with the command line argument:
-Djava.awt.headless=true:

```
java -Djava.awt.headless=true -jar autoplot.jar
```
In these examples, $JAVA is a Sun/Oracle Java version 1.8 or newer.
$AUTOPLOT is the single-jar release of Autoplot, found at
<http://autoplot.org/jnlp/latest/autoplot.jar>.

# Headless Create Pngwalk

One of the first applications for running Autoplot in this manner is to
produce PNGWalks of a product. For RBSP instrument teams, data comes in
nightly and we want to generate pngwalks for use the next day.

`wget&nbsp;`&lt;http://autoplot.org/jnlp/latest/autoplot.jar&gt;  
```
java -Djava.awt.headless=true \
  -cp autoplot.jar \
  org.autoplot.pngwalk.CreatePngWalk --timeFormat='$(o,id=rbspa-pp)' \
  --timeRange=orbit:rbspa-pp:70-99 --vap=/home/jbf/ct/hudson/vap/rbsp_events.vap -o=pngwalk-rbsp/ --version=v1.2 --update
```
This generates PNG images for the product
/home/jbf/ct/hudson/vap/rbsp\_events.vap each day, only calculating the
pngs that are missing.

# Jenkins

Autoplot is tested continually in hundreds of end-to-end tests, all in a
catch environment by the Java web application Hudson (a.k.a. Jenkins).

# Scripts

Jython scripts can be run using the --script argument, and --headless
can be used as well:

```
$JAVA -jar $AUTOPLOT --headless --script /tmp/sayHello.jy
```
where here's the /tmp/sayHello.jy script:

```
print 'hello!'
```
and example values for $JAVA and $AUTOPLOT are:

```
JAVA=/usr/local/jre1.8.0/bin/java
```
`wget&nbsp;`&lt;http://autoplot.org/jnlp/latest/autoplot.jar&gt;  
```
AUTOPLOT=autoplot.jar
```
To remove some of the complexity of the full application, a more direct
method, better suited for servers, would be the org.autoplot.JythonMain
class:

```
$JAVA -cp $AUTOPLOT -Djava.awt.headless=true org.autoplot.JythonMain --script /tmp/sayHello.jy
```
In these examples, $JAVA is a Sun/Oracle Java version 1.8 or newer.
$AUTOPLOT is the single-jar release of Autoplot, found at
<http://autoplot.org/jnlp/latest/autoplot.jar>.

For CDF file reading, the C-based reader is not used, and the pure-Java
one is used to support vap+cdf URIs. This should work identically, but
does use more memory in some cases and is showing some issues on
Windows. The goal is to make this the preferred reader, however if the
C-based reader is needed, then native libraries can be linked in. This
is beyond the scope of the discussion here, and those interested should
contact the Autoplot users group at autoplot@groups.google.com.

# Credentials and \~/autoplot\_data/fscache/keychain.txt

Since often access is needed to restricted resources, the keychain file
was introduced to store credentials. Before its introduction, vap files
would have to put the credentials directly into the file, with URIs like
<http://theuser:thepass@autoplot.org/data/restrict/data.dat>. This is
clearly a security problem and unacceptable. The keychain file was
introduced to provide a mechanism where a batch process can get
credentials. If the file keychain.txt is found in the user's
\~/autoplot\_data/fscache/keychain.txt, then this file is read in and
credentials stored in the running session for use when the resource is
needed. Note this is only used when Autoplot's FileSystem libraries are
used. Readers that access data directly over http will not use the
keychain.txt file.

The keychain file has lines containing the URL and then the
<USER>:<PASSWORD> combination that provides access to each URL.

for example:

&lt;ftp://jbfaden@autoplot.org&gt;`&nbsp;jbfaden:mYPass@d`  
&lt;http://jbf@papco.org&gt;`&nbsp;&nbsp;&nbsp;jbf:easypass`

For convenience, Autoplot will generate the unprotected file with the
jython command with the script:

```
from org.das2.util.filesystem import KeyChain
KeyChain.getDefault().writeKeysFile()
```
Note only a minimal amount of thought has gone into this, so please be
careful with these facilities and use them at your own risk\!

# Apache Tomcat

Autoplot is used regularly with Apache Tomcat and Oracle's Glassfish.

# Autoplot Server

To support use in native web servers like Apache's HTTP server, the
command line org.autoplot.AutoplotDataServer is introduced for data.
org.autoplot.AutoplotServer sends out images.

