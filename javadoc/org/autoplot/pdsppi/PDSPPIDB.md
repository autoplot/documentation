# org.autoplot.pdsppi.PDSPPIDBClass containing the logic for communicating with the PDS-PPI database.
PDSPPIDB( )


***
<a name="PDSPPI"></a>
# PDSPPI



***
<a name="checkTimeSeriesBrowse"></a>
# checkTimeSeriesBrowse
checkTimeSeriesBrowse( String uri ) &rarr; String

parameterize the URI so that any number of files can be read in.  For example,
<blockquote><pre><small>
 vap+pdsppi:sc=Cassini&id=PPI/CO-S-MIMI-4-LEMMS-CALIB-V1.0/DATA/LACCAVG0_1MIN/2006/LACCAVG0_1MIN_2006269_01&param=E0
</small></pre></blockquote>
 would result in 
<blockquote><pre><small>
vap+pdsppi:sc=Cassini&id=PPI/CO-S-MIMI-4-LEMMS-CALIB-V1.0/DATA/LACCAVG0_1MIN/$Y/LACCAVG0_1MIN_$Y$j_01&param=E0
</small></pre></blockquote>

### Parameters:
uri - a String

### Returns:
the aggregation URI or null.

<a href="https://github.com/autoplot/dev/search?q=checkTimeSeriesBrowse&unscoped_q=checkTimeSeriesBrowse">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getIds"></a>
# getIds
getIds(  ) &rarr; List



### Returns:
java.util.List


<a href="https://github.com/autoplot/dev/search?q=getIds&unscoped_q=getIds">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

getIds( java.util.regex.Pattern p ) &rarr; List<br>
getIds( String constraint, String reqPrefix ) &rarr; String<br>
***
<a name="getInstance"></a>
# getInstance
getInstance(  ) &rarr; PDSPPIDB



### Returns:
org.autoplot.pdsppi.PDSPPIDB


<a href="https://github.com/autoplot/dev/search?q=getInstance&unscoped_q=getInstance">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getParams"></a>
# getParams
getParams( String id, ProgressMonitor mon ) &rarr; Map

return a list of the plottable parameter datasets within the ID.
 TODO: this loads the entire dataset, this will be fixed.

### Parameters:
id - a String
<br>mon - a ProgressMonitor

### Returns:
Map label->title of the params.

<a href="https://github.com/autoplot/dev/search?q=getParams&unscoped_q=getParams">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getSpacecraft"></a>
# getSpacecraft
getSpacecraft(  ) &rarr; String

returns the spacecraft.

### Returns:
a java.lang.String[]


<a href="https://github.com/autoplot/dev/search?q=getSpacecraft&unscoped_q=getSpacecraft">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isPlottable"></a>
# isPlottable
isPlottable( String ds ) &rarr; boolean

return true if the name appears to be a plottable id.

### Parameters:
ds - name from their filesystem that ends with .lbl, .tab, etc.

### Returns:
true if the id appears to be plottable.

<a href="https://github.com/autoplot/dev/search?q=isPlottable&unscoped_q=isPlottable">[search for examples]</a>

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
<a name="removeExtraSlashes"></a>
# removeExtraSlashes
removeExtraSlashes( String root ) &rarr; String

apparently the id needs to have underscores where there are slashes...  e.g.
 PPI/CO-E/J/S/SW-CAPS-5-DDR-ELE-MOMENTS-V1.0 -> PPI/CO-E_J_S_SW-CAPS-5-DDR-ELE-MOMENTS-V1.0

### Parameters:
root - like PPI/CO-E/J/S/SW-CAPS-5-DDR-ELE-MOMENTS-V1.0/

### Returns:
result like PPI/CO-E_J_S_SW-CAPS-5-DDR-ELE-MOMENTS-V1.0

<a href="https://github.com/autoplot/dev/search?q=removeExtraSlashes&unscoped_q=removeExtraSlashes">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

