# org.das2.jythoncompletion.nbadapt.Utilities
Utilities( )


***
<a name="getIdentifierBlock"></a>
# getIdentifierBlock
getIdentifierBlock( javax.swing.text.JTextComponent c, int offset ) &rarr; int

Get the identifier around the given position or null if there's no identifier
 around the given position. The identifier is not verified against SyntaxSupport.isIdentifier().

### Parameters:
c - JTextComponent to work on
<br>offset - position in document - usually the caret.getDot()

### Returns:
the block (starting and ending position) enclosing the identifier
 or null if no identifier was found
 
 from NETBEANS/libsrc/org/netbeans/editor/Utilities.java

<a href="https://github.com/autoplot/dev/search?q=getIdentifierBlock&unscoped_q=getIdentifierBlock">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

getIdentifierBlock( org.das2.jythoncompletion.nbadapt.BaseDocument doc, int pos ) &rarr; int<br>
***
<a name="isMac"></a>
# isMac
isMac(  ) &rarr; boolean

from NETBEANS/openide/util/src/org/openide/util/Utilities.java

### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isMac&unscoped_q=isMac">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="openBrowser"></a>
# openBrowser
openBrowser( String url ) &rarr; void

open the URL in a browser.   Borrowed from http://www.centerkey.com/java/browser/.

### Parameters:
url - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=openBrowser&unscoped_q=openBrowser">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

