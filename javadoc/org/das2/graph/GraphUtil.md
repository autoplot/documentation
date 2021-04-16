# org.das2.graph.GraphUtilUtilities for drawing graphics and establishing standard behavior.
 This provides functions to get a 16x16 icon for a color, getting a Path
 from a series of data points, and a "visualize" method for simply looking at
 some data.
GraphUtil( )


***
<a name="CONNECT_MODE_HISTOGRAM"></a>
# CONNECT_MODE_HISTOGRAM

draw the lines in histogram mode, horizontal to the half-way point, then vertical, then horizontal the rest of the way.

***
<a name="CONNECT_MODE_SCATTER"></a>
# CONNECT_MODE_SCATTER

don't draw connecting lines.

***
<a name="CONNECT_MODE_SERIES"></a>
# CONNECT_MODE_SERIES

the normal connecting mode from point-to-point in a series.

***
<a name="blurImage"></a>
# blurImage
blurImage( java.awt.image.BufferedImage im, int size ) &rarr; BufferedImage

blur the image with a Guassian blur.

### Parameters:
im - a BufferedImage
<br>size - the size of the blur, roughly in pixels.

### Returns:
image

<a href="https://github.com/autoplot/dev/search?q=blurImage&unscoped_q=blurImage">[search for examples]</a>

***
<a name="calculateAT"></a>
# calculateAT
calculateAT( org.das2.graph.DasAxis xaxis0, org.das2.graph.DasAxis yaxis0, org.das2.graph.DasAxis xaxis1, org.das2.graph.DasAxis yaxis1 ) &rarr; AffineTransform

calculates the AffineTransform between two sets of x and y axes, if possible.

### Parameters:
xaxis0 - the original reference frame x axis
<br>yaxis0 - the original reference frame y axis
<br>xaxis1 - the new reference frame x axis
<br>yaxis1 - the new reference frame y axis

### Returns:
an AffineTransform that transforms data positioned with xaxis0 and yaxis0 on xaxis1 and yaxis1, or null if no such transform exists.

<a href="https://github.com/autoplot/dev/search?q=calculateAT&unscoped_q=calculateAT">[search for examples]</a>

calculateAT( DatumRange xaxis0, DatumRange yaxis0, org.das2.graph.DasAxis xaxis1, org.das2.graph.DasAxis yaxis1 ) &rarr; AffineTransform<br>
***
<a name="calculateManualTicks"></a>
# calculateManualTicks
calculateManualTicks( String lticks, DatumRange dr, boolean log ) &rarr; TickVDescriptor

calculate a TickVDescriptor for the ticks.  
 Example specifications:<ul>
 <li>+20 every 20 units, whatever the data units are.
 <li>+20s  every 20 seconds
 <li>0,20,40,60,100  explicit locations.
 <li>+20s/4 every 20 seconds, with four minor divisions.
 </ul>

### Parameters:
lticks - the specification
<br>dr - the range to cover
<br>log - a boolean

### Returns:
null if the string can't be parsed, or the TickVDescriptor

<a href="https://github.com/autoplot/dev/search?q=calculateManualTicks&unscoped_q=calculateManualTicks">[search for examples]</a>

***
<a name="clipPath"></a>
# clipPath
clipPath( java.awt.geom.PathIterator it, java.awt.geom.GeneralPath result, java.awt.Rectangle clip ) &rarr; int

clip the path to within the clip rectangle.  Note this may introduce 
 breaks where the path was continuous before.  Note this does not work
 with quadTo etc.  This was motivated by an old version of Adobe Illustrator
 which didn't respect the clip set in the PDF, and with the journal 
 Nature, which apparently uses an old version of Illustrator.

### Parameters:
it - a PathIterator
<br>result - a GeneralPath
<br>clip - a Rectangle

### Returns:
an int


<a href="https://github.com/autoplot/dev/search?q=clipPath&unscoped_q=clipPath">[search for examples]</a>

***
<a name="colorIcon"></a>
# colorIcon
colorIcon( java.awt.Color iconColor, int w, int h ) &rarr; Icon

return an icon block with the color and size.

### Parameters:
iconColor - the color
<br>w - the width in pixels
<br>h - the height in pixels

### Returns:
an icon.

