# org.autoplot.imagedatasource.ImageDataSourceFormat

Format data to RGB images, or ARGB images.
 Formatter presumes data is:<ul>
 <li>(m,n,4) for ARGB 
 <li>(3,m,n) RGB. (this should not be used)
 <li>(m,n,3) RGB.
 </ul>
 When data is (m,n,4) then ds[:,:,0] should be the alpha channel,
 [:,:,1] should be the red channel, and so on.

# ImageDataSourceFormat( )


***
<a name="canFormat"></a>
# canFormat
canFormat( QDataSet ds ) &rarr; boolean



### Parameters:
ds - a QDataSet

### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=canFormat&unscoped_q=canFormat">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="formatData"></a>
# formatData
formatData( String uri, QDataSet data, ProgressMonitor mon ) &rarr; void



### Parameters:
uri - a String
<br>data - a QDataSet
<br>mon - a ProgressMonitor

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=formatData&unscoped_q=formatData">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="fromHSVtoRGB"></a>
# fromHSVtoRGB
fromHSVtoRGB( QDataSet hsv ) &rarr; QDataSet

convert HSV QDataSet to RGB.  The input should be a rank 3 dataset
 with rows for the first index, columns for the second index, and 
 3 indeces for the last index:<ul>
 <li>H, the hue, should vary from 0 to 360.
 <li>S, the Saturation, should vary from 0 to 100.
 <li>V, the Value, should vary from 0 to 100.
 </ul>

### Parameters:
hsv - rank 3, [rows;columns;h,s,v] dataset.

### Returns:
rank 3, [rows;columns;r,g,b] dataset.
### See Also:
<a href='https://git.uiowa.edu/jbf/autoplot/-/blob/master/doc/java/awt/Color.md#HSBtoRGB'>java.awt.Color#HSBtoRGB(float, float, float)</a> where this code was found and converted to QDataSet.<br>
<a href='#fromRGBtoHSV'>fromRGBtoHSV(QDataSet)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=fromHSVtoRGB&unscoped_q=fromHSVtoRGB">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="fromRGBtoHSV"></a>
# fromRGBtoHSV
fromRGBtoHSV( QDataSet rgb ) &rarr; QDataSet

Converts the components of a color, as specified by the default RGB
 model, to an equivalent set of values for hue, saturation, and
 brightness that are the three components of the HSB model.
 NOTE these values will be a bit different than those returned by 
 ImageDataSource's hue, saturation, and value channels, because of slightly
 different mappings.

### Parameters:
rgb - a QDataSet

### Returns:
hsv array [h,w,3]
### See Also:
<a href='https://git.uiowa.edu/jbf/autoplot/-/blob/master/doc/java/awt/Color.md#RGBtoHSB'>java.awt.Color#RGBtoHSB(int, int, int, float[])</a> <br>
<a href='#fromHSVtoRGB'>fromHSVtoRGB(QDataSet)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=fromRGBtoHSV&unscoped_q=fromRGBtoHSV">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDescription"></a>
# getDescription
getDescription(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getDescription&unscoped_q=getDescription">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

