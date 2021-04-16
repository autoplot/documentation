# org.das2.datum.RationalNumberrepresent a rational number
RationalNumber( double d )
create a rationalNumber that is very close to d.

RationalNumber( org.das2.datum.Ratio n, org.das2.datum.Ratio exp )
create a rationalNumber with n * 10^exp

RationalNumber( org.das2.datum.Ratio n )
create a rationalNumber with n * 10^exp

RationalNumber( int n )
create a rationalNumber with n * 10^exp

RationalNumber( int n, int d )
create a new rational number with numerator n and denominator d. The
 result will be n/d*10^0

***
<a name="divide"></a>
# divide
divide( org.das2.datum.RationalNumber number ) &rarr; RationalNumber

divide by the number.

### Parameters:
number - a RationalNumber

### Returns:
an org.das2.datum.RationalNumber


<a href="https://github.com/autoplot/dev/search?q=divide&unscoped_q=divide">[search for examples]</a>

***
<a name="doubleValue"></a>
# doubleValue
doubleValue(  ) &rarr; double

return a close representation using double.

### Returns:
a double


<a href="https://github.com/autoplot/dev/search?q=doubleValue&unscoped_q=doubleValue">[search for examples]</a>

***
<a name="isOne"></a>
# isOne
isOne(  ) &rarr; boolean

return true if the number is 1.

### Returns:
true if the number is 1.

<a href="https://github.com/autoplot/dev/search?q=isOne&unscoped_q=isOne">[search for examples]</a>

***
<a name="isZero"></a>
# isZero
isZero(  ) &rarr; boolean

return true if the number is 0.

### Returns:
true if the number is 0.

<a href="https://github.com/autoplot/dev/search?q=isZero&unscoped_q=isZero">[search for examples]</a>

***
<a name="multiply"></a>
# multiply
multiply( org.das2.datum.RationalNumber number ) &rarr; RationalNumber

multiply by the number

### Parameters:
number - a RationalNumber

### Returns:
an org.das2.datum.RationalNumber


<a href="https://github.com/autoplot/dev/search?q=multiply&unscoped_q=multiply">[search for examples]</a>

***
<a name="parse"></a>
# parse
parse( String s ) &rarr; RationalNumber

parse the string to get the RationalNumber. This simply calls
 Double.parseDouble, but a future implementation could do a better job of
 this.

### Parameters:
s - the string.

### Returns:
the RationalNumber

<a href="https://github.com/autoplot/dev/search?q=parse&unscoped_q=parse">[search for examples]</a>

***
<a name="pow"></a>
# pow
pow( org.das2.datum.Ratio r ) &rarr; RationalNumber



### Parameters:
r - a Ratio

### Returns:
org.das2.datum.RationalNumber


<a href="https://github.com/autoplot/dev/search?q=pow&unscoped_q=pow">[search for examples]</a>

***
<a name="sqrt"></a>
# sqrt
sqrt(  ) &rarr; RationalNumber

returns the sqrt of the number, e.g. 4 * 10^

### Returns:
an org.das2.datum.RationalNumber


<a href="https://github.com/autoplot/dev/search?q=sqrt&unscoped_q=sqrt">[search for examples]</a>

***
<a name="toString"></a>
# toString
toString(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=toString&unscoped_q=toString">[search for examples]</a>

