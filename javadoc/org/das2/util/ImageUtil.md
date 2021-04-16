# org.das2.util.ImageUtilUtilities for image files and images.
ImageUtil( )


***
<a name="getJSONMetadata"></a>
# getJSONMetadata
getJSONMetadata( java.io.File file ) &rarr; String

return the node containing JSON metadata showing where the plots are in images
 produced by the Autoplot Das2 library.

### Parameters:
file - the png file.

### Returns:
null or the JSON describing the image.  See http://autoplot.org/developer.richPng

<a href="https://github.com/autoplot/dev/search?q=getJSONMetadata&unscoped_q=getJSONMetadata">[search for examples]</a>

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

getScaledInstance( java.awt.image.BufferedImage img, int width, int height, boolean pad ) &rarr; BufferedImage<br>
getScaledInstance( java.awt.image.BufferedImage img, int targetWidth, int targetHeight, Object hint, boolean higherQuality ) &rarr; BufferedImage<br>
