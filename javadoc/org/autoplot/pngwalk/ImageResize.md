# org.autoplot.pngwalk.ImageResize

first from http://today.java.net/pub/a/today/2007/04/03/perils-of-image-getscaledinstance.html
 resize taken from http://www.componenthouse.com/article-20

# ImageResize( )


***
<a name="logger"></a>
# logger



***
<a name="getScaledInstance"></a>
# getScaledInstance
getScaledInstance( java.awt.image.BufferedImage img, int thumbSize ) &rarr; BufferedImage

convenient typical use.

### Parameters:
img - image to resize.
<br>thumbSize - corner-to-corner size, preserving aspect ratio.

### Returns:
buffered image that is thumbSize across.

<a href="https://github.com/autoplot/dev/search?q=getScaledInstance&unscoped_q=getScaledInstance">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

getScaledInstance( java.awt.image.BufferedImage img, int targetWidth, int targetHeight, Object hint, boolean higherQuality ) &rarr; BufferedImage<br>
