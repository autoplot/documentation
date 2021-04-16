# org.das2.graph.PsymType-safe enumeration class for the psym property of
 a <code>DasSymbolPlot</code>, with values for none, dots, circles, etc.
***
<a name="NONE"></a>
# NONE



***
<a name="DOTS"></a>
# DOTS



***
<a name="CIRCLES"></a>
# CIRCLES



***
<a name="TRIANGLES"></a>
# TRIANGLES



***
<a name="CROSS"></a>
# CROSS



***
<a name="draw"></a>
# draw
draw( java.awt.Graphics g, double x, double y, float size ) &rarr; void

Draw the psym at the given coordinates.
 if <code>drawsLines()</code> returns false, then the
 ix and iy parameters are ignored.

### Parameters:
g - the graphics context.
<br>x - the x position of the middle of the symbol
<br>y - the y position of the middle of the symbol
<br>size - size of the symbol

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=draw&unscoped_q=draw">[search for examples]</a>

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
<a name="drawTriangle"></a>
# drawTriangle
drawTriangle( java.awt.Graphics g, double x, double y, float size ) &rarr; void



### Parameters:
g - a Graphics
<br>x - a double
<br>y - a double
<br>size - a float

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=drawTriangle&unscoped_q=drawTriangle">[search for examples]</a>

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
<a name="parsePsym"></a>
# parsePsym
parsePsym( String str ) &rarr; Psym

return a Psym for the name, like none, dots, circles, etc.

### Parameters:
str - the name, e.g. none, dots, etc.

### Returns:
Psym.NONE, Psym.DOTS, etc.

<a href="https://github.com/autoplot/dev/search?q=parsePsym&unscoped_q=parsePsym">[search for examples]</a>

***
<a name="toString"></a>
# toString
toString(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=toString&unscoped_q=toString">[search for examples]</a>

