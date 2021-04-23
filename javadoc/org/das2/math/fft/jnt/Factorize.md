# org.das2.math.fft.jnt.Factorize

Supplies static methods for factoring integers needed by various FFT classes.

# Factorize( )


***
<a name="factor"></a>
# factor
factor( int n, int[] fromfactors ) &rarr; int

Return the prime factors of n.
 The method first extracts any factors in fromfactors, in order (which 
 needn't actually be prime).  Remaining factors in increasing order follow.

### Parameters:
n - an int
<br>fromfactors - an int[]

### Returns:
int[]


<a href="https://github.com/autoplot/dev/search?q=factor&unscoped_q=factor">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="log2"></a>
# log2
log2( int n ) &rarr; int

Return the integer log, base 2, of n, or -1 if n is not an integral power of 2.

### Parameters:
n - an int

### Returns:
int


<a href="https://github.com/autoplot/dev/search?q=log2&unscoped_q=log2">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

