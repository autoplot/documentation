# org.das2.util.awt.PdfGraphicsOutputsupport writing to PDF.
PdfGraphicsOutput( )
Creates a new instance of PDFGraphicsOutput

***
<a name="READING_FONTS"></a>
# READING_FONTS



***
<a name="STATE_IDLE"></a>
# STATE_IDLE



***
<a name="STATE_READING"></a>
# STATE_READING



***
<a name="STATE_READY"></a>
# STATE_READY



***
<a name="dumpMapToFile"></a>
# dumpMapToFile
dumpMapToFile( java.io.File f ) &rarr; void

dump the keys out to a file.

### Parameters:
f - a file target.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=dumpMapToFile&unscoped_q=dumpMapToFile">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="finish"></a>
# finish
finish(  ) &rarr; void



### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=finish&unscoped_q=finish">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getGraphics"></a>
# getGraphics
getGraphics(  ) &rarr; Graphics



### Returns:
java.awt.Graphics


<a href="https://github.com/autoplot/dev/search?q=getGraphics&unscoped_q=getGraphics">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getGraphics2D"></a>
# getGraphics2D
getGraphics2D(  ) &rarr; Graphics2D



### Returns:
java.awt.Graphics2D


<a href="https://github.com/autoplot/dev/search?q=getGraphics2D&unscoped_q=getGraphics2D">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="main"></a>
# main
main( java.lang.String[] args ) &rarr; void



### Parameters:
args - a java.lang.String[]

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=main&unscoped_q=main">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="resetFontToTtfMap"></a>
# resetFontToTtfMap
resetFontToTtfMap(  ) &rarr; Map



### Returns:
java.util.Map


<a href="https://github.com/autoplot/dev/search?q=resetFontToTtfMap&unscoped_q=resetFontToTtfMap">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setGraphicsShapes"></a>
# setGraphicsShapes
setGraphicsShapes( boolean graphicsShapes ) &rarr; void

If true, then fonts are written out as lines and will match the screen.
 If false, then labels are editable.

### Parameters:
graphicsShapes - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setGraphicsShapes&unscoped_q=setGraphicsShapes">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setOutputStream"></a>
# setOutputStream
setOutputStream( java.io.OutputStream out ) &rarr; void



### Parameters:
out - an OutputStream

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setOutputStream&unscoped_q=setOutputStream">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setPixelsPerInch"></a>
# setPixelsPerInch
setPixelsPerInch( int ppi ) &rarr; void

set the scaling from graphics pixels to physical paper coordinates,
 where 72dpi is the default.

### Parameters:
ppi - an int

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setPixelsPerInch&unscoped_q=setPixelsPerInch">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setSize"></a>
# setSize
setSize( int width, int height ) &rarr; void

set the size in points.

### Parameters:
width - an int
<br>height - an int

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setSize&unscoped_q=setSize">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="start"></a>
# start
start(  ) &rarr; void



### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=start&unscoped_q=start">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="ttfFromName"></a>
# ttfFromName
ttfFromName( java.awt.Font font ) &rarr; String

return the name of the .ttf file for the platform, or null.

### Parameters:
font - a Font

### Returns:
the name of the .ttf file, or null.

<a href="https://github.com/autoplot/dev/search?q=ttfFromName&unscoped_q=ttfFromName">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="ttfFromNameInteractive"></a>
# ttfFromNameInteractive
ttfFromNameInteractive( java.awt.Font font ) &rarr; String

kludge to support call from AWT.  If the font map is not yet
 loaded, return READING_FONTS and start the lookup on a new thread.

### Parameters:
font - a Font

### Returns:
READING_FONTS or the name (or null).

<a href="https://github.com/autoplot/dev/search?q=ttfFromNameInteractive&unscoped_q=ttfFromNameInteractive">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

