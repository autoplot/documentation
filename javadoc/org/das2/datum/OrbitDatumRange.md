# org.das2.datum.OrbitDatumRangeDatumRange implementation that identifies times by orbit number.  Note orbit numbers are strings, see Cassini for why.
 next will return the same one at the end of the sequence.
 <code>
   dr= new OrbitDatumRange( "crres", "6" )
   dr.toString() &rarr; "orbit:crres:6"
   dr= dr.next()
   dr.toString() &rarr; "orbit:crres:7"
 </code>
 Also, orbit:http://das2.org/wiki/index.php/Orbits/crres:6 is supported for development work and personal lists.
OrbitDatumRange( String sc, String orbit )


OrbitDatumRange( String sc, String orbit, Units unitPref )


***
<a name="compareTo"></a>
# compareTo
compareTo( Object o ) &rarr; int



### Parameters:
o - an Object

### Returns:
int


<a href="https://github.com/autoplot/dev/search?q=compareTo&unscoped_q=compareTo">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

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
<a name="getOrbit"></a>
# getOrbit
getOrbit(  ) &rarr; String

return the string identifying this orbit, assuming the context is 
 provided elsewhere.  For example, supposing this toString() is "orbit:rbspa-pp:43"
 then this would return just "43"

### Returns:
the string providing the orbit.

<a href="https://github.com/autoplot/dev/search?q=getOrbit&unscoped_q=getOrbit">[search for examples]</a>

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

***
<a name="toString"></a>
# toString
toString(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=toString&unscoped_q=toString">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