<a href="https://github.com/autoplot/dev/search?q=colorIcon&unscoped_q=colorIcon">[search for examples]</a>

***
<a name="copyAxis"></a>
# copyAxis
copyAxis( org.das2.graph.DasAxis a ) &rarr; DasAxis

return a copy of the plot.  It does not have the
 row and column set to its own row and column.

### Parameters:
a - a DasAxis

### Returns:
an org.das2.graph.DasAxis


<a href="https://github.com/autoplot/dev/search?q=copyAxis&unscoped_q=copyAxis">[search for examples]</a>

***
<a name="copyColorBar"></a>
# copyColorBar
copyColorBar( org.das2.graph.DasColorBar a ) &rarr; DasColorBar

return a copy of the plot.  It does not have the
 row and column set to its own row and column.

### Parameters:
a - a DasColorBar

### Returns:
an org.das2.graph.DasColorBar


<a href="https://github.com/autoplot/dev/search?q=copyColorBar&unscoped_q=copyColorBar">[search for examples]</a>

***
<a name="copyPlot"></a>
# copyPlot
copyPlot( org.das2.graph.DasPlot p ) &rarr; DasPlot

return a copy of the plot.  This will include the Renderers and the 
 data they contain.  The plot is not attached to a canvas or row 
 and column.
 <pre>
 
   cnvsNew= new DasCanvas(500,500);
   row= new DasRow(cnvsNew,0.2,0.8);
   column= new DasColumn(cnvsNew,0.2,0.8);
   p= GraphUtil.copyPlot(dp); 
   cnvsNew.add(p,row,column); 
 
 </pre>

### Parameters:
p - a DasPlot

### Returns:
an org.das2.graph.DasPlot


<a href="https://github.com/autoplot/dev/search?q=copyPlot&unscoped_q=copyPlot">[search for examples]</a>

***
<a name="describe"></a>
# describe
describe( java.awt.geom.GeneralPath path, boolean enumeratePoints ) &rarr; String

describe the path for debugging.

### Parameters:
path - the Path to describe
<br>enumeratePoints - if true, print all the points as well.

### Returns:
String description.

<a href="https://github.com/autoplot/dev/search?q=describe&unscoped_q=describe">[search for examples]</a>

***
<a name="getATScaleTranslateString"></a>
# getATScaleTranslateString
getATScaleTranslateString( java.awt.geom.AffineTransform at ) &rarr; String

return a string representation of the affine transforms used in DasPlot for
 debugging.

### Parameters:
at - the affine transform

### Returns:
a string representation of the affine transforms used in DasPlot for
 debugging.

<a href="https://github.com/autoplot/dev/search?q=getATScaleTranslateString&unscoped_q=getATScaleTranslateString">[search for examples]</a>

***
<a name="getFontConverter"></a>
# getFontConverter
getFontConverter( org.das2.graph.DasCanvasComponent dcc, String fallbackFont ) &rarr; Converter

converts forward from relative font spec to point size, used by
 the annotation and axis nodes.

### Parameters:
dcc - the canvas component.
<br>fallbackFont - the font to use when a font is not available, like "sans-8"

### Returns:
the converter that converts between strings like "1em" and the font.

<a href="https://github.com/autoplot/dev/search?q=getFontConverter&unscoped_q=getFontConverter">[search for examples]</a>

***
<a name="getGaussianBlurFilter"></a>
# getGaussianBlurFilter
getGaussianBlurFilter( int radius, boolean horizontal ) &rarr; ConvolveOp

return a Gaussian filter for blurring images.

### Parameters:
radius - the radius filter in pixels.
<br>horizontal - true if horizontal blur.

### Returns:
the ConvolveOp

<a href="https://github.com/autoplot/dev/search?q=getGaussianBlurFilter&unscoped_q=getGaussianBlurFilter">[search for examples]</a>

***
<a name="getPath"></a>
# getPath
getPath( org.das2.graph.DasAxis xAxis, org.das2.graph.DasAxis yAxis, QDataSet ds, boolean histogram, boolean clip ) &rarr; GeneralPath

get the path for the points, checking for breaks in the data from fill values.

### Parameters:
xAxis - the x axis.
<br>yAxis - the y axis.
<br>ds - the y values.  SemanticOps.xtagsDataSet is used to extract the x values.
<br>histogram - if true, use histogram (stair-step) mode
<br>clip - limit path to what's visible for each axis.

