***
<a name="valid"></a>
# valid
valid( QDataSet ds ) &rarr; QDataSet

returns a dataset with zero where the data is invalid, and positive 
 non-zero where the data is valid.  (This just returns the weights
 plane of the dataset.)
<blockquote><pre>
r= where( valid( ds ) )
</pre></blockquote>

### Parameters:
ds - a rank N dataset that might have FILL_VALUE, VALID_MIN or VALID_MAX
   set.

### Returns:
a rank N dataset with the same geometry, with zeros where the data
   is invalid and &gt;0 where the data is valid.

<a href="https://github.com/autoplot/dev/search?q=valid&unscoped_q=valid">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="variance"></a>
# variance
variance( Object o ) &rarr; QDataSet



### Parameters:
o - an Object

### Returns:
org.das2.qds.QDataSet


<a href="https://github.com/autoplot/dev/search?q=variance&unscoped_q=variance">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

variance( QDataSet ds ) &rarr; QDataSet<br>
