A [JNLP](http://en.wikipedia.org/wiki/Java_Web_Start) file (Java Network
Launching Protocol) is an XML file that is used to allow a user to
automatically start a Java program by selecting a link in a web browser.
The program will be downloaded and installed if it has not been
previously installed or if an update is required.

The best way to create Autoplot JNLP files is to use our web service
described on this page. (Server-side code is maintained in repository at
in directory `VirboAutoplot/src/external`).

The web service allows links to be created that cause Autoplot to launch
in a certain configuration. For example, if the following link is placed
on a web page

<http://autoplot.org/autoplot.jnlp?http://autoplot.org/data/autoplot.xml?BGSM>

and clicked, Autoplot will open and render the URI

<http://autoplot.org/data/autoplot.xml?BGSM>

# Basic

&lt;http://autoplot.org/autoplot.jnlp&gt;`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`  
&lt;http://autoplot.org/autoplot.jnlp?URI&gt;`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`  
<http://autoplot.org/autoplot.jnlp?open=URI>  
&lt;http://autoplot.org/autoplot.jnlp?version=VERSION&gt;`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`  
&lt;http://autoplot.org/autoplot.jnlp?version=VERSION&amp;URI&gt;`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`  
<http://autoplot.org/autoplot.jnlp?version=VERSION&open=URI>

&lt;http://autoplot.org/autoplot.jnlp?uri=URI&gt;`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;(deprecated)`  
&lt;http://autoplot.org/autoplot.jnlp?version=VERSION&amp;uri=URI&gt;`&nbsp;&nbsp;&nbsp;(deprecated)`

where `URI` is the full URI to be placed in the address bar when
Autoplot starts and `VERSION` is any directory listed at
<http://autoplot.org/jnlp>. See
[Main\_Page\#Formats\_Read](Main_Page.md#formats-read "wikilink") and below
for example links. Each time a link is clicked a new instance of
Autoplot is started. (Eventually there will be an option to allow the
user to click a link and have the URI plotted above, below, or over an
existing plot if Autoplot is already running.)

**Examples**

  - <http://autoplot.org/autoplot.jnlp?http://autoplot.org/data/autoplot.xml?BGSM>
  - <http://autoplot.org/autoplot.jnlp?open=http://autoplot.org/data/autoplot.cdf?BGSM>
  - <http://autoplot.org/autoplot.jnlp?version=v2013a_8&http://autoplot.org/data/autoplot.cdf?BGSM>
  - <http://autoplot.org/autoplot.jnlp?version=v2013b_1&http://autoplot.org/data/autoplot.cdf?BGSM>
  - <http://autoplot.org/autoplot.jnlp?version=latest&open=http://autoplot.org/data/autoplot.cdf?BGSM>

# Advanced

A jnlp file may be requested that will launch Autoplot in a manner that
is identical to as if it were started from the command line with any of
the available command line options. The arguments for the service are
the same as the long form of the command line options. For example,

```
wget -O - "http://autoplot.org/autoplot.jnlp?main-class=org.autoplot.pngwalk.PngWalkTool1&nativeLAF=true&qualityControl=true" > auto.jnlp
javaws auto.jnlp
```
is the same as

`wget&nbsp;`&lt;http://autoplot.org/jnlp/latest/autoplot.jar&gt;  
```
java -cp autoplot.jar org.autoplot.pngwalk.PngWalkTool1 --nativeLAF=true --qualityControl=true
```
## Memory Limits

By default all the .jnlp files specify a 1G memory limit for Autoplot.
This is proving to be quite limiting, and to ease this you can now
request a JNLP file with a larger memory allowance:

```
wget -O - "http://autoplot.org/autoplot.jnlp?max-heap-size=4G" > auto.jnlp
```
Note that some platforms, specifically Windows XP, don't allow more
memory than the default 1024K, so please realize that products made on a
larger Autoplot may not be usable elsewhere.

Examples:

  - <http://autoplot.org/autoplot.jnlp?max-heap-size=2G>
  - <http://autoplot.org/autoplot.jnlp?max-heap-size=2G&version=devel&open=>

## PngWalkTool

The options for `main-class=org.autoplot.pngwalk.PngWalkTool1` are

```
template=[URI] start with this URI template (must be the last argument in the link)
nativeLAF=[true|false] use the system look and feel (default: true)
mode=[grid|filmStrip|covers|contextFlow] initial display mode
goto=[2010-01-01] start display at the beginning of this range
qualityControl=[true|false] enable quality control review mode (default: true)
```
Example link (note that the `template` argument is last):

<http://autoplot.org/autoplot.jnlp?main-class=org.autoplot.pngwalk.PngWalkTool1&nativeLAF=true&qualityControl=true&mode=grid&goto=2010-01-01&template=http://autoplot.org/data/pngwalk/product_$Y$m$d.png>

or from the command line

```
wget -q -O auto.jnlp 'http://autoplot.org/autoplot.jnlp?main-class=org.autoplot.pngwalk.PngWalkTool1&nativeLAF=true&qualityControl=true&mode=grid&goto=2010-01-01&template=http://autoplot.org/data/pngwalk/product_$Y$m$d.png'
javaws auto.jnlp
```
## AutoplotUI

The options for `main-class=org.virbo.autoplot.AutoplotUI` are

```
bookmarks=[URL] bookmark URL to load 
open=[URI] open this URI (must be the last argument in the link)
logConsole=[true|false] enable log console (default: false)
scriptPanel=[true|false] enable script panel (default: false)
script=[URI] run this script after starting.  Arguments following are passed into the script as sys.argv
nativeLAF=[true|false] use the system look and feel
print=[URI] print this URI
port=[NUM] enable scripting via this port
```
Example (note that the `open` argument is last):