### Returns:
the GeneralPath.

<a href="https://github.com/autoplot/dev/search?q=getPath&unscoped_q=getPath">[search for examples]</a>

getPath( org.das2.graph.DasAxis xAxis, org.das2.graph.DasAxis yAxis, QDataSet xds, QDataSet yds, boolean histogram, boolean clip ) &rarr; GeneralPath<br>
getPath( org.das2.graph.DasAxis xAxis, org.das2.graph.DasAxis yAxis, QDataSet xds, QDataSet yds, String mode, boolean clip ) &rarr; GeneralPath<br>
***
<a name="getRicePaperColor"></a>
# getRicePaperColor
getRicePaperColor(  ) &rarr; Color

return translucent white color for indicating the application is busy.

### Returns:
translucent white color

<a href="https://github.com/autoplot/dev/search?q=getRicePaperColor&unscoped_q=getRicePaperColor">[search for examples]</a>

***
<a name="getSlopeIntercept"></a>
# getSlopeIntercept
getSlopeIntercept( double x0, double y0, double x1, double y1 ) &rarr; double

calculates the slope and intercept of a line going through two points.

### Parameters:
x0 - the first point x
<br>y0 - the first point y
<br>x1 - the second point x
<br>y1 - the second point y

### Returns:
a double array with two elements [ slope, intercept ].

<a href="https://github.com/autoplot/dev/search?q=getSlopeIntercept&unscoped_q=getSlopeIntercept">[search for examples]</a>

***
<a name="guessPlot"></a>
# guessPlot
guessPlot( QDataSet ds ) &rarr; DasPlot

get a plot and renderer for the dataset.

### Parameters:
ds - the dataset

### Returns:
a plot with a renderer for the dataset.

<a href="https://github.com/autoplot/dev/search?q=guessPlot&unscoped_q=guessPlot">[search for examples]</a>

***
<a name="guessRenderer"></a>
# guessRenderer
guessRenderer( QDataSet ds ) &rarr; Renderer

legacy guess that is used who-knows-where.  Autoplot has much better code
 for guessing, refer to it.

### Parameters:
ds - a QDataSet

### Returns:
an org.das2.graph.Renderer


<a href="https://github.com/autoplot/dev/search?q=guessRenderer&unscoped_q=guessRenderer">[search for examples]</a>

***
<a name="guessXAxis"></a>
# guessXAxis
guessXAxis( QDataSet ds ) &rarr; DasAxis



### Parameters:
ds - a QDataSet

### Returns:
org.das2.graph.DasAxis


<a href="https://github.com/autoplot/dev/search?q=guessXAxis&unscoped_q=guessXAxis">[search for examples]</a>

***
<a name="guessYAxis"></a>
# guessYAxis
guessYAxis( QDataSet dsz ) &rarr; DasAxis



### Parameters:
dsz - a QDataSet

### Returns:
org.das2.graph.DasAxis


<a href="https://github.com/autoplot/dev/search?q=guessYAxis&unscoped_q=guessYAxis">[search for examples]</a>

***
<a name="guessZAxis"></a>
# guessZAxis
guessZAxis( QDataSet dsz ) &rarr; DasAxis



### Parameters:
dsz - a QDataSet

### Returns:
org.das2.graph.DasAxis


<a href="https://github.com/autoplot/dev/search?q=guessZAxis&unscoped_q=guessZAxis">[search for examples]</a>

***
<a name="invTransformRange"></a>
# invTransformRange
invTransformRange( org.das2.graph.DasAxis axis, double x1, double x2 ) &rarr; DatumRange



### Parameters:
axis - a DasAxis
<br>x1 - a double
<br>x2 - a double

### Returns:
org.das2.datum.DatumRange


<a href="https://github.com/autoplot/dev/search?q=invTransformRange&unscoped_q=invTransformRange">[search for examples]</a>

***
<a name="lineIntersection"></a>
# lineIntersection
lineIntersection( java.awt.geom.Line2D line1, java.awt.geom.Line2D line2, boolean noBoundsCheck ) &rarr; Point2D

returns the point where the two line segments intersect, or null.

