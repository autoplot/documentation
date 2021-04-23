# org.autoplot.html.AsciiTableStreamerGeneric class for converting a table of ASCII strings to QDataSet stream.
 This supports streaming sources by reporting QDataSet records as they arrive.
AsciiTableStreamer( )


***
<a name="addRecord"></a>
# addRecord
addRecord( java.util.List values ) &rarr; void



### Parameters:
values - a java.util.List

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=addRecord&unscoped_q=addRecord">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="hasHeader"></a>
# hasHeader
hasHeader(  ) &rarr; boolean

return true if the header has been set.

### Returns:
true if the header has been set.

<a href="https://github.com/autoplot/dev/search?q=hasHeader&unscoped_q=hasHeader">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="hasNext"></a>
# hasNext
hasNext(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=hasNext&unscoped_q=hasNext">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="next"></a>
# next
next(  ) &rarr; QDataSet



### Returns:
org.das2.qds.QDataSet


<a href="https://github.com/autoplot/dev/search?q=next&unscoped_q=next">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="remove"></a>
# remove
remove(  ) &rarr; void



### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=remove&unscoped_q=remove">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setHasNext"></a>
# setHasNext
setHasNext( boolean t ) &rarr; void

indicate that no more records will be added.  This can only be set to 
 false.

### Parameters:
t - this must be set to false.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setHasNext&unscoped_q=setHasNext">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

