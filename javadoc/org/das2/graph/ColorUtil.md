# org.das2.graph.ColorUtilsingle place to contain Color-Name mapping.  See https://sourceforge.net/p/autoplot/feature-requests/263/
ColorUtil( )


***
<a name="decodeColor"></a>
# decodeColor
decodeColor( String s ) &rarr; Color

decode the color, throwing a RuntimeException when the color 
 is not parsable. Valid entries include:<ul>
 <li>"red" 
 <li>"RED" 
 <li>"0xFF0000" 
 <li>"0xff0000" 
 <li>"#ffeedd"
 </ul>
 This also allows a color name to follow the RGB like so:<ul>
 <li>"0xFFFF00 (Purple)"
 </ul>
 to improve legibility of .vap files.

### Parameters:
s - a String

### Returns:
a java.awt.Color


<a href="https://github.com/autoplot/dev/search?q=decodeColor&unscoped_q=decodeColor">[search for examples]</a>

***
<a name="encodeColor"></a>
# encodeColor
encodeColor( java.awt.Color color ) &rarr; String

return either a named color or 
 "#" + Integer.toHexString( color.getRGB() &amp; 0xFFFFFF)

### Parameters:
color - a Color

### Returns:
named color or hex string like "#FF0000" for Red.

<a href="https://github.com/autoplot/dev/search?q=encodeColor&unscoped_q=encodeColor">[search for examples]</a>

***
<a name="getNamedColors"></a>
# getNamedColors
getNamedColors(  ) &rarr; Map

return a map of the named colors.

### Returns:
a map of the named colors.

<a href="https://github.com/autoplot/dev/search?q=getNamedColors&unscoped_q=getNamedColors">[search for examples]</a>

***
<a name="getRicePaperColor"></a>
# getRicePaperColor
getRicePaperColor(  ) &rarr; Color

return standard color for slightly masking background.

### Returns:
a java.awt.Color


<a href="https://github.com/autoplot/dev/search?q=getRicePaperColor&unscoped_q=getRicePaperColor">[search for examples]</a>

***
<a name="nameForColor"></a>
# nameForColor
nameForColor( java.awt.Color color ) &rarr; String

return the preferred name for the color

### Parameters:
color - a Color

### Returns:
the preferred name (or #RGB) for the color

<a href="https://github.com/autoplot/dev/search?q=nameForColor&unscoped_q=nameForColor">[search for examples]</a>

