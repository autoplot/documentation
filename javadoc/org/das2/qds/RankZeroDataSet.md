# org.das2.qds.RankZeroDataSet

interface provide access to a rank 0 dataset, which can be thought of as
 a scalar (and set of correlated scalars) with metadata.

 This is a marker interface, since it no longer adds any new methods to the
 interface.  TODO: this really needs to be studied, see 
 org.virbo.qstream.SimpleStreamFormatter.timeDigits(SimpleStreamFormatter.java:188)
 which would assume the data was a rank0 dataset, which it once was because
 it came from slice0.

***
<a name="property"></a>
# property
property( String name ) &rarr; Object



### Parameters:
name - a String

### Returns:
java.lang.Object


<a href="https://github.com/autoplot/dev/search?q=property&unscoped_q=property">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="value"></a>
# value
value(  ) &rarr; double

rank 0 accessor.

### Returns:
the scalar value stored in this dataset.

<a href="https://github.com/autoplot/dev/search?q=value&unscoped_q=value">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

