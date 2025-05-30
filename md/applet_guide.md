Development notes on using Autoplot as an applet. Recent examples:
[applet_demos](applet_demos.md)

Older examples: Showing timing
[1](http://aurora.gmu.edu/autoplot-applet/dist-packed/OnePanelApplet-bgloadAll.html).
Other [2](http://autoplot.org/applet/production/) and
[3](http://aurora.gmu.edu/autoplot-applet/dist-packed).

# Installation

Only a small number of DataSources support the security restrictions of
applets. These include: qds, d2s, tsds. The dataSetURL must be to the
same URL that the applet was loaded from.

## Basic

    <applet width="800" height="400" id="applet1" code="org.virbo.autoplot.AutoplotApplet" archive="AutoplotApplet.jar">
       <param name="dataSetURL" value="http://www.autoplot.org/data/alpha_proton_ratio.qds">          
    </applet>

## Testing Clients

Right now, only the Sun java plug-in for Mozilla firefox is supported.
This can be tested at: <http://www.java.com/en/download/testjava.jsp> We
intend to support other clients as well, including the OpenJDK plugin,
see [bug
ticket](http://sourceforge.net/tracker/?func=detail&aid=3219816&group_id=199733&atid=970682).

## Advanced: Pre-load

To load the Java Virtual Machine in the background after the page has
loaded but before the user has had a chance to initiate an applet
visualization, see
<http://aurora.gmu.edu/autoplot-applet/dist-packed/OnePanelApplet-bgloadAll.html>.

## Advanced: Compressed

The applet jar file can be compressed from 3 MB to 0.3 MB using
[pack200](http://java.sun.com/j2se/1.5.0/docs/guide/deployment/deployment-guide/pack200.html)
and [proguard](http://proguard.sourceforge.net/) (each give about a
factor-of-three compression). See most recent applet release at
[Autoplot_Change_Log](Autoplot_Change_Log.md) and select the html file named
AutoplotAppletCompressed.html. See page source for usage example.

The procedure for building Autoplot and the applet is described in
[build from source](Autoplot_from_source.md "wikilink"). The pack200 and
proguard steps have been added to the build process. A packed applet
requires a .htaccess file. See the file named htaccess.txt.

## Tips

  - Change applet memory settings:
    <http://www.duckware.com/pmvr/howtoincreaseappletmemory.html>
  - Clear cache on Linux with rm -rf \~/.java/deployment/cache
  - Clear cache on Windows with Control Panel -\> Java -\> General Tab
    -\> "Temporary Internet Files Section -\> Settings" -\> Delete Files
  - Clear cache on Mac using
    Finder-\>Applications-\>Utilities-\>Java-\>Java Preferences-\>Delete
    Files

# Parameters

See [api\#Common](api.md#common "wikilink") for the list of all parameters.
Applet parameters are specified as <param name="NAME" value="VALUE">

  - **splashImage** is the image to use as the preview as the applet
    initializes.
  - **clickCallback** is a javascript function to call with click info.
    <clickCallback>( plotid, xdatum, ydatum, xcanvas, ycanvas, clickType
    )
  - **statusCallback** the name of a javascript function to call with
    status. It should take one string argument, which will describe the
    status. These include:
      - **readParameters** the configuration parameters have been read
        in.
      - **dataSourceSet** the data source is resolved.
      - **dataSourceLoaded** the data is loaded.
      - **ready** the initial work is complete and the applet is waiting
        for user interaction.
  - **timeCallback** the name of a javascript function to call to
    indicate the current x-axis range. This is a string.
  - **clickCallback** The name of a javascript function which will get
    the location of clicks. For most recent test version, see the latest
    release at [Autoplot\_Change\_Log](Autoplot_Change_Log.md "wikilink")
    and select AutoplotAppletOnClick.html. See page source for usage
    example. Initial version:
    [4](http://www.sarahandjeremy.net/jeremy/applet/AutoplotApplet.html).
      - **onClick,label=Show Coordinates** onClick is a javascript
        routine name. Show Coordinates is the label in the context menu.
  - **contextOverview**=**on** (off is default.) Show two-panels, lower
    panel is context plot, upper panel is zoom in.

# Methods

Applet methods can be called from Javascript. For example, if the
applet's id is applet\_1, then in JavaScript, one can call

```
applet_1.setTimeRange( '2009-01-01' )
```
because the applet defines a public method setTimeRange that accepts a
string parameter.

  - **setTimeRange(String)**. The string is parsed as a time range and
    the x axis is set to the new range.
  - **setDataSetURL(String)**. Point the applet to a new data source.
  - **setCanvasFont(String)**. Reset the canvas font. (Broken in current
    release.)
  - **setDomNode( String name, String value )**. Uses Java introspection
    to set the value of the property identified. This uses the object
    serialization defined in QStream to parse strings into objects.
    Hopefully any type allowed in the dom tree will work here.

For example:

    setDomNode( 'timeRange', '2009-05-06' )
    setDomNode( 'plots[0].xaxis.log', 'true' )  # TODO: I think the indexed variables don't work presently.
    setDomNode( 'options.drawMinorGrid', 'true' )

  - **printDomNode( String name )** Uses Java introspection and
    QStream's serialize delegates to provide a string representation of
    the property. You cannot at this time get the string back because of
    limitations in how we use Javascript and java, but this provides a
    means of displaying the node in the java console. TODO: fix this
    limitation

<!-- end list -->

    printDomNode( 'timeRange' )
    printDomNode( 'plots[0].xaxis.log' )

When adding to the applet's API, the thread calling the applet is
considered a hostile thread and a security exception will be thrown when
a setter is called. Wrap the setter in a Runnable, then pass the
Runnable to SwingUtilities.invokeLater so the code is run from a trusted
thread.

# Development Notes

**Problems**

*Many of these problems have been fixed. These notes are kept for
reference only*

Load applet w/o page hang

*Note: This is no longer a problem. See
<http://aurora.gmu.edu/dist-packed/OnePanelApplet-bgload.html>*

In this example, <http://timeseries.org/applet/autoplota.htm>, jQuery +
a JavaScript setTimeout() call is used to make the applet jar files
loaded and the JVM is start after the page load is complete (and the
user can interact with it normally). Note that the extra step of
selecting the "Show Applet" button is needed - otherwise the
setTimeRange function is not found. This is a bug in the Applet - see
<http://bugs.sun.com/bugdatabase/view_bug.do?bug_id=6356869>. The
alternative is to put an alert() right before the call to setTimeRange.
Really. We have tried many work-arounds for this, but none allow for the
background load + no "Show Applet" button.

  - See <https://applet-launcher.dev.java.net/> is requests to server
    for copyright notice may be avoided using
        <param name="codebase_lookup" value="false">

The applet does not work in FF 3.07 on WinXP with JRE 1.6.0\_07,
possibly due to this problem:
<http://forums.java.net/jive/thread.jspa?threadID=39432>. Works on IE7
and Safari ... A hint: Safari gives

```
liveconnect: JavaScript: default security policy=
```
while FF says

`liveconnect:&nbsp;JavaScript:&nbsp;default&nbsp;security&nbsp;policy=`&lt;http://timeseries.org&gt;

Bottom of this thread suggests reverse DNS lookup is needed:
<http://forums.java.net/jive/thread.jspa?messageID=277896>
<http://seclists.org/fulldisclosure/2007/Jul/0159.html>

Java console on Mac: <http://ruk.ca/article/3001>

TODO: Try running applet from aurora.gmu.edu (which appears in the
reverse lookup for 129.174.113.163 or explicitly use ip address instead
of timeseries.org.

See also:
<http://crossbrowsertesting.blogspot.com/2008/03/possible-fix-for-intermittent-java.html>

It appears that we must wait until the applet internally has tried to
connect to the server before making a call to the applet with Javascript
that requires a request to the server.

<http://forums.sun.com/thread.jspa?threadID=5230759&start=0&tstart=0>

[Java Deployment tips](:Image:TS-1319.pdf.md "wikilink")

  - Inserting applet in DOM in background: <http://kaioa.com/node/21>

