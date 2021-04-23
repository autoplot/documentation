# org.autoplot.dom.CanvasControllerController for canvases.
CanvasController( org.autoplot.dom.Application dom, org.autoplot.dom.Canvas canvas )


***
<a name="addColumn"></a>
# addColumn
addColumn(  ) &rarr; Column

add a column to the application to the right of the other columns.

### Returns:
the column

<a href="https://github.com/autoplot/dev/search?q=addColumn&unscoped_q=addColumn">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="addColumns"></a>
# addColumns
addColumns( int count ) &rarr; List

add columns to the current plot.

### Parameters:
count - number of columns to add

### Returns:
a list of the new Columns.

<a href="https://github.com/autoplot/dev/search?q=addColumns&unscoped_q=addColumns">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="addRow"></a>
# addRow
addRow(  ) &rarr; Row

add a row to the application, below.

### Returns:
the row

<a href="https://github.com/autoplot/dev/search?q=addRow&unscoped_q=addRow">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="addRows"></a>
# addRows
addRows( int count ) &rarr; List

add rows below the current plot.

### Parameters:
count - an int

### Returns:
a java.util.List


<a href="https://github.com/autoplot/dev/search?q=addRows&unscoped_q=addRows">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

addRows( int count, Object dir ) &rarr; List<br>
***
<a name="getDasCanvas"></a>
# getDasCanvas
getDasCanvas(  ) &rarr; DasCanvas



### Returns:
org.das2.graph.DasCanvas


<a href="https://github.com/autoplot/dev/search?q=getDasCanvas&unscoped_q=getDasCanvas">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDropTargetListener"></a>
# getDropTargetListener
getDropTargetListener(  ) &rarr; DropTargetListener



### Returns:
java.awt.dnd.DropTargetListener


<a href="https://github.com/autoplot/dev/search?q=getDropTargetListener&unscoped_q=getDropTargetListener">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getRowFor"></a>
# getRowFor
getRowFor( org.autoplot.dom.Plot domPlot ) &rarr; Row



### Parameters:
domPlot - a Plot

### Returns:
org.autoplot.dom.Row


<a href="https://github.com/autoplot/dev/search?q=getRowFor&unscoped_q=getRowFor">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="indicateSelection"></a>
# indicateSelection
indicateSelection( java.util.List selectedItems ) &rarr; void

flash the selected plots and plotElements, by temporarily 
 adding a painter to the canvas.

### Parameters:
selectedItems - the items to flash.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=indicateSelection&unscoped_q=indicateSelection">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="maybeAddColumn"></a>
# maybeAddColumn
maybeAddColumn( String spec ) &rarr; Column

add a column with the spec (e.g. "30%+1em,60%-4em").  If another column with 
 the same spec is found, then just return that column.

### Parameters:
spec - spec like "30%+1em,60%-4em"

### Returns:
a column that implements.

<a href="https://github.com/autoplot/dev/search?q=maybeAddColumn&unscoped_q=maybeAddColumn">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="maybeAddRow"></a>
# maybeAddRow
maybeAddRow( String spec ) &rarr; Row

add a row with the spec (e.g. "30%+1em,60%-4em").  If another row with 
 the same spec is found, then just return that row.

### Parameters:
spec - spec like "30%+1em,60%-4em"

### Returns:
a row that implements.

<a href="https://github.com/autoplot/dev/search?q=maybeAddRow&unscoped_q=maybeAddRow">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setColumn"></a>
# setColumn
setColumn( String column ) &rarr; void

support legacy column property of canvas

### Parameters:
column - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setColumn&unscoped_q=setColumn">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setDimensions"></a>
# setDimensions
setDimensions( int width, int height ) &rarr; void

set the height and width in one atomic operation.

### Parameters:
width - an int
<br>height - an int

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setDimensions&unscoped_q=setDimensions">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setDropTargetListener"></a>
# setDropTargetListener
setDropTargetListener( java.awt.dnd.DropTargetListener list ) &rarr; void



### Parameters:
list - a DropTargetListener

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setDropTargetListener&unscoped_q=setDropTargetListener">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setRow"></a>
# setRow
setRow( String row ) &rarr; void

support legacy row property of canvas

### Parameters:
row - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setRow&unscoped_q=setRow">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="toString"></a>
# toString
toString(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=toString&unscoped_q=toString">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

