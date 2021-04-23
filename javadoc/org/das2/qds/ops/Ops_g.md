***
<a name="gamma"></a>
# gamma
gamma( double n ) &rarr; double

return the gamma function for numbers greater than 0.  This will 
 soon work for any number where gamma has a result (Apache Math v3 is needed for this).

### Parameters:
n - a double

### Returns:
a double


<a href="https://github.com/autoplot/dev/search?q=gamma&unscoped_q=gamma">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

gamma( Object n ) &rarr; QDataSet<br>
***
<a name="ge"></a>
# ge
ge( QDataSet ds1, QDataSet ds2 ) &rarr; QDataSet

element-wise function returns 1 where ds1&gt;=ds2.

### Parameters:
ds1 - a QDataSet
<br>ds2 - a QDataSet

### Returns:
a QDataSet


<a href="https://github.com/autoplot/dev/search?q=ge&unscoped_q=ge">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

ge( Object ds1, Object ds2 ) &rarr; QDataSet<br>
***
<a name="getProperty"></a>
# getProperty
getProperty( QDataSet ds, String name ) &rarr; Object

retrieve a property from the dataset.  This was introduced for use
 in the Data Mash Up tool.

### Parameters:
ds - the dataset
<br>name - the property name

### Returns:
the property or null (None) if the dataset doesn't have the property.

<a href="https://github.com/autoplot/dev/search?q=getProperty&unscoped_q=getProperty">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

getProperty( QDataSet ds, String propertyName, java.lang.Class clazz ) &rarr; Object<br>
***
<a name="getQubeDimsForArray"></a>
# getQubeDimsForArray
getQubeDimsForArray( Object arg0 ) &rarr; int

return the length of each index of a n-D array.  In Java these are
 arrays of arrays, and no test is made to verify that the array is really
 a qube.  This was introduced when it appeared that Python/jpype was
 producing arrays without the getClass method.
 
 For example, if we have an array of 3 arrays, each having 5 elements, 
 then [ 3,5 ] is returned.

### Parameters:
arg0 - an array, or array of arrays, or array of array of arrays, etc.

### Returns:
the n dimensions of each index of the array.

<a href="https://github.com/autoplot/dev/search?q=getQubeDimsForArray&unscoped_q=getQubeDimsForArray">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="greaterOf"></a>
# greaterOf
greaterOf( QDataSet ds1, QDataSet ds2 ) &rarr; QDataSet

element-wise function returns the greater of ds1 and ds2.
 If an element of ds1 or ds2 is fill, then the result is fill.

### Parameters:
ds1 - a QDataSet
<br>ds2 - a QDataSet

### Returns:
the bigger of the two, in the units of ds1.

<a href="https://github.com/autoplot/dev/search?q=greaterOf&unscoped_q=greaterOf">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

greaterOf( Object ds1, Object ds2 ) &rarr; QDataSet<br>
***
<a name="grid"></a>
# grid
grid( QDataSet ds ) &rarr; QDataSet

Opposite of the flatten function, takes rank 2 bundle (x,y,z) and 
 makes a table from it z(x,y). This presumes that the rank 1 X and
 Y data contain repeating elements for the rows and columns of the grid.

### Parameters:
ds - rank 2 bundle of X,Y, and Z data.

### Returns:
rank 2 table.
### See Also:
<a href='Ops_f.md#flatten'>flatten(QDataSet)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=grid&unscoped_q=grid">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="gridIrregularY"></a>
# gridIrregularY
gridIrregularY( QDataSet t, QDataSet y, QDataSet z, QDataSet ytags ) &rarr; QDataSet

This finds sweeps of Y and interpolates T->Y->Z to make a regular 
 spectrogram T,yTags->Z[T,yTags] 
 This function was once known as "LvT" because it was used to create a spectrogram
 of Flux(Time,Lshell) by interpolating along sweeps.

### Parameters:
t - the rank 1 x values (often time)
<br>y - the rank 1 y values (for example, L)
<br>z - the rank 1 z values at each y.
<br>ytags - the rank 1 y tags for the result.

### Returns:
the rank 2 spectrogram.

<a href="https://github.com/autoplot/dev/search?q=gridIrregularY&unscoped_q=gridIrregularY">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="gt"></a>
# gt
gt( QDataSet ds1, QDataSet ds2 ) &rarr; QDataSet

element-wise function returns 1 where ds1&gt;ds2.

### Parameters:
ds1 - a QDataSet
<br>ds2 - a QDataSet

### Returns:
a QDataSet


<a href="https://github.com/autoplot/dev/search?q=gt&unscoped_q=gt">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

gt( Object ds1, Object ds2 ) &rarr; QDataSet<br>
***
<a name="guessLabel"></a>
# guessLabel
guessLabel( QDataSet ds ) &rarr; String

get the label, using the NAME when LABEL is not available.

### Parameters:
ds - the dataset

### Returns:
the human-readable label.

<a href="https://github.com/autoplot/dev/search?q=guessLabel&unscoped_q=guessLabel">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

guessLabel( QDataSet ds, String deft ) &rarr; String<br>
***
<a name="guessName"></a>
# guessName
guessName( QDataSet ds ) &rarr; String

guess a name for the dataset, looking for NAME and then safeName(LABEL).  The
 result will be a Java-style identifier suitable for the variable.

### Parameters:
ds - the dataset

### Returns:
the name or null if there is no NAME or LABEL

<a href="https://github.com/autoplot/dev/search?q=guessName&unscoped_q=guessName">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

guessName( QDataSet ds, String deft ) &rarr; String<br>