### Parameters:
line1 - a Line2D
<br>line2 - a Line2D
<br>noBoundsCheck - if true, then do not check the segment bounds.

### Returns:
a java.awt.geom.Point2D


<a href="https://github.com/autoplot/dev/search?q=lineIntersection&unscoped_q=lineIntersection">[search for examples]</a>

***
<a name="lineRectangleIntersection"></a>
# lineRectangleIntersection
lineRectangleIntersection( java.awt.geom.Point2D p0, java.awt.geom.Point2D p1, java.awt.geom.Rectangle2D r0 ) &rarr; Point2D

return the intersection of a line segment and the edge of a rectangle, 
 where one point is outside of the rectangle and one is inside.

### Parameters:
p0 - a Point2D
<br>p1 - a Point2D
<br>r0 - a Rectangle2D

### Returns:
null or the point along the rectangle

<a href="https://github.com/autoplot/dev/search?q=lineRectangleIntersection&unscoped_q=lineRectangleIntersection">[search for examples]</a>

***
<a name="lineRectangleMask"></a>
# lineRectangleMask
lineRectangleMask( java.awt.geom.Point2D p0, java.awt.geom.Point2D p1, java.awt.geom.Rectangle2D r ) &rarr; Line2D

return the line segment which is within the rectangle mask.

### Parameters:
p0 - the first point
<br>p1 - the second point
<br>r - the rectangle

### Returns:
null when they do not intersect, or the segment

<a href="https://github.com/autoplot/dev/search?q=lineRectangleMask&unscoped_q=lineRectangleMask">[search for examples]</a>

***
<a name="newDasPlot"></a>
# newDasPlot
newDasPlot( org.das2.graph.DasCanvas canvas, DatumRange x, DatumRange y ) &rarr; DasPlot

create a plot for the canvas, along with the row and column for layout.

### Parameters:
canvas - the canvas parent for the plot.
<br>x - the x range
<br>y - the y range

### Returns:
the plot.

<a href="https://github.com/autoplot/dev/search?q=newDasPlot&unscoped_q=newDasPlot">[search for examples]</a>

***
<a name="parseLayoutLength"></a>
# parseLayoutLength
parseLayoutLength( String s, double totalWidth, double em ) &rarr; double

parse strings like "14em+2pt" into a length in pixels.
 <ul>
 <li>"1em",0,8 -> 8
 <li>"50%",240,0 -> 120
 <li>"4pt",240,8 -> 4
 <li>"4px",240,8 -> 4
 <li>"1em+4pt",240,8 -> 12
 </ul>

### Parameters:
s - the string specifying ems and pxs
<br>totalWidth - the total with for the normalized length.
<br>em - the size of an em in pixels.

### Returns:
the length in pixels
### See Also:
<a href='DasDevicePosition.md#parseLayoutStr'>DasDevicePosition#parseLayoutStr(java.lang.String)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=parseLayoutLength&unscoped_q=parseLayoutLength">[search for examples]</a>

***
<a name="perpendicularLine"></a>
# perpendicularLine
perpendicularLine( java.awt.geom.Line2D line, java.awt.Point p, double len ) &rarr; Line2D

create a line perpendicular to the line segment <code>line</code>, which
 would go through <code>p</code>, and have length <code>abs(len)</code>.
 If len is negative, then line.p1,line.p2,p is counter-clockwise.
 This is left unimplemented as it's a nice student project.

### Parameters:
line - a line segment.
<br>p - a point, whose projection is necessarily within the line segment.
<br>len - the length of the resulting line, or

### Returns:
line colinear with p and having length abs(len).

<a href="https://github.com/autoplot/dev/search?q=perpendicularLine&unscoped_q=perpendicularLine">[search for examples]</a>

***
<a name="pointsAlongCurve"></a>
# pointsAlongCurve
pointsAlongCurve( java.awt.geom.PathIterator it, double[] pathlen, java.awt.geom.Point2D.Double[] result, double[] orientation, boolean stopAtMoveTo ) &rarr; double

return the points along a curve.  Used by ContourRenderer.  The returned
 result is the remaining path length.  Elements of pathlen that are beyond
 the total path length are not computed, and the result points will be null.

