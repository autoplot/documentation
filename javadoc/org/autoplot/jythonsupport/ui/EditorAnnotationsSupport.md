# org.autoplot.jythonsupport.ui.EditorAnnotationsSupport

annotations support for the editor, marking program counter position 
 and errors.

***
<a name="ANNO_ERROR"></a>
# ANNO_ERROR

error marked in the code

***
<a name="ANNO_PROGRAM_COUNTER"></a>
# ANNO_PROGRAM_COUNTER

current interpreter position

***
<a name="ANNO_WARNING"></a>
# ANNO_WARNING

warning in the code

***
<a name="ANNO_CODE_HINT"></a>
# ANNO_CODE_HINT

warning in the code

***
<a name="ANNO_USAGE"></a>
# ANNO_USAGE

usage of a symbol in the code

***
<a name="annotateChars"></a>
# annotateChars
annotateChars( int line, int i0, int i1, String name, String text, PythonInterpreter interp ) &rarr; void

annotate the characters on the line.  This was introduced to highlite the location of symbol names.

### Parameters:
line - the line number, where 1 is the first line.
<br>i0 - the column number, where 1 is the first column.
<br>i1 - the last column number, exclusive.
<br>name - annotation type, such as "usage" or "error" see constants.
<br>text - the tooltip text.
<br>interp - null or the interpreter.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=annotateChars&unscoped_q=annotateChars">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

annotateChars( int i0, int i1, String name, String text, PythonInterpreter interp ) &rarr; void<br>
***
<a name="annotateError"></a>
# annotateError
annotateError( PyException ex, int offset ) &rarr; void

mark the error in the editor by looking at the python exception to get the line number.

### Parameters:
ex - the python exception
<br>offset - line offset from beginning of file where execution began.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=annotateError&unscoped_q=annotateError">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="annotateLine"></a>
# annotateLine
annotateLine( int line, String name, String text ) &rarr; void

highlite the line by setting the background to color.  null clears the highlite.

### Parameters:
line - the line number to highlite.  1 is the first line.
<br>name - the name of the style, including "error" and "programCounter"
<br>text - annotation to display when hovering. Currently ignored.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=annotateLine&unscoped_q=annotateLine">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

annotateLine( int lline, String name, String ltext, PythonInterpreter interp ) &rarr; void<br>
***
<a name="clearAnnotations"></a>
# clearAnnotations
clearAnnotations(  ) &rarr; void

remove all annotations

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=clearAnnotations&unscoped_q=clearAnnotations">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

clearAnnotations( int pos ) &rarr; void<br>
***
<a name="getExpressionLookup"></a>
# getExpressionLookup
getExpressionLookup(  ) &rarr; ExpressionLookup



### Returns:
org.autoplot.jythonsupport.ui.EditorAnnotationsSupport.ExpressionLookup


<a href="https://github.com/autoplot/dev/search?q=getExpressionLookup&unscoped_q=getExpressionLookup">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getForInterp"></a>
# getForInterp
getForInterp( PythonInterpreter interp ) &rarr; ExpressionLookup



### Parameters:
interp - a PythonInterpreter

### Returns:
org.autoplot.jythonsupport.ui.EditorAnnotationsSupport.ExpressionLookup


<a href="https://github.com/autoplot/dev/search?q=getForInterp&unscoped_q=getForInterp">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getLinePosition"></a>
# getLinePosition
getLinePosition( int line ) &rarr; int

return the position of the line in chars.  The second is exclusive.

### Parameters:
line - the line number 1 is the first line.

### Returns:
[st,en]

<a href="https://github.com/autoplot/dev/search?q=getLinePosition&unscoped_q=getLinePosition">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getPreferredSize"></a>
# getPreferredSize
getPreferredSize(  ) &rarr; Dimension

The editor component should delegate to these.

### Returns:
the preferred size

<a href="https://github.com/autoplot/dev/search?q=getPreferredSize&unscoped_q=getPreferredSize">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getSymbolAt"></a>
# getSymbolAt
getSymbolAt( org.autoplot.jythonsupport.ui.EditorTextPane editor, int position ) &rarr; String

return the symbol (e.g. variable name) at the caret position, or "".

### Parameters:
editor - the code editor
<br>position - typically editor.getCarotPosition

### Returns:
the symbol (e.g. variable name) at the current caret location

<a href="https://github.com/autoplot/dev/search?q=getSymbolAt&unscoped_q=getSymbolAt">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getToolTipText"></a>
# getToolTipText
getToolTipText( java.awt.event.MouseEvent me ) &rarr; String

The editor component should delegate to these.

### Parameters:
me - a MouseEvent

### Returns:
the text

<a href="https://github.com/autoplot/dev/search?q=getToolTipText&unscoped_q=getToolTipText">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="scrollToOffset"></a>
# scrollToOffset
scrollToOffset( int offset ) &rarr; void

scroll to make sure offset is visible.

### Parameters:
offset - an int

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=scrollToOffset&unscoped_q=scrollToOffset">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setExpressionLookup"></a>
# setExpressionLookup
setExpressionLookup( org.autoplot.jythonsupport.ui.EditorAnnotationsSupport.ExpressionLookup l ) &rarr; void



### Parameters:
l - an EditorAnnotationsSupport.ExpressionLookup

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setExpressionLookup&unscoped_q=setExpressionLookup">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

