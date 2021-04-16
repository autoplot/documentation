# org.autoplot.test.Util
Util( )


***
<a name="pushContextMenu"></a>
# pushContextMenu
pushContextMenu( org.das2.graph.DasPlot c, java.lang.String[] items ) &rarr; JMenuItem

push the context menu item identified by the items.  This is a
 list of regular expressions identifying the levels.

### Parameters:
c - the focus plot
<br>items - labels, eg [ "Plot Style", "Series" ]

### Returns:
the JMenuItem found, which has been pushed.

<a href="https://github.com/autoplot/dev/search?q=pushContextMenu&unscoped_q=pushContextMenu">[search for examples]</a>

***
<a name="reportLogger"></a>
# reportLogger
reportLogger( java.util.logging.Logger l ) &rarr; void

print a report about the logger to stderr.

### Parameters:
l - a Logger

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=reportLogger&unscoped_q=reportLogger">[search for examples]</a>

***
<a name="waitUntilBusy"></a>
# waitUntilBusy
waitUntilBusy( int timeout, org.autoplot.dom.Application dom ) &rarr; void

wait until dom.controller.pendingChanges becomes true.

### Parameters:
timeout - timeout in milliseconds.
<br>dom - the application.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=waitUntilBusy&unscoped_q=waitUntilBusy">[search for examples]</a>

