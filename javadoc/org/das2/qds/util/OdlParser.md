# org.das2.qds.util.OdlParserTool for parsing ODL found at the top of .sts files.
OdlParser( )


***
<a name="readOdl"></a>
# readOdl
readOdl( java.io.BufferedReader r ) &rarr; String

read the ODL off the top of the file, returning the ODL
 in a string and leaving the InputStream pointed at the 
 line following the ODL.

### Parameters:
r - reader for the file which starts with ODL.  The reader will be left pointing at the first non-ODL line.

### Returns:
the ODL header.

<a href="https://github.com/autoplot/dev/search?q=readOdl&unscoped_q=readOdl">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

