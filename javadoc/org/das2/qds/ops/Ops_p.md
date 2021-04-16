***
<a name="polarToCartesian"></a>
# polarToCartesian
polarToCartesian( QDataSet ds ) &rarr; QDataSet

converts a rank 2 bundle of polar data, where ds[:,0] are the radii and ds[:,1] 
 are the angles.  Any additional bundled datasets are left alone.

### Parameters:
ds - a QDataSet

### Returns:
bundle of X, Y, and remaining data.

<a href="https://github.com/autoplot/dev/search?q=polarToCartesian&unscoped_q=polarToCartesian">[search for examples]</a>

***
<a name="pow"></a>
# pow
pow( QDataSet ds1, QDataSet pow ) &rarr; QDataSet

element-wise pow (** in FORTRAN, ^ in IDL) of two datasets with the compatible
 geometry.

### Parameters:
ds1 - the base
<br>pow - the exponent

### Returns:
the value ds1**pow

<a href="https://github.com/autoplot/dev/search?q=pow&unscoped_q=pow">[search for examples]</a>

pow( long x, long y ) &rarr; long<br>
pow( double x, double y ) &rarr; double<br>
pow( Object ds1, Object pow ) &rarr; QDataSet<br>
***
<a name="putBundleProperty"></a>
# putBundleProperty
putBundleProperty( QDataSet ds, String name, int index, Object value ) &rarr; MutablePropertyDataSet

Like putIndexedProperty, but manages the bundle for the client.  This
 was introduced to make it easier to work with bundles.  This
 converts types often seen in Jython and Java codes to the correct type.  For
 example,  ds= putBundleProperty( ds, 'UNITS', 0, 'seconds since 2012-01-01').  
 The dataset may be copied to make it mutable. If the bundle descriptor dataset 
 is not found, it is added, making the rank 2 dataset a bundle.

### Parameters:
ds - the rank 1 or rank 2 bundle dataset to which the property is to be set.
<br>name - the property name
<br>index - the property index
<br>value - the property value, which can converted to the proper type.

### Returns:
the dataset, possibly converted to a mutable dataset.

<a href="https://github.com/autoplot/dev/search?q=putBundleProperty&unscoped_q=putBundleProperty">[search for examples]</a>

***
<a name="putIndexedProperty"></a>
# putIndexedProperty
putIndexedProperty( QDataSet ds, String name, int index, Object value ) &rarr; MutablePropertyDataSet

Like putProperty, but this inserts the value at the index.  This
 was introduced to make it easier to work with bundles.  This
 converts types often seen in Jython and Java codes to the correct type.  For
 example,  bds= putProperty( bds, 'UNITS', 0, 'seconds since 2012-01-01').  
 The dataset may be copied to make it mutable.

### Parameters:
ds - the dataset to which the property is to be set.
<br>name - the property name
<br>index - the property index
<br>value - the property value, which can converted to the proper type.

### Returns:
the dataset, possibly converted to a mutable dataset.

<a href="https://github.com/autoplot/dev/search?q=putIndexedProperty&unscoped_q=putIndexedProperty">[search for examples]</a>

***
<a name="putProperty"></a>
# putProperty
putProperty( Object ds, String name, Object value ) &rarr; MutablePropertyDataSet

converts types often seen in Jython and Java codes to the correct type.  For
 example,
 <pre>ds= putProperty( [1400,2800], 'UNITS', 'seconds since 2012-01-01')</pre>
 will convert the string 'seconds since 2012-01-01' into a Unit before assigning
 it to the dataset.

### Parameters:
ds - the object which can be interpreted as a dataset, such as a number or array of numbers.
<br>name - the property name
<br>value - the property value, which can converted to the proper type.

### Returns:
the dataset, possibly converted to a mutable dataset.

<a href="https://github.com/autoplot/dev/search?q=putProperty&unscoped_q=putProperty">[search for examples]</a>

putProperty( QDataSet ds, String name, Object value ) &rarr; MutablePropertyDataSet<br>
***
<a name="putValues"></a>
# putValues
putValues( Object ds, Object indeces, Object values ) &rarr; WritableDataSet



### Parameters:
ds - an Object
<br>indeces - an Object
<br>values - an Object

### Returns:
org.das2.qds.WritableDataSet


<a href="https://github.com/autoplot/dev/search?q=putValues&unscoped_q=putValues">[search for examples]</a>

putValues( QDataSet ds, QDataSet indeces, QDataSet value ) &rarr; WritableDataSet<br>
