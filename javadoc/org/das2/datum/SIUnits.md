# org.das2.datum.SIUnitsFinally introduce SI Units library, which preserves units through
 multiplication and division.
***
<a name="add"></a>
# add
add( Number a, Number b, Units bUnits ) &rarr; Datum



### Parameters:
a - a Number
<br>b - a Number
<br>bUnits - an Units

### Returns:
org.das2.datum.Datum


<a href="https://github.com/autoplot/dev/search?q=add&unscoped_q=add">[search for examples]</a>

***
<a name="create"></a>
# create
create( String id ) &rarr; SIUnits



### Parameters:
id - a String

### Returns:
org.das2.datum.SIUnits


<a href="https://github.com/autoplot/dev/search?q=create&unscoped_q=create">[search for examples]</a>

create( String id, String desc, org.das2.datum.Ratio m, org.das2.datum.Ratio kg, org.das2.datum.Ratio s, org.das2.datum.Ratio A, org.das2.datum.Ratio K, org.das2.datum.RationalNumber multiplier ) &rarr; SIUnits<br>
create( String id, String desc, int m, int kg, int s, double multiplier ) &rarr; SIUnits<br>
create( String id, String desc, int m, int kg, int s ) &rarr; SIUnits<br>
create( String id, String desc, int m, int kg, int s, int A, int K ) &rarr; SIUnits<br>
create( String id, String desc, org.das2.datum.Ratio m, org.das2.datum.Ratio k, org.das2.datum.Ratio s, org.das2.datum.RationalNumber multiplier ) &rarr; SIUnits<br>
***
<a name="divide"></a>
# divide
divide( Number a, Number b, Units bUnits ) &rarr; Datum



### Parameters:
a - a Number
<br>b - a Number
<br>bUnits - an Units

### Returns:
org.das2.datum.Datum


<a href="https://github.com/autoplot/dev/search?q=divide&unscoped_q=divide">[search for examples]</a>

***
<a name="fromClusterCDFSIConversion"></a>
# fromClusterCDFSIConversion
fromClusterCDFSIConversion( String si, String id, String desc ) &rarr; SIUnits

Cluster CDFs had "SI_Conversion" that showed how to convert to SI units.
 Parse this string. For example: SI_conversion=<code>"1.0e-3>V m^-1"</code>

### Parameters:
si - the string.
<br>id - a String
<br>desc - a String

### Returns:
the SIUnits

<a href="https://github.com/autoplot/dev/search?q=fromClusterCDFSIConversion&unscoped_q=fromClusterCDFSIConversion">[search for examples]</a>

***
<a name="main"></a>
# main
main( java.lang.String[] args ) &rarr; void



### Parameters:
args - a java.lang.String[]

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=main&unscoped_q=main">[search for examples]</a>

***
<a name="multiply"></a>
# multiply
multiply( org.das2.datum.SIUnits s1, org.das2.datum.SIUnits s2 ) &rarr; SIUnits



### Parameters:
s1 - a SIUnits
<br>s2 - a SIUnits

### Returns:
org.das2.datum.SIUnits


<a href="https://github.com/autoplot/dev/search?q=multiply&unscoped_q=multiply">[search for examples]</a>

multiply( String id, String desc, org.das2.datum.SIUnits s1, org.das2.datum.RationalNumber s ) &rarr; SIUnits<br>
multiply( Number a, Number b, Units bUnits ) &rarr; Datum<br>
***
<a name="pow"></a>
# pow
pow( org.das2.datum.SIUnits s1, int pow ) &rarr; SIUnits

apply the power to the exponent.  For example
 pow(Units.kg,2)&rarr; kg**2
 pow(Units.cm,2)&rarr; cm**2 == .01^2 * m^2.
 Units.kg

### Parameters:
s1 - the unit, e.g. SIUnits.si_Hz
<br>pow - the exponent e.g. -1

### Returns:
SI unit, e.g. SIUnits.si_s

<a href="https://github.com/autoplot/dev/search?q=pow&unscoped_q=pow">[search for examples]</a>

***
<a name="subtract"></a>
# subtract
subtract( Number a, Number b, Units bUnits ) &rarr; Datum



### Parameters:
a - a Number
<br>b - a Number
<br>bUnits - an Units

### Returns:
org.das2.datum.Datum


<a href="https://github.com/autoplot/dev/search?q=subtract&unscoped_q=subtract">[search for examples]</a>

***
<a name="toString"></a>
# toString
toString(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=toString&unscoped_q=toString">[search for examples]</a>

