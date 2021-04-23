# org.das2.qds.TagGenDataSet

return a value based on the scale and offset.  For example, this
 is used to create timetags:
 <blockquote><pre>
   TagGenDataSet( 1440, 60, 0, Units.t2000 )
 </pre></blockquote>
 These are the 1440 minutely timetags in the first day of 2000-01-01.

# TagGenDataSet( int length, double scale, double offset )
create new dimensionless TagGenDataSet

# TagGenDataSet( int length, double scale, double offset, Units units )
create new TagGenDataSet

***
<a name="slice"></a>
# slice
slice( int i ) &rarr; QDataSet



### Parameters:
i - an int

### Returns:
org.das2.qds.QDataSet


<a href="https://github.com/autoplot/dev/search?q=slice&unscoped_q=slice">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="trim"></a>
# trim
trim( int start, int end ) &rarr; QDataSet



### Parameters:
start - an int
<br>end - an int

### Returns:
org.das2.qds.QDataSet


<a href="https://github.com/autoplot/dev/search?q=trim&unscoped_q=trim">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="value"></a>
# value
value( int i ) &rarr; double



### Parameters:
i - an int

### Returns:
double


<a href="https://github.com/autoplot/dev/search?q=value&unscoped_q=value">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

