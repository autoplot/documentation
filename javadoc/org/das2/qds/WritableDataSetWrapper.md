# org.das2.qds.WritableDataSetWrapperJython needs all datasets to be writable, and this provides the write capability while avoiding unnecessary
 copies when the dataset is never mutated.
WritableDataSetWrapper( QDataSet ds )
create the WritableDataSetWrapper

***
<a name="length"></a>
# length
length(  ) &rarr; int

return the length the dimension at the index.

### Returns:
the length of the dimension.

<a href="https://github.com/autoplot/dev/search?q=length&unscoped_q=length">[search for examples]</a>

length( int i0 ) &rarr; int<br>
length( int i0, int i1 ) &rarr; int<br>
length( int i0, int i1, int i2 ) &rarr; int<br>
***
<a name="putValue"></a>
# putValue
putValue( double d ) &rarr; void

insert the new value at this index.  If this is the first write to the dataset, 
 then a writable dataset is created.

### Parameters:
d - the value

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=putValue&unscoped_q=putValue">[search for examples]</a>

putValue( int i0, double d ) &rarr; void<br>
putValue( int i0, int i1, double d ) &rarr; void<br>
putValue( int i0, int i1, int i2, double d ) &rarr; void<br>
putValue( int i0, int i1, int i2, int i3, double d ) &rarr; void<br>
***
<a name="rank"></a>
# rank
rank(  ) &rarr; int

return the rank of the dataset.

### Returns:
the rank

<a href="https://github.com/autoplot/dev/search?q=rank&unscoped_q=rank">[search for examples]</a>

***
<a name="value"></a>
# value
value(  ) &rarr; double

return the value of this rank 0 dataset.

### Returns:
the value

<a href="https://github.com/autoplot/dev/search?q=value&unscoped_q=value">[search for examples]</a>

value( int i0 ) &rarr; double<br>
value( int i0, int i1 ) &rarr; double<br>
value( int i0, int i1, int i2 ) &rarr; double<br>
value( int i0, int i1, int i2, int i3 ) &rarr; double<br>
