# org.das2.datum.LeapSecondsConverter

TT2000 converter that takes leap seconds into account from us2000.

# LeapSecondsConverter( boolean us2000ToTT2000 )


***
<a name="T1972_LEAP"></a>
# T1972_LEAP



***
<a name="convert"></a>
# convert
convert( double value ) &rarr; double



### Parameters:
value - a double

### Returns:
double


<a href="https://github.com/autoplot/dev/search?q=convert&unscoped_q=convert">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getInverse"></a>
# getInverse
getInverse(  ) &rarr; UnitsConverter



### Returns:
org.das2.datum.UnitsConverter


<a href="https://github.com/autoplot/dev/search?q=getInverse&unscoped_q=getInverse">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getLeapSecondCountForTT2000"></a>
# getLeapSecondCountForTT2000
getLeapSecondCountForTT2000( long tt2000 ) &rarr; int

calculate the number of leap seconds in the tt2000 time.  For example,
 <pre>
 
 print getLeapSecondCountForTT2000( Units.cdfTT2000.parse('1972-01-01T00:00Z').doubleValue(Units.cdfTT2000) ) # results in 10
 print getLeapSecondCountForTT2000( 0 )   # results in 32
 print getLeapSecondCountForTT2000( Units.cdfTT2000.parse('2017-01-01T00:00Z').doubleValue(Units.cdfTT2000) ) # results in 37
 
 </pre>
 This is intended to replicate the table https://cdf.gsfc.nasa.gov/html/CDFLeapSeconds.txt

### Parameters:
tt2000 - the time in tt2000, which include the leap seconds.

### Returns:
the number of leap seconds for the time.

<a href="https://github.com/autoplot/dev/search?q=getLeapSecondCountForTT2000&unscoped_q=getLeapSecondCountForTT2000">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getLeapSecondCountForUs2000"></a>
# getLeapSecondCountForUs2000
getLeapSecondCountForUs2000( double us2000 ) &rarr; int

calculate the number of leap seconds in the us2000 time.  For example,
 <pre>
 
 print getLeapSecondCountForUs2000( Units.us2000.parse('1972-01-01T00:00Z').doubleValue(Units.us2000) ) # results in 10
 print getLeapSecondCountForUs2000( Units.us2000.parse('2017-01-01T00:00Z').doubleValue(Units.us2000) ) # results in 37
 
 </pre>
 This is intended to replicate the table https://cdf.gsfc.nasa.gov/html/CDFLeapSeconds.txt

### Parameters:
us2000 - the time in us2000, which include the leap seconds.

### Returns:
the number of leap seconds for the time.

<a href="https://github.com/autoplot/dev/search?q=getLeapSecondCountForUs2000&unscoped_q=getLeapSecondCountForUs2000">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

