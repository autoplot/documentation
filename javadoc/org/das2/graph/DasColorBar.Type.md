# org.das2.graph.DasColorBar.Typeenumeration of the types of colorbars.
Type( String desc, int[] colorTable )
create a new color table Type.

***
<a name="COLOR_WEDGE"></a>
# COLOR_WEDGE

Rainbow colorbar used by default.  TODO: this is a misnomer, where
 color_wedge was the type of object in das1, not the instance of the type,
 and this should be renamed to "rainbow"

***
<a name="APL_RAINBOW_BLACK0"></a>
# APL_RAINBOW_BLACK0

rainbow colorbar used at APL that has black at the bottom.

***
<a name="APL_RAINBOW_WHITE0"></a>
# APL_RAINBOW_WHITE0

rainbow colorbar used at APL that has white at the bottom.

***
<a name="GSFC_RP_SPECIAL"></a>
# GSFC_RP_SPECIAL

rainbow colorbar introduced for use at Goddard Space Flight Center.

***
<a name="MATLAB_JET"></a>
# MATLAB_JET

Mimic the default Matlab colorbar for comparison with Matlab-generated spectrograms.

***
<a name="MATLAB_JET_BLACK0"></a>
# MATLAB_JET_BLACK0

Mimic the default Matlab colorbar for comparison with Matlab-generated spectrograms, but with black for the bottom most color.

***
<a name="MATLAB_HSV"></a>
# MATLAB_HSV

Mimic the default Matlab colorbar HSV.

***
<a name="BLUE_TO_ORANGE"></a>
# BLUE_TO_ORANGE



***
<a name="GRAYSCALE"></a>
# GRAYSCALE

gray scale with white at the minimum (bottom) and black at the maximum.

***
<a name="INVERSE_GRAYSCALE"></a>
# INVERSE_GRAYSCALE

gray scale with black at the minimum (bottom) and white at the maximum.

***
<a name="WRAPPED_COLOR_WEDGE"></a>
# WRAPPED_COLOR_WEDGE

rainbow that wraps around so that the top and bottom are the same color,
 When used with care this is useful for spaces that wrap around (modulo),
 such as longitude.

***
<a name="BLUE_BLACK_RED_WEDGE"></a>
# BLUE_BLACK_RED_WEDGE

colorbar with black in the middle, blue at the minimum and red at the maximum
 for showing deviations from the center.

***
<a name="BLUE_WHITE_RED_WEDGE"></a>
# BLUE_WHITE_RED_WEDGE

colorbar with white in the middle, blue at the minimum and red at the maximum
 for showing deviations from the center.

***
<a name="BLACK_RED"></a>
# BLACK_RED

black to red, introduced to show the red component of RGB images

***
<a name="BLACK_GREEN"></a>
# BLACK_GREEN

black to green, introduced to show the green component of RGB images

***
<a name="BLACK_BLUE"></a>
# BLACK_BLUE

black to blue, introduced to show the blue component of RGB images

***
<a name="WHITE_BLUE_BLACK"></a>
# WHITE_BLUE_BLACK

white to blue to black

***
<a name="INVERSE_WHITE_BLUE_BLACK"></a>
# INVERSE_WHITE_BLUE_BLACK

black to blue to white

***
<a name="VIOLET_YELLOW"></a>
# VIOLET_YELLOW

Violet -Yellow

***
<a name="SCIPY_PLASMA"></a>
# SCIPY_PLASMA

SciPy Plasma

***
<a name="AJ4CO_RAINBOW"></a>
# AJ4CO_RAINBOW

AJ4CO_RAINBOW for Radio JOVE community

***
<a name="drawListIcon"></a>
# drawListIcon
drawListIcon( java.awt.Graphics2D g, int x, int y ) &rarr; void



### Parameters:
g - a Graphics2D
<br>x - an int
<br>y - an int

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=drawListIcon&unscoped_q=drawListIcon">[search for examples]</a>

***
<a name="getAllTypes"></a>
# getAllTypes
getAllTypes(  ) &rarr; List

