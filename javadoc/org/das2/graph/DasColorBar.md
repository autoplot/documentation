# org.das2.graph.DasColorBar

Axis that converts to RGB color instead of horizontal or vertical
 position.

# DasColorBar( Datum min, Datum max, boolean log )
Create an color bar object, relating data and color.

# DasColorBar( Datum min, Datum max, int orientation, boolean log )
Create an color bar object, relating data and color.

***
<a name="PROPERTY_TYPE"></a>
# PROPERTY_TYPE

handle for the property "type".

***
<a name="PROPERTY_FILL_COLOR"></a>
# PROPERTY_FILL_COLOR

handle for the property fillColor.

***
<a name="PROP_SHOWCOLORBAR"></a>
# PROP_SHOWCOLORBAR



***
<a name="getActiveRegion"></a>
# getActiveRegion
getActiveRegion(  ) &rarr; Shape



### Returns:
java.awt.Shape


<a href="https://github.com/autoplot/dev/search?q=getActiveRegion&unscoped_q=getActiveRegion">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getColorBarColumn"></a>
# getColorBarColumn
getColorBarColumn( org.das2.graph.DasColumn column ) &rarr; DasColumn

return a column suitable for the colorbar, based on the spectrogram
 column.

### Parameters:
column - the column for the spectrogram described.

### Returns:
the new column.

<a href="https://github.com/autoplot/dev/search?q=getColorBarColumn&unscoped_q=getColorBarColumn">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getFillColor"></a>
# getFillColor
getFillColor(  ) &rarr; Color

get the color used to indicate fill, often gray or a transparent 
 white.  Note all instances use the same fillColor.

### Returns:
the fill color.

<a href="https://github.com/autoplot/dev/search?q=getFillColor&unscoped_q=getFillColor">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getFillColorIndex"></a>
# getFillColorIndex
getFillColorIndex(  ) &rarr; int

return the index of the fill color in the indexed color model.

### Returns:
the index of the fill color

<a href="https://github.com/autoplot/dev/search?q=getFillColorIndex&unscoped_q=getFillColorIndex">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getIndexColorModel"></a>
# getIndexColorModel
getIndexColorModel(  ) &rarr; IndexColorModel

return the color model so that indexed color model can be used.

### Returns:
the color model

<a href="https://github.com/autoplot/dev/search?q=getIndexColorModel&unscoped_q=getIndexColorModel">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getType"></a>
# getType
getType(  ) &rarr; Type

return the type of colorbar (e.g. DasColorBar.Type.GRAYSCALE or DasColorBar.Type.APL_RAINBOW_BLACK0)

### Returns:
the type of colorbar

<a href="https://github.com/autoplot/dev/search?q=getType&unscoped_q=getType">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="indexColorTransform"></a>
# indexColorTransform
indexColorTransform( double data, Units units ) &rarr; int

convert the double to an indexed color.

### Parameters:
data - a data value
<br>units - the units of the given data value.

### Returns:
the index into the color table.
### See Also:
<a href='#getIndexColorModel'>getIndexColorModel()</a> <br>

<a href="https://github.com/autoplot/dev/search?q=indexColorTransform&unscoped_q=indexColorTransform">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isShowColorBar"></a>
# isShowColorBar
isShowColorBar(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isShowColorBar&unscoped_q=isShowColorBar">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="rgbTransform"></a>
# rgbTransform
rgbTransform( double data, Units units ) &rarr; int

convert the double to an RGB color.

### Parameters:
data - a data value
<br>units - the units of the given data value.

### Returns:
the combined RGB components
### See Also:
<a href='Color.md#Color'>Color#Color(int)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=rgbTransform&unscoped_q=rgbTransform">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setFillColor"></a>
# setFillColor
setFillColor( java.awt.Color fillColor ) &rarr; void

set the color used to indicate fill, often gray or a transparent 
 white.  Note all instances use the same fillColor.

### Parameters:
fillColor - the new fill color.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setFillColor&unscoped_q=setFillColor">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setShowColorBar"></a>
# setShowColorBar
setShowColorBar( boolean showColorBar ) &rarr; void

when set to false, this is basically an ordinary axis.  Autoplot uses
 this to support StackedHistogram mode.

### Parameters:
showColorBar - true if the colorbar should be drawn.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setShowColorBar&unscoped_q=setShowColorBar">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setType"></a>
# setType
setType( org.das2.graph.DasColorBar.Type type ) &rarr; void

set the type of colorbar

### Parameters:
type - type of colorbar (e.g. DasColorBar.Type.GRAYSCALE or DasColorBar.Type.APL_RAINBOW_BLACK0)

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setType&unscoped_q=setType">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

