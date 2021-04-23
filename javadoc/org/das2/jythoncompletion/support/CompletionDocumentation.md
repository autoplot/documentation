# org.das2.jythoncompletion.support.CompletionDocumentation

The interface of an item that can be displayed in the documentation popup.

***
<a name="getGotoSourceAction"></a>
# getGotoSourceAction
getGotoSourceAction(  ) &rarr; Action

Returns an action that opens the item's source representation in the editor
 or <code>null</code> if the item has no source representation.

### Returns:
javax.swing.Action


<a href="https://github.com/autoplot/dev/search?q=getGotoSourceAction&unscoped_q=getGotoSourceAction">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getText"></a>
# getText
getText(  ) &rarr; String

Returns a HTML text dispaleyd in the documentation popup.

### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getText&unscoped_q=getText">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getURL"></a>
# getURL
getURL(  ) &rarr; URL

Returns a URL of the item's external representation that can be displayed
 in an external browser or <code>null</code> if the item has no external
 representation.

### Returns:
java.net.URL


<a href="https://github.com/autoplot/dev/search?q=getURL&unscoped_q=getURL">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="resolveLink"></a>
# resolveLink
resolveLink( String link ) &rarr; CompletionDocumentation

Returns a documentation item representing an object linked from the item's 
 HTML text.

### Parameters:
link - a String

### Returns:
org.das2.jythoncompletion.support.CompletionDocumentation


<a href="https://github.com/autoplot/dev/search?q=resolveLink&unscoped_q=resolveLink">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

