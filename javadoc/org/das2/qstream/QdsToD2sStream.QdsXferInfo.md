# org.das2.qstream.QdsToD2sStream.QdsXferInfo

Determine and hold the information needed to transfer values out of a
 given QDataSet into a byte buffer.  The byte order is always native 
 endian

***
<a name="name"></a>
# name
name(  ) &rarr; String

Get a size independent type name

### Returns:
the type with any size information stripped off

<a href="https://github.com/autoplot/dev/search?q=name&unscoped_q=name">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="size"></a>
# size
size(  ) &rarr; int



### Returns:
the size in bytes of each output value

<a href="https://github.com/autoplot/dev/search?q=size&unscoped_q=size">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="xSliceBytes"></a>
# xSliceBytes
xSliceBytes( int i ) &rarr; int

Get the number of bytes needed to hold an x-slice of a single

### Parameters:
i - an int

### Returns:
an int


<a href="https://github.com/autoplot/dev/search?q=xSliceBytes&unscoped_q=xSliceBytes">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="xSliceItems"></a>
# xSliceItems
xSliceItems( int i ) &rarr; int

Get the number items in a single X-axis slice of this dataset the
 X-axis is synonymous with the QDataSet 0th axis for now.

### Parameters:
i - - The X point at which to get the items

### Returns:
an int


<a href="https://github.com/autoplot/dev/search?q=xSliceItems&unscoped_q=xSliceItems">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

