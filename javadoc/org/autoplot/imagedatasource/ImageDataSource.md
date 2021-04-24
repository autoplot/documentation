# org.autoplot.imagedatasource.ImageDataSource



# ImageDataSource( java.net.URI uri )


***
<a name="CHANNEL_HUE"></a>
# CHANNEL_HUE



***
<a name="CHANNEL_SATURATION"></a>
# CHANNEL_SATURATION



***
<a name="CHANNEL_VALUE"></a>
# CHANNEL_VALUE



***
<a name="getDataSet"></a>
# getDataSet
getDataSet( ProgressMonitor mon ) &rarr; QDataSet



### Parameters:
mon - a ProgressMonitor

### Returns:
org.das2.qds.QDataSet


<a href="https://github.com/autoplot/dev/search?q=getDataSet&unscoped_q=getDataSet">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getJpegExifMetaData"></a>
# getJpegExifMetaData
getJpegExifMetaData( ProgressMonitor mon ) &rarr; Map

read useful JPG metadata, such as the Orientation.  This also looks to see if GPS
 metadata is available.

### Parameters:
mon - a ProgressMonitor

### Returns:
a java.util.Map


<a href="https://github.com/autoplot/dev/search?q=getJpegExifMetaData&unscoped_q=getJpegExifMetaData">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

getJpegExifMetaData( java.io.InputStream in ) &rarr; Map<br>
***
<a name="getMetadata"></a>
# getMetadata
getMetadata( ProgressMonitor mon ) &rarr; Map



### Parameters:
mon - a ProgressMonitor

### Returns:
java.util.Map


<a href="https://github.com/autoplot/dev/search?q=getMetadata&unscoped_q=getMetadata">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getRange"></a>
# getRange
getRange( JSONObject axis ) &rarr; QDataSet



### Parameters:
axis - a JSONObject

### Returns:
org.das2.qds.QDataSet


<a href="https://github.com/autoplot/dev/search?q=getRange&unscoped_q=getRange">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="rotateImage"></a>
# rotateImage
rotateImage( java.awt.image.BufferedImage image, double drot, java.awt.image.BufferedImage dest ) &rarr; BufferedImage

rotate the image.

### Parameters:
image - a BufferedImage
<br>drot - rotate this many degrees clockwise
<br>dest - the target BufferedImage or null if one should be created, the same size as the original, regardless of rotation.

### Returns:
the created bufferedImage

<a href="https://github.com/autoplot/dev/search?q=rotateImage&unscoped_q=rotateImage">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

