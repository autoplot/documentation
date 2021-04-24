# org.autoplot.idlsupport.APDataSet

Extension to QDataSetBridge, which supports reading in data from Autoplot URIs.

# APDataSet( )
1.4.1 clean up Das2Server source so that monitor is only called once.

***
<a name="loadDataSet"></a>
# loadDataSet
loadDataSet( String uri ) &rarr; int

get the dataset in one load.

### Parameters:
uri - the URI to load.

### Returns:
0 if everything went okay, non-zero if there was an error
### See Also:
<a href='QDataSetBridge.md#getException'>QDataSetBridge#getException()</a> <br>

<a href="https://github.com/autoplot/dev/search?q=loadDataSet&unscoped_q=loadDataSet">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

loadDataSet( String uri, ProgressMonitor mon ) &rarr; int<br>
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
<a name="setDataSetURI"></a>
# setDataSetURI
setDataSetURI( String suri ) &rarr; void

set the data source URI.

### Parameters:
suri - the dataset URI, such as vap+dat:http://autoplot.org/data/autoplot.dat

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setDataSetURI&unscoped_q=setDataSetURI">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setDataSetURL"></a>
# <del>setDataSetURL</del>
Deprecated: use setDataSetURI, which takes the same argument.
***
<a name="toString"></a>
# toString
toString(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=toString&unscoped_q=toString">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

