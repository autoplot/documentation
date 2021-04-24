# org.das2.qds.LongWriteAccess

Provide write access to the long array which backs the data.
 For example, this could be used with LongDataSet to 
 provide access to the original TT2000 values of a 
 CDF file.

***
<a name="putLValue"></a>
# putLValue
putLValue( long value ) &rarr; void



### Parameters:
value - a long

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=putLValue&unscoped_q=putLValue">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

putLValue( int i0, long value ) &rarr; void<br>
putLValue( int i0, int i1, long value ) &rarr; void<br>
putLValue( int i0, int i1, int i2, long value ) &rarr; void<br>
putLValue( int i0, int i1, int i2, int i3, long value ) &rarr; void<br>
