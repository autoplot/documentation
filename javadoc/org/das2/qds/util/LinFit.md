# org.das2.qds.util.LinFitLinear Fit routine. This will allow errors on the Y values, and will report
 chi squared.

 Borrowed from pamguard, https://sourceforge.net/projects/pamguard/.
LinFit( QDataSet x, QDataSet y )
do fit with uniform weights or weight=0 where fill is found.

LinFit( QDataSet x, QDataSet y, QDataSet sig )
do fit with weights. X and Y must not contain fill where sig&gt;0.

***
<a name="getA"></a>
# getA
getA(  ) &rarr; double

return the result A, the intercept, of the fit y = A + B * x

### Returns:
the result A of the fit y = A + B * x

<a href="https://github.com/autoplot/dev/search?q=getA&unscoped_q=getA">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getB"></a>
# getB
getB(  ) &rarr; double

return the result B, the slope, of the fit y = A + B * x

### Returns:
the result B of the fit y = A + B * x

<a href="https://github.com/autoplot/dev/search?q=getB&unscoped_q=getB">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getChi2"></a>
# getChi2
getChi2(  ) &rarr; double

return the Chi-Squared result from the fit.

### Returns:
the Chi-Squared result from the fit.

<a href="https://github.com/autoplot/dev/search?q=getChi2&unscoped_q=getChi2">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getIntercept"></a>
# getIntercept
getIntercept(  ) &rarr; Datum

return the intercept (A of linear fit equation) as a datum with units of y.

### Returns:
a Datum


<a href="https://github.com/autoplot/dev/search?q=getIntercept&unscoped_q=getIntercept">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getQ"></a>
# getQ
getQ(  ) &rarr; double



### Returns:
double


<a href="https://github.com/autoplot/dev/search?q=getQ&unscoped_q=getQ">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getSiga"></a>
# getSiga
getSiga(  ) &rarr; double



### Returns:
double


<a href="https://github.com/autoplot/dev/search?q=getSiga&unscoped_q=getSiga">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getSigb"></a>
# getSigb
getSigb(  ) &rarr; double



### Returns:
double


<a href="https://github.com/autoplot/dev/search?q=getSigb&unscoped_q=getSigb">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getSlope"></a>
# getSlope
getSlope(  ) &rarr; Datum

return the slope (B of linear fit equation) as a datum with units of Yunits/Xunits. Note the current
 version of the library is unable to do many unit calculations.

### Returns:
the slope as a Datum with units.

<a href="https://github.com/autoplot/dev/search?q=getSlope&unscoped_q=getSlope">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

