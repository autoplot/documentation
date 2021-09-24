Audience: IDL users wishing to plot data in Autoplot from IDL.

# Introduction 
The IDL program applot is intended to allow autoplot to replace many cases where IDL's plot command would be used.  The goal is that
~~~~~
IDL> plot, x, y
~~~~~

would be replaced with 
~~~~~
IDL> applot, x, y
~~~~~
and the data is packed up and sent over to Autoplot for plotting.  This plot in Autoplot is then interactive and avoids disturbing IDL's state.

Here is the script which should be run in IDL: https://svn.code.sf.net/p/autoplot/code/autoplot/trunk/VirboAutoplot/src/external/applot.pro. 
This should be downloaded and compiled in the IDL session.  Autoplot is then started, and its server enabled using 
Options&rarr;Enable Feature&rarr;Server, and use the default port 12345.

# Example use
~~~~~
 Unix> wget https://autoplot.svn.sourceforge.net/svnroot/autoplot/autoplot/trunk/VirboAutoplot/src/external/applot.pro
 Unix> idl
 IDL> .comp applot
 IDL> ; ensure that the server mode is enabled on Autoplot via [menubar]->Options->Enable Feature->Server
 IDL> applot, dist(200)
 IDL> applot, findgen(200), sin(findgen(200))
 IDL> applot, findgen(200), sin(findgen(200)), xunits='seconds since 2001-011T00:00'
~~~~~

# Discussion 
## ow it works 
The script works by saving the data into a das2stream, which is das2/Autoplot's serialized data format, and sending over to 
Autoplot via the /tmp directory.  Autoplot's server is used to tell it to plot the file.

# Problems 
* applot.pro has code to start up Autoplot from IDL that should be updated.  It assumes Windows and 
a fixed path for java, and the CLASSPATH variable isn't used.
