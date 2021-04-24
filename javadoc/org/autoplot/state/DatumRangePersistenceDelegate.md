# org.autoplot.state.DatumRangePersistenceDelegate



# DatumRangePersistenceDelegate( )


***
<a name="newDatumRange"></a>
# newDatumRange
newDatumRange( double min, double max, String units ) &rarr; DatumRange



### Parameters:
min - a double
<br>max - a double
<br>units - a String

### Returns:
org.das2.datum.DatumRange


<a href="https://github.com/autoplot/dev/search?q=newDatumRange&unscoped_q=newDatumRange">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="newTimeRange"></a>
# newTimeRange
newTimeRange( String stimeRange ) &rarr; DatumRange

create a time DatumRange from the string.  Since persistent file may be
 hacked by humans, check for parse exceptions.

### Parameters:
stimeRange - a String

### Returns:
a DatumRange


<a href="https://github.com/autoplot/dev/search?q=newTimeRange&unscoped_q=newTimeRange">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="writeObject"></a>
# writeObject
writeObject( Object oldInstance, java.beans.Encoder out ) &rarr; void



### Parameters:
oldInstance - an Object
<br>out - an Encoder

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=writeObject&unscoped_q=writeObject">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

