# org.autoplot.server.RequestListener
RequestListener( )


***
<a name="PROP_READDATA"></a>
# PROP_READDATA



***
<a name="PROP_SOCKET"></a>
# PROP_SOCKET



***
<a name="PROP_PORT"></a>
# PROP_PORT



***
<a name="PROP_DATA"></a>
# PROP_DATA



***
<a name="PROP_LISTENING"></a>
# PROP_LISTENING



***
<a name="PROP_REQUESTCOUNT"></a>
# PROP_REQUESTCOUNT



***
<a name="addPropertyChangeListener"></a>
# addPropertyChangeListener
addPropertyChangeListener( java.beans.PropertyChangeListener listener ) &rarr; void

Add PropertyChangeListener.

### Parameters:
listener - a PropertyChangeListener

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=addPropertyChangeListener&unscoped_q=addPropertyChangeListener">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

addPropertyChangeListener( String propertyName, java.beans.PropertyChangeListener listener ) &rarr; void<br>
***
<a name="getData"></a>
# getData
getData(  ) &rarr; String

Get the value of data

### Returns:
the value of data

<a href="https://github.com/autoplot/dev/search?q=getData&unscoped_q=getData">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getOutputStream"></a>
# getOutputStream
getOutputStream(  ) &rarr; OutputStream



### Returns:
java.io.OutputStream


<a href="https://github.com/autoplot/dev/search?q=getOutputStream&unscoped_q=getOutputStream">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getPort"></a>
# getPort
getPort(  ) &rarr; int

return the port being used.  Note if the port was zero, this
 will be assigned the port that was used.

### Returns:
the port being used.

<a href="https://github.com/autoplot/dev/search?q=getPort&unscoped_q=getPort">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getRequestCount"></a>
# getRequestCount
getRequestCount(  ) &rarr; int



### Returns:
int


<a href="https://github.com/autoplot/dev/search?q=getRequestCount&unscoped_q=getRequestCount">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getSocket"></a>
# getSocket
getSocket(  ) &rarr; Socket



### Returns:
java.net.Socket


<a href="https://github.com/autoplot/dev/search?q=getSocket&unscoped_q=getSocket">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isListening"></a>
# isListening
isListening(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isListening&unscoped_q=isListening">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isReadData"></a>
# isReadData
isReadData(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isReadData&unscoped_q=isReadData">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="removePropertyChangeListener"></a>
# removePropertyChangeListener
removePropertyChangeListener( java.beans.PropertyChangeListener listener ) &rarr; void

Remove PropertyChangeListener.

### Parameters:
listener - a PropertyChangeListener

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=removePropertyChangeListener&unscoped_q=removePropertyChangeListener">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

removePropertyChangeListener( String propertyName, java.beans.PropertyChangeListener listener ) &rarr; void<br>
***
<a name="setData"></a>
# setData
setData( String newdata ) &rarr; void

Set the value of data

### Parameters:
newdata - new value of data

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setData&unscoped_q=setData">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setListening"></a>
# setListening
setListening( boolean newlistening ) &rarr; void



### Parameters:
newlistening - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setListening&unscoped_q=setListening">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setPort"></a>
# setPort
setPort( int newport ) &rarr; void

this may be zero to request that a port be chosen, or non-zero
 for the port number.

### Parameters:
newport - an int

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setPort&unscoped_q=setPort">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setReadData"></a>
# setReadData
setReadData( boolean newreadData ) &rarr; void



### Parameters:
newreadData - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setReadData&unscoped_q=setReadData">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setRequestCount"></a>
# setRequestCount
setRequestCount( int newrequestCount ) &rarr; void



### Parameters:
newrequestCount - an int

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setRequestCount&unscoped_q=setRequestCount">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setSocket"></a>
# setSocket
setSocket( java.net.Socket newsocket ) &rarr; void



### Parameters:
newsocket - a Socket

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setSocket&unscoped_q=setSocket">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="startListening"></a>
# startListening
startListening(  ) &rarr; void



### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=startListening&unscoped_q=startListening">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="stopListening"></a>
# stopListening
stopListening(  ) &rarr; void



### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=stopListening&unscoped_q=stopListening">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

