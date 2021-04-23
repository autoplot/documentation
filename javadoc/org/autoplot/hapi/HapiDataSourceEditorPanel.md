# org.autoplot.hapi.HapiDataSourceEditorPanel

Swing editor for HAPI URIs

# HapiDataSourceEditorPanel( )
Creates new form HapiDataSourceEditorPanel

***
<a name="getDurationForHumans"></a>
# getDurationForHumans
getDurationForHumans( long milliseconds ) &rarr; String

return the duration in a easily-human-consumable form.

### Parameters:
milliseconds - the duration in milliseconds.

### Returns:
a duration like "2.6 hours"

<a href="https://github.com/autoplot/dev/search?q=getDurationForHumans&unscoped_q=getDurationForHumans">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getPanel"></a>
# getPanel
getPanel(  ) &rarr; JPanel



### Returns:
javax.swing.JPanel


<a href="https://github.com/autoplot/dev/search?q=getPanel&unscoped_q=getPanel">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getURI"></a>
# getURI
getURI(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getURI&unscoped_q=getURI">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="loadKnownServersImmediately"></a>
# loadKnownServersImmediately
loadKnownServersImmediately(  ) &rarr; void

load the known servers and set the GUI.  This should not be called from
 the event thread, and a runnable for the event thread will be submitted.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=loadKnownServersImmediately&unscoped_q=loadKnownServersImmediately">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="loadKnownServersSoon"></a>
# loadKnownServersSoon
loadKnownServersSoon(  ) &rarr; void

request that the known servers be displayed.  This will spawn an 
 asynchronous thread to get the server names, and then will load the GUI 
 on the event thread.  This can be called from the event thread.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=loadKnownServersSoon&unscoped_q=loadKnownServersSoon">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="main"></a>
# main
main( java.lang.String[] args ) &rarr; void



### Parameters:
args - a java.lang.String[]

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=main&unscoped_q=main">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="markProblems"></a>
# markProblems
markProblems( java.util.List problems ) &rarr; void



### Parameters:
problems - a java.util.List

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=markProblems&unscoped_q=markProblems">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="prepare"></a>
# prepare
prepare( String uri, java.awt.Window parent, ProgressMonitor mon ) &rarr; boolean



### Parameters:
uri - a String
<br>parent - a Window
<br>mon - a ProgressMonitor

### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=prepare&unscoped_q=prepare">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="reject"></a>
# reject
reject( String uri ) &rarr; boolean



### Parameters:
uri - a String

### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=reject&unscoped_q=reject">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setURI"></a>
# setURI
setURI( String uri ) &rarr; void



### Parameters:
uri - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setURI&unscoped_q=setURI">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

