# org.autoplot.tca.UriTcaSourceAllow Autoplot URIs to supply data to label plots.

   class:org.autoplot.tca.AutoplotTCASource:vap+file:/tmp/foo.txt?rank2=field1-field4&depend0=field0
   class:org.autoplot.tca.AutoplotTCASource:vap+dat:file:/home/jbf/project/autoplot/data/dat/rockets/21139_E_field.txt?skipLines=1&depend0=field0&rank2=field3-field4
UriTcaSource( String uri )


***
<a name="exampleInput"></a>
# exampleInput
exampleInput(  ) &rarr; QDataSet



### Returns:
org.das2.qds.QDataSet


<a href="https://github.com/autoplot/dev/search?q=exampleInput&unscoped_q=exampleInput">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="value"></a>
# value
value( QDataSet parm ) &rarr; QDataSet



### Parameters:
parm - a QDataSet

### Returns:
org.das2.qds.QDataSet


<a href="https://github.com/autoplot/dev/search?q=value&unscoped_q=value">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="values"></a>
# values
values( QDataSet parms ) &rarr; QDataSet

This will set the focus range for the TimeSeriesBrowse, if available, 
 and then call each tick individually.

### Parameters:
parms - a QDataSet

### Returns:
a QDataSet


<a href="https://github.com/autoplot/dev/search?q=values&unscoped_q=values">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

