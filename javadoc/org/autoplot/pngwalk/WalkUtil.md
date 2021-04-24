# org.autoplot.pngwalk.WalkUtil



# WalkUtil( )


***
<a name="fileExists"></a>
# fileExists
fileExists( String surl ) &rarr; boolean



### Parameters:
surl - a String

### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=fileExists&unscoped_q=fileExists">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getFilesFor"></a>
# getFilesFor
getFilesFor( String surl, DatumRange timeRange, java.util.List timeRanges, boolean download, ProgressMonitor mon ) &rarr; List

return an array of URIs that match the spec for the timerange 
 (if provided), limiting the search to this range.

### Parameters:
surl - an Autoplot URI with an aggregation specifier.
<br>timeRange - a string that is parsed to a time range, such as 2001, or null.
<br>timeRanges - list which is populated
<br>download - (is not used)
<br>mon - progress monitor

### Returns:
a list of URIs without the aggregation specifier.

<a href="https://github.com/autoplot/dev/search?q=getFilesFor&unscoped_q=getFilesFor">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="resizeImage"></a>
# resizeImage
resizeImage( java.awt.image.BufferedImage originalImage, int width, int height ) &rarr; BufferedImage

fast resize based on Java2D.  This is lower quality than ScalePerspectiveImageOp, but much faster.

### Parameters:
originalImage - a BufferedImage
<br>width - an int
<br>height - an int

### Returns:
a java.awt.image.BufferedImage


<a href="https://github.com/autoplot/dev/search?q=resizeImage&unscoped_q=resizeImage">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

