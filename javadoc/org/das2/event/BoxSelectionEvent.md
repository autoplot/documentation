# org.das2.event.BoxSelectionEventThis is the range analog to the DataPointSelectionEvent.  The 
 DataPointSelectionEvent is a point, and this is a box.

 Note that it's acceptable to have null xrange and yrange, so that the same
 code can support a variety of applications.  It's left to the programmer to
 see that these are used consistently.
BoxSelectionEvent( Object source, DatumRange xrange, DatumRange yrange )
create the BoxSelectionEvent with additional planes of data.

BoxSelectionEvent( Object source, DatumRange xrange, DatumRange yrange, java.util.HashMap planes )
create the BoxSelectionEvent with additional planes of data.

***
<a name="getDataSet"></a>
# getDataSet
getDataSet(  ) &rarr; QDataSet

get the dataset attached to this event.

### Returns:
the dataset attached to this event.

<a href="https://github.com/autoplot/dev/search?q=getDataSet&unscoped_q=getDataSet">[search for examples]</a>

***
<a name="getFinishX"></a>
# getFinishX
getFinishX(  ) &rarr; Datum

get the X coordinate of the mouse button release

### Returns:
the release coordinate X

<a href="https://github.com/autoplot/dev/search?q=getFinishX&unscoped_q=getFinishX">[search for examples]</a>

***
<a name="getFinishY"></a>
# getFinishY
getFinishY(  ) &rarr; Datum

get the Y coordinate of the mouse button release

### Returns:
the release coordinate Y

<a href="https://github.com/autoplot/dev/search?q=getFinishY&unscoped_q=getFinishY">[search for examples]</a>

***
<a name="getPlane"></a>
# getPlane
getPlane( String plane ) &rarr; Object

get the data attached to the plane name.  This allows applications
 to attach additional data to the event.  For example, the BoxSelectorMouseModule
 attaches the key pressed.

### Parameters:
plane - a String

### Returns:
the value associated with the plane, or null.

<a href="https://github.com/autoplot/dev/search?q=getPlane&unscoped_q=getPlane">[search for examples]</a>

***
<a name="getPlaneIds"></a>
# getPlaneIds
getPlaneIds(  ) &rarr; String

return the list of additional data planes attached to this event.

### Returns:
a java.lang.String[]


<a href="https://github.com/autoplot/dev/search?q=getPlaneIds&unscoped_q=getPlaneIds">[search for examples]</a>

***
<a name="getStartX"></a>
# getStartX
getStartX(  ) &rarr; Datum

get the X coordinate or the mouse button press

### Returns:
the X coordinate or the mouse button press

<a href="https://github.com/autoplot/dev/search?q=getStartX&unscoped_q=getStartX">[search for examples]</a>

***
<a name="getStartY"></a>
# getStartY
getStartY(  ) &rarr; Datum

get the Y coordinate or the mouse button press

### Returns:
the Y coordinate or the mouse button press

<a href="https://github.com/autoplot/dev/search?q=getStartY&unscoped_q=getStartY">[search for examples]</a>

***
<a name="getXRange"></a>
# getXRange
getXRange(  ) &rarr; DatumRange

get the X data range of the gesture

### Returns:
the X data range of the gesture

<a href="https://github.com/autoplot/dev/search?q=getXRange&unscoped_q=getXRange">[search for examples]</a>

***
<a name="getYRange"></a>
# getYRange
getYRange(  ) &rarr; DatumRange

get the Y data range of the gesture

### Returns:
the Y data range of the gesture

<a href="https://github.com/autoplot/dev/search?q=getYRange&unscoped_q=getYRange">[search for examples]</a>

***
<a name="setDataSet"></a>
# setDataSet
setDataSet( QDataSet ds ) &rarr; void

attach a dataset to this event.

### Parameters:
ds - a dataset for this event.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setDataSet&unscoped_q=setDataSet">[search for examples]</a>

***
<a name="setFinish"></a>
# setFinish
setFinish( Datum x, Datum y ) &rarr; void

set the end coordinates of the mouse release.

### Parameters:
x - the release coordinate X
<br>y - the release coordinate Y

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setFinish&unscoped_q=setFinish">[search for examples]</a>

***
<a name="setStart"></a>
# setStart
setStart( Datum x, Datum y ) &rarr; void

set the coordinates of the mouse button press

### Parameters:
x - the x coordinate
<br>y - the y coordinate

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setStart&unscoped_q=setStart">[search for examples]</a>

***
<a name="toString"></a>
# toString
toString(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=toString&unscoped_q=toString">[search for examples]</a>