### Parameters:
it - PathIterator first point is used to start the length.
<br>pathlen - monotonically increasing path lengths at which the position is to be located.  May be null if only the total path length is desired.
<br>result - the resultant points will be put into this array.  This array should have the same number of elements as pathlen
<br>orientation - the local orientation, in radians, of the point at will be put into this array.  This array should have the same number of elements as pathlen
<br>stopAtMoveTo - treat SEG_MOVETO as the end of the path.  The pathIterator will be left at this point.

### Returns:
the remaining length.  Note null may be used for pathlen, result, and orientation and this will simply return the total path length.

<a href="https://github.com/autoplot/dev/search?q=pointsAlongCurve&unscoped_q=pointsAlongCurve">[search for examples]</a>

***
<a name="reducePath"></a>
# reducePath
reducePath( java.awt.geom.PathIterator it, java.awt.geom.GeneralPath result ) &rarr; int

Returns the input GeneralPath filled with new points which will be rendered identically to the input path,
 but contains a minimal number of points.  We bin average the points within a cell, because discretization
 would mess up the label orientation in contour plotting.

 a new GeneralPath which will be rendered identically to the input path,
 but contains a minimal number of points.

### Parameters:
it - A path iterator with minute details that will be lost when rendering.
<br>result - A GeneralPath to put the result into.

### Returns:
the number of "points" (LINE_TOs) in the result.

<a href="https://github.com/autoplot/dev/search?q=reducePath&unscoped_q=reducePath">[search for examples]</a>

reducePath( java.awt.geom.PathIterator it, java.awt.geom.GeneralPath result, int res ) &rarr; int<br>
***
<a name="reducePath20140622"></a>
# reducePath20140622
reducePath20140622( java.awt.geom.PathIterator it, java.awt.geom.GeneralPath result, int resn, int resd ) &rarr; int

New ReducePath reduces a path by keeping track of vertically collinear points, and reducing them to an entry
 point, an exit point, min and max.  This can be all four in one point.  We also limit the resolution and 
 combine points that are basically the same value, using resn and resd (numerator and denominator).  For 
 example (1/5) would mean that points within x of 1/5 of one another are considered vertically collinear.

### Parameters:
it - input path.
<br>result - output path.
<br>resn - the resolution numerator (e.g. 1)
<br>resd - the resolution denominator (e.g. 5)

### Returns:
the number of points.

<a href="https://github.com/autoplot/dev/search?q=reducePath20140622&unscoped_q=reducePath20140622">[search for examples]</a>

***
<a name="shortenLine"></a>
# shortenLine
shortenLine( java.awt.geom.Line2D line, double l1, double l2 ) &rarr; Line2D

return line shorted by so many pixels at each end.

### Parameters:
line - the line
<br>l1 - number of units to adjust the first point, towards the center
<br>l2 - number of units to adjust the second point, towards the center

### Returns:
the new line

<a href="https://github.com/autoplot/dev/search?q=shortenLine&unscoped_q=shortenLine">[search for examples]</a>

***
<a name="shrinkRectangle"></a>
# shrinkRectangle
shrinkRectangle( java.awt.Rectangle bounds, int percent ) &rarr; Rectangle

return rectangle with same center that is percent/100 of the
 original width and height.

### Parameters:
bounds - the original rectangle.
<br>percent - the percent to increase (110% is 10% bigger)

### Returns:
a rectangle with same center that is percent/100. of the
 original width and height.

<a href="https://github.com/autoplot/dev/search?q=shrinkRectangle&unscoped_q=shrinkRectangle">[search for examples]</a>

***
<a name="transformRange"></a>
# transformRange
transformRange( org.das2.graph.DasAxis axis, DatumRange range ) &rarr; double

returns pixel range of the datum range, guarenteeing that the first 
 element will be less than or equal to the second.

### Parameters:
axis - a DasAxis
<br>range - a DatumRange

### Returns:
a double[]


<a href="https://github.com/autoplot/dev/search?q=transformRange&unscoped_q=transformRange">[search for examples]</a>

***
<a name="visualize"></a>
# visualize
visualize( QDataSet ds ) &rarr; DasPlot

get a plot and add it to a JFrame.

### Parameters:
ds - a QDataSet

### Returns:
an org.das2.graph.DasPlot


<a href="https://github.com/autoplot/dev/search?q=visualize&unscoped_q=visualize">[search for examples]</a>

