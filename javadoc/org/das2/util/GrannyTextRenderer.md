# org.das2.util.GrannyTextRendererUtility class for rendering "Granny" strings, which use the codes
 identified by Grandle and Nystrom in their 1980 paper to provide 
 rich formatting such as new lines and superscripts.
 These are strings like "E=mc!e2" where the !e indicates the pen should be 
 moved to the exponent position before drawing.  This supports sequences
 including:<pre>
 !A  shift up one half line
 !B  shift down one half line  (e.g.  !A3!n-!B4!n is 3/4).
 !C  newline 
 !D  subscript 0.62 of old font size.
 !U  superscript of 0.62 of old font size.
 !E  superscript 0.44 of old font size.
 !I  subscript 0.44 of old font size.
 !N  return to the original font size.
 !R  restore position to last saved position
 !S  save the current position.
 !K  reduce the font size. (Not in IDL's set.)
 !!  the exclamation point (!)
 !(ext;args) where ext can be:
   !(color;saddleBrown)
   !(painter;codeId;codeArg1)
   </pre>
 For Greek and math symbols, Unicode characters should be
 used like so: &amp;#9742; (&#9742 phone symbol), or symbols like <tt>&amp;Omega;</tt> and <tt>&amp;omega;</tt>
GrannyTextRenderer( )


***
<a name="LEFT_ALIGNMENT"></a>
# LEFT_ALIGNMENT



***
<a name="CENTER_ALIGNMENT"></a>
# CENTER_ALIGNMENT



***
<a name="RIGHT_ALIGNMENT"></a>
# RIGHT_ALIGNMENT



***
<a name="addPainter"></a>
# addPainter
addPainter( String id, org.das2.util.GrannyTextRenderer.Painter p ) &rarr; void

add a painter for the grannyTextRenderer.  This is done by associating
 a Painter code with an id, and the id is used within the annotation string.

### Parameters:
id - id for the painter, where the id is found in the granny text string
<br>p - the painter code which draws on a graphics context.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=addPainter&unscoped_q=addPainter">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="clearPainters"></a>
# clearPainters
clearPainters(  ) &rarr; void

remove all the painters

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=clearPainters&unscoped_q=clearPainters">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="draw"></a>
# draw
draw( java.awt.Graphics ig, float ix, float iy ) &rarr; void

draw the current string.  Note the first line will be above iy, and following lines will
 be below iy.  This is to be consistent with Graphics2D.drawString.

### Parameters:
ig - Graphic object to use to render the text.
<br>ix - The x position of the first character of text.
<br>iy - The y position of the baseline of the first line of text.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=draw&unscoped_q=draw">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getAlignment"></a>
# getAlignment
getAlignment(  ) &rarr; float

returns the current alignment, by default LEFT_ALIGNMENT.

### Returns:
the current alignment.

<a href="https://github.com/autoplot/dev/search?q=getAlignment&unscoped_q=getAlignment">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getAscent"></a>
# getAscent
getAscent(  ) &rarr; double

return the amount that the bounding box will go above the baseline.
 This is also the height of the first line.

### Returns:
the amount that the bounding box will go above the baseline.

<a href="https://github.com/autoplot/dev/search?q=getAscent&unscoped_q=getAscent">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getBounds"></a>
# getBounds
getBounds(  ) &rarr; Rectangle

returns the bounds of the current string.  The lower-left corner of
 the first character will be roughly (0,0), to be compatible with
 FontMetrics.getStringBounds().

### Returns:
a Rectangle indicating the text boundaries.

<a href="https://github.com/autoplot/dev/search?q=getBounds&unscoped_q=getBounds">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getBounds2D"></a>
# getBounds2D
getBounds2D(  ) &rarr; Rectangle2D

return a rectangle backed by floating point numbers.

### Returns:
Rectangle2D.Double

<a href="https://github.com/autoplot/dev/search?q=getBounds2D&unscoped_q=getBounds2D">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDescent"></a>
# getDescent
getDescent(  ) &rarr; double

return the amount that the bounding box will go below the baseline.

### Returns:
the amount that the bounding box will go below the baseline.

<a href="https://github.com/autoplot/dev/search?q=getDescent&unscoped_q=getDescent">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getHeight"></a>
# getHeight
getHeight(  ) &rarr; double

returns the hieght of the calculated bounding box.

### Returns:
the height of the bounding box, in pixels.

<a href="https://github.com/autoplot/dev/search?q=getHeight&unscoped_q=getHeight">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getLineOneWidth"></a>
# getLineOneWidth
getLineOneWidth(  ) &rarr; double

returns the width in pixels of the first line.

### Returns:
the width in pixels of the first line.

<a href="https://github.com/autoplot/dev/search?q=getLineOneWidth&unscoped_q=getLineOneWidth">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getWidth"></a>
# getWidth
getWidth(  ) &rarr; double

returns the width of the bounding box, in pixels.

### Returns:
the width of the bounding box, in pixels.

<a href="https://github.com/autoplot/dev/search?q=getWidth&unscoped_q=getWidth">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="removePainter"></a>
# removePainter
removePainter( String id ) &rarr; void

remove the painter with the given id.

### Parameters:
id - id for the painter, where the id is found in the granny text string

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=removePainter&unscoped_q=removePainter">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setAlignment"></a>
# setAlignment
setAlignment( float a ) &rarr; void

set the alignment for rendering, one of LEFT_ALIGNMENT  CENTER_ALIGNMENT or RIGHT_ALIGNMENT.

### Parameters:
a - the alignment, one of LEFT_ALIGNMENT  CENTER_ALIGNMENT or RIGHT_ALIGNMENT.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setAlignment&unscoped_q=setAlignment">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setString"></a>
# <del>setString</del>
Deprecated: use setString( Graphics g, String str ) instead.
setString( java.awt.Graphics g, String str ) &rarr; void<br>
setString( java.awt.Font font, String label ) &rarr; void<br>
***
<a name="toString"></a>
# toString
toString(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=toString&unscoped_q=toString">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

