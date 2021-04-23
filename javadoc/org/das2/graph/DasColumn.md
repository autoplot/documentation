# org.das2.graph.DasColumn

DasColumn object represents the horizontal position on the canvas.

# DasColumn( org.das2.graph.DasCanvas parent, double nMin, double nMax )
create a DasColumn with the normal position and no offsets.

# DasColumn( org.das2.graph.DasCanvas canvas, org.das2.graph.DasColumn parent, double nMin, double nMax, double emMin, double emMax, int ptMin, int ptMax )
create a DasColumn

***
<a name="NULL"></a>
# NULL

placeholder for unassigned value.

***
<a name="create"></a>
# create
create( org.das2.graph.DasCanvas canvas, org.das2.graph.DasColumn parent, String minStr, String maxStr ) &rarr; DasColumn

makes a new DasColumn by parsing a string like "100%-5em+3pt" to get the offsets.
 The three qualifiers are "%", "em", and "pt", but "px" is allowed as well 
 as surely people will use that by mistake.  If an offset or the normal position
 is not specified, then 0 is used.

### Parameters:
canvas - the canvas for the layout, ignored when a parent DasColumn is used.
<br>parent - if non-null, this DasColumn is specified with respect to parent.
<br>minStr - a string like "0%+5em"
<br>maxStr - a string like "100%-7em"

### Returns:
a new DasColumn

<a href="https://github.com/autoplot/dev/search?q=create&unscoped_q=create">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

create( org.das2.graph.DasCanvas parent ) &rarr; DasColumn<br>
***
<a name="createAttachedColumn"></a>
# createAttachedColumn
createAttachedColumn( double pleft, double pright ) &rarr; DasColumn

create a column that is positioned relative to this column.

### Parameters:
pleft - the normal position
<br>pright - the normal position

### Returns:
the new row.

<a href="https://github.com/autoplot/dev/search?q=createAttachedColumn&unscoped_q=createAttachedColumn">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getWidth"></a>
# getWidth
getWidth(  ) &rarr; int

return the width in points (pixels) of the column.

### Returns:
the width in points (pixels) of the column.

<a href="https://github.com/autoplot/dev/search?q=getWidth&unscoped_q=getWidth">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="left"></a>
# left
left(  ) &rarr; int

return pixel location of the left of the column.

### Returns:
pixel location of the left of the column.

<a href="https://github.com/autoplot/dev/search?q=left&unscoped_q=left">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="right"></a>
# right
right(  ) &rarr; int

return pixel location the right (non-inclusive) of the column.

### Returns:
pixel location the right (non-inclusive) of the column.

<a href="https://github.com/autoplot/dev/search?q=right&unscoped_q=right">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

