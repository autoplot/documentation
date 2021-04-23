# org.das2.util.DasMath



# DasMath( )
Creates a new instance of DasMath

***
<a name="biggerOf"></a>
# biggerOf
biggerOf( double x1, double x2 ) &rarr; double



### Parameters:
x1 - a double
<br>x2 - a double

### Returns:
double


<a href="https://github.com/autoplot/dev/search?q=biggerOf&unscoped_q=biggerOf">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="exp10"></a>
# exp10
exp10( double x ) &rarr; double



### Parameters:
x - a double

### Returns:
double


<a href="https://github.com/autoplot/dev/search?q=exp10&unscoped_q=exp10">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

exp10( int x ) &rarr; double<br>
***
<a name="findex"></a>
# findex
findex( double[] datax, double[] x ) &rarr; double

Returns the "floating point indeces" of x within array datax.
 A floating point index (or "findex") indicates the indeces
 of the points that bracket and the weights of each bracketing
 point to use.  A findex of 4.5 indicates that x is half-way
 between index 4 and 5, so equal weights should be used.
 floor( findex ) is the "left" bracket, ceil(findex) is the
 "right" bracket, and fp( findex ) is the weight for the
 right bracket.  See interpolate for an example of its use.

### Parameters:
datax - a double[]
<br>x - a double[]

### Returns:
double[]


<a href="https://github.com/autoplot/dev/search?q=findex&unscoped_q=findex">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

findex( double[] datax, double x, int guess ) &rarr; double<br>
***
<a name="gcd"></a>
# gcd
gcd( double[] A, double error ) &rarr; double



### Parameters:
A - a double[]
<br>error - a double

### Returns:
double


<a href="https://github.com/autoplot/dev/search?q=gcd&unscoped_q=gcd">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="interpolate"></a>
# interpolate
interpolate( double[] datay, double findex ) &rarr; double

Interpolate just one point

### Parameters:
datay - a double[]
<br>findex - a double

### Returns:
double


<a href="https://github.com/autoplot/dev/search?q=interpolate&unscoped_q=interpolate">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

interpolate( double[] datay, double[] findex ) &rarr; double<br>
***
<a name="log10"></a>
# log10
log10( double x ) &rarr; double



### Parameters:
x - a double

### Returns:
double


<a href="https://github.com/autoplot/dev/search?q=log10&unscoped_q=log10">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="main"></a>
# main
main( java.lang.String[] args ) &rarr; void



### Parameters:
args - a java.lang.String[]

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=main&unscoped_q=main">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="max"></a>
# max
max( double[] A ) &rarr; double

return the maximum of the list

### Parameters:
A - the list

### Returns:
the maximum of the list

<a href="https://github.com/autoplot/dev/search?q=max&unscoped_q=max">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="mean"></a>
# mean
mean( double[] A ) &rarr; double

return the mean of the list. The first element's magnitude is
 removed from each accumulated value so that items with large offset 
 values (for example times) can be averaged.  There is no checking
 for NaNs or fill values.

### Parameters:
A - a double[]

### Returns:
the mean of the list.

<a href="https://github.com/autoplot/dev/search?q=mean&unscoped_q=mean">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="median"></a>
# median
median( double[] A ) &rarr; double

return the median of the list length N, which is the value at index N/2 of 
 the sorted list.  This does not return the average for even-length lists.
 and there is no checking for NaNs or fill values.

### Parameters:
A - a double[]

### Returns:
the median of the list

<a href="https://github.com/autoplot/dev/search?q=median&unscoped_q=median">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="min"></a>
# min
min( double[] A ) &rarr; double

return the minimum of the list

### Parameters:
A - the list

### Returns:
the minimum of the list

<a href="https://github.com/autoplot/dev/search?q=min&unscoped_q=min">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="modp"></a>
# modp
modp( double x, double t ) &rarr; double

just like modulo (%) function, but negative numbers return positive phase.

### Parameters:
x - a double
<br>t - a double

### Returns:
double


<a href="https://github.com/autoplot/dev/search?q=modp&unscoped_q=modp">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

modp( int x, int t ) &rarr; int<br>
***
<a name="roundNFractionalDigits"></a>
# roundNFractionalDigits
roundNFractionalDigits( double x, int n ) &rarr; double



### Parameters:
x - a double
<br>n - an int

### Returns:
double


<a href="https://github.com/autoplot/dev/search?q=roundNFractionalDigits&unscoped_q=roundNFractionalDigits">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="roundNSignificantDigits"></a>
# roundNSignificantDigits
roundNSignificantDigits( double x, int n ) &rarr; double



### Parameters:
x - a double
<br>n - an int

### Returns:
double


<a href="https://github.com/autoplot/dev/search?q=roundNSignificantDigits&unscoped_q=roundNSignificantDigits">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="sort"></a>
# sort
sort( double[] A ) &rarr; double

return a sorted version of the array.  The original array is not
 modified.

### Parameters:
A - a double[]

### Returns:
return a sorted version of the array.

<a href="https://github.com/autoplot/dev/search?q=sort&unscoped_q=sort">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="tanh"></a>
# tanh
tanh( double x ) &rarr; double



### Parameters:
x - a double

### Returns:
double


<a href="https://github.com/autoplot/dev/search?q=tanh&unscoped_q=tanh">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

