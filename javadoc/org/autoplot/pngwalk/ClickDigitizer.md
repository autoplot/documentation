# org.autoplot.pngwalk.ClickDigitizer

Quick-n-dirty class for picking off points from images.  The ClickDigitizer knows how to 
 grab JSON metadata from the image (http://autoplot.org/richPng) and invTransform the pixel
 location to a dataset.

# ClickDigitizer( org.autoplot.pngwalk.PngWalkView view )


***
<a name="dataToPixelTransform"></a>
# dataToPixelTransform
dataToPixelTransform( int iplot, QDataSet p ) &rarr; int

return the pixel coordinates for a given data coordinates.

### Parameters:
iplot - the plot number
<br>p - bundle of x and y data coordinates.

### Returns:
int[2] for the x and y pixel coordinates (0,0 is upper left).

<a href="https://github.com/autoplot/dev/search?q=dataToPixelTransform&unscoped_q=dataToPixelTransform">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="pixelToDataTransform"></a>
# pixelToDataTransform
pixelToDataTransform( int x, int y ) &rarr; QDataSet

return the coordinates for the click in data coordinates if the JSON
 Rich PNG metadata is available, or just the pixel coordinates if it
 is not, with the property "PlotNumber" indicating which plot number
 in the JSON is used.  The property "PlotNumber" 
 will be an integer equal -1 if the rich png metadata is not found,
 or zero or positive int for valid clicks.  If the x and y are not within
 a plot, then -1 is returned for the plot number.

### Parameters:
x - the horizontal pixel coordinate
<br>y - the vertical pixel coordinate, with 0 at the top.

### Returns:
two-element bundle QDataSet with PlotNumber property.  -1 
   indicates no plot found at the location, and -99 means no rich png data.

<a href="https://github.com/autoplot/dev/search?q=pixelToDataTransform&unscoped_q=pixelToDataTransform">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

pixelToDataTransform( int iplot, int x, int y ) &rarr; QDataSet<br>