return a list of all defined Types, in the order in which they were constructed.

### Returns:
list of Type objects.

<a href="https://github.com/autoplot/dev/search?q=getAllTypes&unscoped_q=getAllTypes">[search for examples]</a>

***
<a name="getColorCount"></a>
# getColorCount
getColorCount(  ) &rarr; int

Return the number of colors in the color bar.  Fill (gray) is an additional
 color, and it's understood that the colors indeces from 0 to getColorCount()-1 
 are the color wedge, and getColorCount() is the fill color.

### Returns:
the number of colors.

<a href="https://github.com/autoplot/dev/search?q=getColorCount&unscoped_q=getColorCount">[search for examples]</a>

***
<a name="getHorizontalScaledImage"></a>
# getHorizontalScaledImage
getHorizontalScaledImage( int width, int height ) &rarr; BufferedImage

return an image showing the colors from left to right.

### Parameters:
width - the width of the image
<br>height - the height of the image

### Returns:
the image

<a href="https://github.com/autoplot/dev/search?q=getHorizontalScaledImage&unscoped_q=getHorizontalScaledImage">[search for examples]</a>

***
<a name="getListIcon"></a>
# getListIcon
getListIcon(  ) &rarr; Icon



### Returns:
javax.swing.Icon


<a href="https://github.com/autoplot/dev/search?q=getListIcon&unscoped_q=getListIcon">[search for examples]</a>

***
<a name="getListLabel"></a>
# getListLabel
getListLabel(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getListLabel&unscoped_q=getListLabel">[search for examples]</a>

***
<a name="getRGB"></a>
# getRGB
getRGB( int index ) &rarr; int

return the RGB encoded color for the index.

### Parameters:
index - the index, from 0 to getColorCount().

### Returns:
the RGB color
### See Also:
<a href='Color.md#Color'>Color#Color(int)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=getRGB&unscoped_q=getRGB">[search for examples]</a>

***
<a name="getVerticalScaledImage"></a>
# getVerticalScaledImage
getVerticalScaledImage( int width, int height ) &rarr; BufferedImage

return an image showing the colors from bottom to top.

### Parameters:
width - the width of the image
<br>height - the height of the image

### Returns:
the image

<a href="https://github.com/autoplot/dev/search?q=getVerticalScaledImage&unscoped_q=getVerticalScaledImage">[search for examples]</a>

***
<a name="makeColorTable"></a>
# makeColorTable
makeColorTable( int[] index, int[] red, int[] green, int[] blue, int ncolor, int bottom, int top ) &rarr; int

returns a color table with interpolated colors for the wedge from 0 to ncolor-1, and at ncolor, the fill color.

### Parameters:
index - set of indeces that are control points for interpolation, including 0 and ncolor-1.
<br>red - the red value from 0 to 255 at each index
<br>green - the green value from 0 to 255 at each index
<br>blue - the blue value from 0 to 255 at each index
<br>ncolor - number of colors, typically COLORTABLE_SIZE=240.
<br>bottom - the bottom, typically 0.
<br>top - the top, typically COLORTABLE_SIZE=240.

### Returns:
an array of RGB colors.
### See Also:
<a href='Color.md#Color'>Color#Color(int)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=makeColorTable&unscoped_q=makeColorTable">[search for examples]</a>

***
<a name="maybeInitializeIcon"></a>
# maybeInitializeIcon
maybeInitializeIcon(  ) &rarr; void

initialize the icon representing this colorbar, if not done already.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=maybeInitializeIcon&unscoped_q=maybeInitializeIcon">[search for examples]</a>

***
<a name="parse"></a>
# parse
parse( String s ) &rarr; Type

from the string, identify the type.

### Parameters:
s - string like "apl_rainbow_black0"

### Returns:
type like Type.APL_RAINBOW_BLACK0.

<a href="https://github.com/autoplot/dev/search?q=parse&unscoped_q=parse">[search for examples]</a>

***
<a name="toString"></a>
# toString
toString(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=toString&unscoped_q=toString">[search for examples]</a>

