# org.das2.qds.WritableDataSetSome QDataSets are be mutable as well, meaning their values can be assigned
 as well as read.  In addition to the value() method they have putValue() methods.
 These datasets cannot be written to once they are made 
 immutable by calling the makeImmutable() of MutablePropertyDataSet, and clients 
 must check the isImmutable flag or call Ops.maybeCopy when they need write 
 access to the data.
   
 Mutable datasets warning: No dataset should be mutable once it is accessible to the
 rest of the system.  This would require clients make defensive copies which would 
 seriously degrade performance.
***
<a name="putValue"></a>
# putValue
putValue( double d ) &rarr; void

put a value into the rank 0 dataset.

### Parameters:
d - the value

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=putValue&unscoped_q=putValue">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

putValue( int i0, double d ) &rarr; void<br>
putValue( int i0, int i1, double d ) &rarr; void<br>
putValue( int i0, int i1, int i2, double d ) &rarr; void<br>
putValue( int i0, int i1, int i2, int i3, double d ) &rarr; void<br>
