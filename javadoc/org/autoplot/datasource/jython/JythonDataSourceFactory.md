# org.autoplot.datasource.jython.JythonDataSourceFactory
JythonDataSourceFactory( )


***
<a name="addExeceptionListener"></a>
# addExeceptionListener
addExeceptionListener( java.beans.ExceptionListener listener ) &rarr; void

provide the script panel with a method for getting errors when they 
 occur, so it can mark where they have occurred.

### Parameters:
listener - an ExceptionListener

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=addExeceptionListener&unscoped_q=addExeceptionListener">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getCapability"></a>
# getCapability
getCapability( java.lang.Class clazz ) &rarr; Object



### Parameters:
clazz - a java.lang.Class

### Returns:
java.lang.Object


<a href="https://github.com/autoplot/dev/search?q=getCapability&unscoped_q=getCapability">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getCompletions"></a>
# getCompletions
getCompletions( org.autoplot.datasource.CompletionContext cc, ProgressMonitor mon ) &rarr; List



### Parameters:
cc - a CompletionContext
<br>mon - a ProgressMonitor

### Returns:
java.util.List


<a href="https://github.com/autoplot/dev/search?q=getCompletions&unscoped_q=getCompletions">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDataSource"></a>
# getDataSource
getDataSource( java.net.URI uri ) &rarr; DataSource



### Parameters:
uri - an URI

### Returns:
org.autoplot.datasource.DataSource


<a href="https://github.com/autoplot/dev/search?q=getDataSource&unscoped_q=getDataSource">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="jydsHasLocalReferences"></a>
# jydsHasLocalReferences
jydsHasLocalReferences( java.net.URI uri ) &rarr; boolean

this is a non-trivial problem, and for now we will
 assume any .jyds has local references and therefore cannot
 be run from a remote .vap file from the server.  Further, it's 
 probably better to look into creating a sandboxed thread on which 
 to run the script.

### Parameters:
uri - an URI

### Returns:
true if the jyds has local resource references

<a href="https://github.com/autoplot/dev/search?q=jydsHasLocalReferences&unscoped_q=jydsHasLocalReferences">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="reject"></a>
# reject
reject( String surl, java.util.List problems, ProgressMonitor mon ) &rarr; boolean

Reject when:
   - the URI doesn't contain a timerange but the data source has TimeSeriesBrowse

### Parameters:
surl - a String
<br>problems - a java.util.List
<br>mon - a ProgressMonitor

### Returns:
a boolean


<a href="https://github.com/autoplot/dev/search?q=reject&unscoped_q=reject">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

