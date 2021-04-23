# org.das2.qds.DataSetAnnotationsPlace to experiment with runtime notes about datasets in this 
 single-instance lookup table.  This uses weak references so that 
 datasets will be garbage collected.
DataSetAnnotations( )


***
<a name="VALUE_0"></a>
# VALUE_0

the value 0 to avoid the if statement in valueOf

***
<a name="VALUE_1"></a>
# VALUE_1

the value 1 to avoid the if statement in valueOf

***
<a name="ANNOTATION_INVALID_COUNT"></a>
# ANNOTATION_INVALID_COUNT

number of invalid entries.  If zero, the data is all valid, within
 valid min to valid max and not fill.

***
<a name="ANNOTATION_ZERO_COUNT"></a>
# ANNOTATION_ZERO_COUNT

number of entries containing the value zero.  If zero, then the
 data is all non-zero or fill.  This is used with ANNOTATION_INVALID_COUNT
 in the where function.

***
<a name="ANNOTATION_BOUNDS"></a>
# ANNOTATION_BOUNDS

the bounding cube of the dataset, see SemanticOps.getBounds.

***
<a name="ANNOTATION_CADENCE"></a>
# ANNOTATION_CADENCE

the cadence for the dataset.

***
<a name="ANNOTATION_QUBE"></a>
# ANNOTATION_QUBE

qube for the dataset.

***
<a name="getAnnotation"></a>
# getAnnotation
getAnnotation( QDataSet ds, String annotation ) &rarr; Object

return either null or the value for the annotation.  Note some
 Java compilers (Java6?) will not allow code such as:<tt>
 0==DataSetAnnotations.getInstance().getAnnotation(...)
 </tt>
 so instead use
 <tt>
 Integer.valueOf(0)==DataSetAnnotations.getInstance().getAnnotation(...)
 </tt>

### Parameters:
ds - the dataset.
<br>annotation - the annotation name, such as ANNOTATION_INVALID_COUNT.

### Returns:
null or the annotation value.

<a href="https://github.com/autoplot/dev/search?q=getAnnotation&unscoped_q=getAnnotation">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getInstance"></a>
# getInstance
getInstance(  ) &rarr; DataSetAnnotations

access the single instance

### Returns:
the single instance

<a href="https://github.com/autoplot/dev/search?q=getInstance&unscoped_q=getInstance">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="peek"></a>
# peek
peek(  ) &rarr; void

print the map of annotations to stderr.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=peek&unscoped_q=peek">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="putAnnotation"></a>
# putAnnotation
putAnnotation( QDataSet ds, String annotation, Object value ) &rarr; void

add the annotation.

### Parameters:
ds - the dataset to annotate
<br>annotation - the annotation name, such as ANNOTATION_INVALID_COUNT.
<br>value - the value.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=putAnnotation&unscoped_q=putAnnotation">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="reset"></a>
# reset
reset(  ) &rarr; void

reset the internal state.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=reset&unscoped_q=reset">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

