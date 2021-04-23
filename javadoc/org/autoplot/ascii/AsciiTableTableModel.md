# org.autoplot.ascii.AsciiTableTableModel

You will need to:
 <tt>
 model.setParser(parser);
 this.jTable1.setModel(model);
 model.setFile(file);
 jTable1.setDefaultRenderer(Object.class, new ColSpanTableCellRenderer());
 AsciiParser.DelimParser p;
 try {
    p = parser.setDelimParser(f, AsciiParser.DELIM_COMMA);
    model.setRecParser(p);
 }
 </tt>

# AsciiTableTableModel( )


***
<a name="PROP_FILE"></a>
# PROP_FILE



***
<a name="PROP_RECPARSER"></a>
# PROP_RECPARSER



***
<a name="PROP_PARSER"></a>
# PROP_PARSER



***
<a name="addPropertyChangeListener"></a>
# addPropertyChangeListener
addPropertyChangeListener( java.beans.PropertyChangeListener listener ) &rarr; void



### Parameters:
listener - a PropertyChangeListener

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=addPropertyChangeListener&unscoped_q=addPropertyChangeListener">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getColumnCount"></a>
# getColumnCount
getColumnCount(  ) &rarr; int



### Returns:
int


<a href="https://github.com/autoplot/dev/search?q=getColumnCount&unscoped_q=getColumnCount">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getFile"></a>
# getFile
getFile(  ) &rarr; File



### Returns:
java.io.File


<a href="https://github.com/autoplot/dev/search?q=getFile&unscoped_q=getFile">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getLine"></a>
# getLine
getLine( int skip ) &rarr; String



### Parameters:
skip - an int

### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getLine&unscoped_q=getLine">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getParser"></a>
# getParser
getParser(  ) &rarr; AsciiParser



### Returns:
org.das2.qds.util.AsciiParser


<a href="https://github.com/autoplot/dev/search?q=getParser&unscoped_q=getParser">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getRecParser"></a>
# getRecParser
getRecParser(  ) &rarr; RecordParser



### Returns:
org.das2.qds.util.AsciiParser.RecordParser


<a href="https://github.com/autoplot/dev/search?q=getRecParser&unscoped_q=getRecParser">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getRowCount"></a>
# getRowCount
getRowCount(  ) &rarr; int



### Returns:
int


<a href="https://github.com/autoplot/dev/search?q=getRowCount&unscoped_q=getRowCount">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getValueAt"></a>
# getValueAt
getValueAt( int row, int column ) &rarr; Object



### Parameters:
row - an int
<br>column - an int

### Returns:
java.lang.Object


<a href="https://github.com/autoplot/dev/search?q=getValueAt&unscoped_q=getValueAt">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isColSpan"></a>
# isColSpan
isColSpan( int row, int column ) &rarr; boolean



### Parameters:
row - an int
<br>column - an int

### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isColSpan&unscoped_q=isColSpan">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isRecord"></a>
# isRecord
isRecord( int row ) &rarr; boolean

returns true if the row is believed to be a record.  If it is not,
 then the entire line is returned for each column, and the
 ColSpanTableCellRenderer should be used.

### Parameters:
row - an int

### Returns:
a boolean


<a href="https://github.com/autoplot/dev/search?q=isRecord&unscoped_q=isRecord">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="removePropertyChangeListener"></a>
# removePropertyChangeListener
removePropertyChangeListener( java.beans.PropertyChangeListener listener ) &rarr; void



### Parameters:
listener - a PropertyChangeListener

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=removePropertyChangeListener&unscoped_q=removePropertyChangeListener">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setFile"></a>
# setFile
setFile( java.io.File file ) &rarr; void



### Parameters:
file - a File

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setFile&unscoped_q=setFile">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setParser"></a>
# setParser
setParser( org.das2.qds.util.AsciiParser parser ) &rarr; void



### Parameters:
parser - an AsciiParser

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setParser&unscoped_q=setParser">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setRecParser"></a>
# setRecParser
setRecParser( org.das2.qds.util.AsciiParser.RecordParser recParser ) &rarr; void



### Parameters:
recParser - an AsciiParser.RecordParser

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setRecParser&unscoped_q=setRecParser">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

