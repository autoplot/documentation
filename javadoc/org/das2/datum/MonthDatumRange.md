# org.das2.datum.MonthDatumRangeDatumRange implementation that preserves month and year boundaries in the next() and previous() implementations.  For example,
<blockquote><pre>
   dr= MonthDatumRange( [ 1999, 01, 01, 00, 00, 00, 0 ], [ 1999, 02, 01, 00, 00, 00, 0 ] )
   dr.toString() &rarr; "Jan 1999"
   dr= dr.next()
   dr.toString() &rarr; "Feb 1999"  ; a normal datumRange would simply advance 31 days.
</pre></blockquote>
MonthDatumRange( int[] start, int[] end, Units u )
create the MonthDatumRange with the decomposed times.

MonthDatumRange( int[] start, int[] end )
create the MonthDatumRange with the decomposed times.

***
<a name="convertTo"></a>
# convertTo
convertTo( Units u ) &rarr; DatumRange



### Parameters:
u - an Units

### Returns:
org.das2.datum.DatumRange


<a href="https://github.com/autoplot/dev/search?q=convertTo&unscoped_q=convertTo">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="equals"></a>
# equals
equals( Object o ) &rarr; boolean



### Parameters:
o - an Object

### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=equals&unscoped_q=equals">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="hashCode"></a>
# hashCode
hashCode(  ) &rarr; int



### Returns:
int


<a href="https://github.com/autoplot/dev/search?q=hashCode&unscoped_q=hashCode">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="next"></a>
# next
next(  ) &rarr; DatumRange



### Returns:
org.das2.datum.DatumRange


<a href="https://github.com/autoplot/dev/search?q=next&unscoped_q=next">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="previous"></a>
# previous
previous(  ) &rarr; DatumRange



### Returns:
org.das2.datum.DatumRange


<a href="https://github.com/autoplot/dev/search?q=previous&unscoped_q=previous">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

