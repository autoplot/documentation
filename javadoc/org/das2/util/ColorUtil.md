# org.das2.util.ColorUtil

single place to contain Color-Name mapping.  These include
 an old set of 10 or so color names, plus the 130 or so web color
 names like "SaddleBrown" and "DarkOrchid".

# ColorUtil( )


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
 <li>"#00000000" (transparent)
 <li>"0x00ffffff" (transparent)
 <li>"#ffeedd"
 <li>"LightPink" (X11 color names)
 </ul>
 This also allows a color name to follow the RGB like so:<ul>
 <li>"0xFFFF00 (Purple)"
 </ul>
 to improve legibility of .vap files.  
 <a href="https://wikipedia.org/wiki/X11_color_names#Color_name_chart">X11 color names</a>
 can be found at wikipedia.

### Parameters:
s - the string representation

### Returns:
the color
### See Also:
<a href='https://en.wikipedia.org/wiki/X11_color_names'>https://en.wikipedia.org/wiki/X11_color_names</a> <br>
<a href='http://cng.seas.rochester.edu/CNG/docs/x11color.html'>http://cng.seas.rochester.edu/CNG/docs/x11color.html</a> <br>

<a href="https://github.com/autoplot/dev/search?q=decodeColor&unscoped_q=decodeColor">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="encodeColor"></a>
# encodeColor
encodeColor( java.awt.Color color ) &rarr; String

return either a named color or 
 #00aaff for opaque colors and #80aaff00 for transparent colors.

### Parameters:
color - a Color

### Returns:
named color or hex string like "#FF0000" for Red.

<a href="https://github.com/autoplot/dev/search?q=encodeColor&unscoped_q=encodeColor">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getNamedColors"></a>
# getNamedColors
getNamedColors(  ) &rarr; Map

return a map of the named colors.

### Returns:
a map of the named colors.

<a href="https://github.com/autoplot/dev/search?q=getNamedColors&unscoped_q=getNamedColors">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getRicePaperColor"></a>
# getRicePaperColor
getRicePaperColor(  ) &rarr; Color

return standard color for slightly masking background.

### Returns:
a java.awt.Color


<a href="https://github.com/autoplot/dev/search?q=getRicePaperColor&unscoped_q=getRicePaperColor">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

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
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

