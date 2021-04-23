# org.das2.qstream.QdsToD2sStreamBase class for QDataSet to das2 stream serializers
QdsToD2sStream( )
Initialize a binary QDataSet to das2 stream exporter

QdsToD2sStream( int genSigDigits, int fracSecDigits )
Initialize a text QDataSet to das2 stream exporter

***
<a name="FORMAT_2_2"></a>
# FORMAT_2_2



***
<a name="FORMAT_2_3_BASIC"></a>
# FORMAT_2_3_BASIC



***
<a name="FORMAT_2_4_GENERAL"></a>
# FORMAT_2_4_GENERAL



***
<a name="formats"></a>
# formats



***
<a name="DEFAUT_FRAC_SEC"></a>
# DEFAUT_FRAC_SEC



***
<a name="DEFAUT_SIG_DIGIT"></a>
# DEFAUT_SIG_DIGIT



***
<a name="FIXED_PKT_TAGS"></a>
# FIXED_PKT_TAGS



***
<a name="VAR_PKT_TAGS"></a>
# VAR_PKT_TAGS



***
<a name="canWrite"></a>
# canWrite
canWrite( QDataSet qds ) &rarr; boolean

Determine if the given dataset can be written

### Parameters:
qds - a QDataSet

### Returns:
a boolean


<a href="https://github.com/autoplot/dev/search?q=canWrite&unscoped_q=canWrite">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getQdsAxis"></a>
# getQdsAxis
getQdsAxis( QDataSet qds ) &rarr; String

Determine the name of the das2 axis on which values from a dataset
 would typically be plotted.
 
 This is a duck-typing check.  Which looks at the number of dependencies 
 and planes in a dataset.  If the dataset has a PLANE_0 property, the axis
 of the PLANE_0 values is returned instead of the axis of the primary
 dataset.

### Parameters:
qds - a QDataSet

### Returns:
one of "x", "y", "z","w" or null if we can't figure it out.

<a href="https://github.com/autoplot/dev/search?q=getQdsAxis&unscoped_q=getQdsAxis">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="write"></a>
# write
write( QDataSet qds, java.io.OutputStream os ) &rarr; boolean

Write the given dataset

### Parameters:
qds - a QDataSet
<br>os - an OutputStream

### Returns:
a boolean


<a href="https://github.com/autoplot/dev/search?q=write&unscoped_q=write">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

