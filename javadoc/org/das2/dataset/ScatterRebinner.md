# org.das2.dataset.ScatterRebinner
ScatterRebinner( )


***
<a name="CreateTemplateBox"></a>
# CreateTemplateBox
CreateTemplateBox( int xHardBinPlus, int xHardBinMinus, int yHardBinPlus, int yHardBinMinus, int xSoftRad, int ySoftRad ) &rarr; double



### Parameters:
xHardBinPlus - an int
<br>xHardBinMinus - an int
<br>yHardBinPlus - an int
<br>yHardBinMinus - an int
<br>xSoftRad - an int
<br>ySoftRad - an int

### Returns:
double[][]


<a href="https://github.com/autoplot/dev/search?q=CreateTemplateBox&unscoped_q=CreateTemplateBox">[search for examples]</a>

***
<a name="EllipseValue"></a>
# EllipseValue
EllipseValue( int xDist, int yDist, double xR, double yR ) &rarr; double



### Parameters:
xDist - an int
<br>yDist - an int
<br>xR - a double
<br>yR - a double

### Returns:
double


<a href="https://github.com/autoplot/dev/search?q=EllipseValue&unscoped_q=EllipseValue">[search for examples]</a>

***
<a name="InBinPlusMinuxHardEdgeBox"></a>
# InBinPlusMinuxHardEdgeBox
InBinPlusMinuxHardEdgeBox( int xPlusMinus, int yPlusMinus, int xHardBinPlus, int xHardBinMinus, int yHardBinPlus, int yHardBinMinus ) &rarr; boolean



### Parameters:
xPlusMinus - an int
<br>yPlusMinus - an int
<br>xHardBinPlus - an int
<br>xHardBinMinus - an int
<br>yHardBinPlus - an int
<br>yHardBinMinus - an int

### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=InBinPlusMinuxHardEdgeBox&unscoped_q=InBinPlusMinuxHardEdgeBox">[search for examples]</a>

***
<a name="InEllipseCutoff"></a>
# InEllipseCutoff
InEllipseCutoff( int xDist, int yDist, double xR, double yR ) &rarr; boolean



### Parameters:
xDist - an int
<br>yDist - an int
<br>xR - a double
<br>yR - a double

### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=InEllipseCutoff&unscoped_q=InEllipseCutoff">[search for examples]</a>

***
<a name="getBinWidths"></a>
# getBinWidths
getBinWidths( org.das2.dataset.RebinDescriptor rebinDesc ) &rarr; double



### Parameters:
rebinDesc - a RebinDescriptor

### Returns:
double[]


<a href="https://github.com/autoplot/dev/search?q=getBinWidths&unscoped_q=getBinWidths">[search for examples]</a>

***
<a name="getCadenceValues"></a>
# getCadenceValues
getCadenceValues( double[] binWidths, double CadenceValue, int maxSep ) &rarr; int



### Parameters:
binWidths - a double[]
<br>CadenceValue - a double
<br>maxSep - an int

### Returns:
int[]


<a href="https://github.com/autoplot/dev/search?q=getCadenceValues&unscoped_q=getCadenceValues">[search for examples]</a>

***
<a name="rebin"></a>
# rebin
rebin( QDataSet zds, org.das2.dataset.RebinDescriptor ddX, org.das2.dataset.RebinDescriptor ddY, org.das2.dataset.RebinDescriptor ddZ ) &rarr; QDataSet



### Parameters:
zds - a QDataSet
<br>ddX - a RebinDescriptor
<br>ddY - a RebinDescriptor
<br>ddZ - a RebinDescriptor

### Returns:
org.das2.qds.QDataSet


<a href="https://github.com/autoplot/dev/search?q=rebin&unscoped_q=rebin">[search for examples]</a>

