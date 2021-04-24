# org.das2.graph.DasRow

DasRow object represents the vertical position on the canvas.

# DasRow( org.das2.graph.DasCanvas parent, double top, double bottom )
create a DasRow with the normal position and no offsets.

# DasRow( org.das2.graph.DasCanvas canvas, org.das2.graph.DasRow parent, double nMin, double nMax, double emMin, double emMax, int ptMin, int ptMax )
create a DasRow

***
<a name="NULL"></a>
# NULL

placeholder for unassigned value.

***
<a name="bottom"></a>
# bottom
bottom(  ) &rarr; int

return the device location of the bottom (non-inclusive) of the row.

### Returns:
the device location of the bottom (non-inclusive) of the row.

<a href="https://github.com/autoplot/dev/search?q=bottom&unscoped_q=bottom">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="create"></a>
# create
create( org.das2.graph.DasCanvas canvas, org.das2.graph.DasRow parent, String minStr, String maxStr ) &rarr; DasRow

makes a new DasRow by parsing a string like "100%-5em+3pt" to get the offsets.
 The three qualifiers are "%", "em", and "pt", but "px" is allowed as well 
 as surely people will use that by mistake.  If an offset or the normal position
 is not specified, then 0 is used.

### Parameters:
canvas - the canvas for the layout, ignored when a parent DasRow is used.
<br>parent - if non-null, this DasRow is specified with respect to parent.
<br>minStr - a string like "0%+5em"
<br>maxStr - a string like "100%-7em"

### Returns:
a new DasRow.

<a href="https://github.com/autoplot/dev/search?q=create&unscoped_q=create">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

create( org.das2.graph.DasCanvas parent ) &rarr; DasRow<br>
create( org.das2.graph.DasCanvas parent, int iplot, int nplot ) &rarr; DasRow<br>
***
<a name="createAttachedRow"></a>
# createAttachedRow
createAttachedRow( double ptop, double pbottom ) &rarr; DasRow

create a row that is positioned relative to this row.

### Parameters:
ptop - the normal position
<br>pbottom - the normal position

### Returns:
the new row.

<a href="https://github.com/autoplot/dev/search?q=createAttachedRow&unscoped_q=createAttachedRow">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="createSubRow"></a>
# <del>createSubRow</del>
Deprecated: This created a row that was not attached to anything, so
 it was simply a convenience method that didn't save much effort.
***
<a name="getHeight"></a>
# getHeight
getHeight(  ) &rarr; int

return the height in points (pixels) of the row.

### Returns:
the height in points (pixels) of the row.

<a href="https://github.com/autoplot/dev/search?q=getHeight&unscoped_q=getHeight">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="top"></a>
# top
top(  ) &rarr; int

return the device location of the top of the row.

### Returns:
the device location of the top of the row.

<a href="https://github.com/autoplot/dev/search?q=top&unscoped_q=top">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

