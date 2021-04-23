# org.das2.event.DataPointSelectionEventThis is the general-purpose "a data point was selected" event.  Note that
 auxiliary data is supported, such as a keystroke that triggered the event.
 
 The X and Y Datums may be null, so that code may be reused.
DataPointSelectionEvent( Object source, Datum x, Datum y, java.util.Map planes )
Creates a new instance of DataPointSelectionEvent

DataPointSelectionEvent( Object source, Datum x, Datum y )


***
<a name="birthMilli"></a>
# birthMilli



***
<a name="getDataSet"></a>
# getDataSet
getDataSet(  ) &rarr; QDataSet

return the context dataset, from which the selection is made.

### Returns:
a QDataSet


<a href="https://github.com/autoplot/dev/search?q=getDataSet&unscoped_q=getDataSet">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getPlane"></a>
# getPlane
getPlane( String plane ) &rarr; Object



### Parameters:
plane - a String

### Returns:
java.lang.Object


<a href="https://github.com/autoplot/dev/search?q=getPlane&unscoped_q=getPlane">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getPlaneIds"></a>
# getPlaneIds
getPlaneIds(  ) &rarr; String



### Returns:
java.lang.String[]


<a href="https://github.com/autoplot/dev/search?q=getPlaneIds&unscoped_q=getPlaneIds">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getX"></a>
# getX
getX(  ) &rarr; Datum



### Returns:
org.das2.datum.Datum


<a href="https://github.com/autoplot/dev/search?q=getX&unscoped_q=getX">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getY"></a>
# getY
getY(  ) &rarr; Datum



### Returns:
org.das2.datum.Datum


<a href="https://github.com/autoplot/dev/search?q=getY&unscoped_q=getY">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="set"></a>
# set
set( Datum x, Datum y ) &rarr; void



### Parameters:
x - a Datum
<br>y - a Datum

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=set&unscoped_q=set">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setDataSet"></a>
# setDataSet
setDataSet( QDataSet ds ) &rarr; void



### Parameters:
ds - a QDataSet

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setDataSet&unscoped_q=setDataSet">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="toString"></a>
# toString
toString(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=toString&unscoped_q=toString">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

