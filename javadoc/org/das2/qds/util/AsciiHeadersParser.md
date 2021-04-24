# org.das2.qds.util.AsciiHeadersParser

This additional support for parsing ascii data looks at the comment block in
 an ASCII file for a structured set of Dataset tags further describing the
 data.  This is loosely formatted JSON that describes each column of the
 data file more abstractly than the AsciiParser.

 This is based on QDataSet metadata tags, as much as possible.

# AsciiHeadersParser( )


***
<a name="PROP_DIMENSION"></a>
# PROP_DIMENSION

property for dimension of the data defining rank and qube dims. For example,
   "[]" (default}
   "[1]" scalar--alternate form, and [] is preferred.
   "[3]" (three element vector)
   "[20,30]" (qube of 60 elements).

***
<a name="PROP_ELEMENT_NAMES"></a>
# PROP_ELEMENT_NAMES

NAME identifier to assign to each column of the parameter.  These should follow QDataSet NAME rules.
 This is always a 1-D array.

***
<a name="PROP_ELEMENT_LABELS"></a>
# PROP_ELEMENT_LABELS

Human-readable label for each column of the parameter.

***
<a name="getInlineDataSet"></a>
# getInlineDataSet
getInlineDataSet( QDataSet bds, String name ) &rarr; QDataSet

allow inline dataset to be retrieved.

### Parameters:
bds - a BundleDescriptor, from BUNDLE_1.  This must have been created by this code.
<br>name - the name of the inline dataset

### Returns:
the dataset, or null if the dataset is not found.

<a href="https://github.com/autoplot/dev/search?q=getInlineDataSet&unscoped_q=getInlineDataSet">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getInlineDataSetNames"></a>
# getInlineDataSetNames
getInlineDataSetNames( QDataSet bds ) &rarr; String

return the list of inline dataset names.  This was probably used during
 development.

### Parameters:
bds - bundle dataset descriptor, though only BundleDescriptor is supported.

### Returns:
the inline dataset names.

<a href="https://github.com/autoplot/dev/search?q=getInlineDataSetNames&unscoped_q=getInlineDataSetNames">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="parseMetadata"></a>
# parseMetadata
parseMetadata( String header, java.lang.String[] columns, java.lang.String[] columnLabels ) &rarr; BundleDescriptor

attempt to parse the JSON metadata stored in the header.  The header lines must
 be prefixed with hash (#).  Loosely formatted test is converted into
 nicely-formatted JSON and then parsed with a JSON parser.  Note the Java
 JSON parser itself is pretty loose, for example allowing 1-word strings to
 go without quotes delimiters.  The scheme for this header is either:<ul>
 <li>"rich ascii" or http://autoplot.org/richAscii
 <li>"hapi" https://github.com/hapi-server/data-specification/blob/master/hapi-dev/HAPI-data-access-spec-dev.md#info
 </ul>

### Parameters:
header - the JSON header
<br>columns - identifiers for each column
<br>columnLabels - labels for each column

### Returns:
the BundleDescriptor
### See Also:
<a href='http://autoplot.org/richAscii'>http://autoplot.org/richAscii</a> <br>
<a href='https://github.com/hapi-server/data-specification/blob/master/hapi-dev/HAPI-data-access-spec-dev.md#info'>https://github.com/hapi-server/data-specification/blob/master/hapi-dev/HAPI-data-access-spec-dev.md#info</a> <br>

<a href="https://github.com/autoplot/dev/search?q=parseMetadata&unscoped_q=parseMetadata">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="parseMetadataHapi"></a>
# parseMetadataHapi
parseMetadataHapi( JSONObject doc ) &rarr; BundleDescriptor



### Parameters:
doc - a JSONObject

### Returns:
org.das2.qds.util.AsciiHeadersParser.BundleDescriptor


<a href="https://github.com/autoplot/dev/search?q=parseMetadataHapi&unscoped_q=parseMetadataHapi">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

