# org.autoplot.layout.LayoutUtilutility methods for adjusting canvas layout.
LayoutUtil( )


***
<a name="autolayout"></a>
# autolayout
autolayout( org.das2.graph.DasCanvas canvas, org.das2.graph.DasRow marginRow, org.das2.graph.DasColumn marginColumn ) &rarr; void

resets the layout on the canvas so that labels are not clipped (somewhat).
 Child row and columns are inspected as well, and it's assumed that adjusting
 this row and column (Autoplot's margin row and column), that everyone will be correctly adjusted.
 
 We calculate bounds on each component dependent on the row and column, then
 the region outside the canvas determines how much the row and column should
 be brought in.

### Parameters:
canvas - a DasCanvas
<br>marginRow - a DasRow
<br>marginColumn - a DasColumn

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=autolayout&unscoped_q=autolayout">[search for examples]</a>

***
<a name="getChildBounds"></a>
# getChildBounds
getChildBounds( org.das2.graph.DasColumn col ) &rarr; Rectangle

look for attached columns, get the bounds of all attachments.  For 
 example, this includes the bounds of a colorbar attached to the plot.

### Parameters:
col - a DasColumn

### Returns:
the bounds of all children, or null.

<a href="https://github.com/autoplot/dev/search?q=getChildBounds&unscoped_q=getChildBounds">[search for examples]</a>

getChildBounds( org.das2.graph.DasRow row ) &rarr; Rectangle<br>
***
<a name="getChildColumns"></a>
# getChildColumns
getChildColumns( org.das2.graph.DasDevicePosition col ) &rarr; List

Return a list of DasColumns where the parent is the given column.

### Parameters:
col - the column

### Returns:
list of columns.

<a href="https://github.com/autoplot/dev/search?q=getChildColumns&unscoped_q=getChildColumns">[search for examples]</a>

***
<a name="normalizeRows"></a>
# normalizeRows
normalizeRows( org.autoplot.dom.Canvas canvas ) &rarr; void

preserve pixel locations of the rows, with corrections to the marginRow.

### Parameters:
canvas - a Canvas

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=normalizeRows&unscoped_q=normalizeRows">[search for examples]</a>

normalizeRows( double em, org.das2.graph.DasRow marginRow, java.util.List rows ) &rarr; void<br>
