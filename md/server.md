Audience: Software wishing to use Autoplot from other software packages.

Purpose: Outline the server interface

# Introduction

Autoplot has a "server" mode where it is able to accept commands from a
socket, and possibly send back graphics. The interface is just a Jython
command line similar to that on the console tab, except that "telnet"
can be used to connect. Similarly, IDL can be used to connect to have
Autoplot render data.

# First Look

The server mode must first be enabled. Connections are only allowed from
the local machine, but there are clearly still security risks in opening
up a port which can accept commands. If Autoplot is already running,
then the server can be started with \[menubar\]&rarr;Options&rarr;&quot;Enable
Feature&quot;&rarr;Server, then use 12345 for the port and hit OK. Now use
telnet to experiment with the interface. For example:

```
spot5> telnet localhost 12345
Trying ::1...
Connected to localhost.
autoplot> plot( [1,2,3,4,5], title="My Data" )
autoplot> plot( '`<http://autoplot.org/data/autoplot.cdf?Magnitude>`' )
```

The external software might format data then tell Autoplot to plot the
data. For example,
<https://sourceforge.net/p/autoplot/code/HEAD/tree/autoplot/trunk/Autoplot/src/external/applot.pro>
is IDL software which will connect to Autoplot on the server plot and
send over data.

# Advanced Details

It may be necessary for Autoplot to issue a newline after the prompt is
sent, so that a client code can see that Autoplot is finished when
buffering prevents this. This can be done by resetting the prompt
property of ApplicationModel:

```
dom.controller.applicationModel.prompt='autoplot>\n'
```

Note that when the connection is broken, the server will shut down and
must be restarted.

