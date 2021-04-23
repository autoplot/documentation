# org.autoplot.imagedatasource.ImageDataSetAdapt a BufferedImage to a rank 2 or rank 3 QDataSet, using
 ColorOp to extract red, green, or blue channels.  When mask
 is null and op is null, then a rank 3 dataset [w,h,3] is returned, 
 a bundle of red, green, blue channels.
ImageDataSet( java.awt.image.BufferedImage image )
create a dataset from the image,
 returning a rank 3 dataset ds[w,h,3].

ImageDataSet( java.awt.image.BufferedImage image, java.awt.Color mask, org.autoplot.imagedatasource.ImageDataSet.ColorOp op )
create a dataset from the image.  When mask and op are null,
 then a rank 3 dataset ds[w,h,3] is returned.

***
<a name="length"></a>
# length
length(  ) &rarr; int



### Returns:
int


<a href="https://github.com/autoplot/dev/search?q=length&unscoped_q=length">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

length( int i ) &rarr; int<br>
length( int i, int j ) &rarr; int<br>
***
<a name="rank"></a>
# rank
rank(  ) &rarr; int



### Returns:
int


<a href="https://github.com/autoplot/dev/search?q=rank&unscoped_q=rank">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="value"></a>
# value
value( int i0, int i1 ) &rarr; double



### Parameters:
i0 - an int
<br>i1 - an int

### Returns:
double


<a href="https://github.com/autoplot/dev/search?q=value&unscoped_q=value">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

value( int i0, int i1, int i2 ) &rarr; double<br>
