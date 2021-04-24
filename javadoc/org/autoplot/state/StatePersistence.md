# org.autoplot.state.StatePersistence

Class for serializing and deserializing application configuration.

***
<a name="currentScheme"></a>
# currentScheme
currentScheme(  ) &rarr; AbstractVapScheme

return the current DOM version, describing the scheme of the DOM.

### Returns:
an org.autoplot.state.AbstractVapScheme


<a href="https://github.com/autoplot/dev/search?q=currentScheme&unscoped_q=currentScheme">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getChildElement"></a>
# getChildElement
getChildElement( org.w3c.dom.Element parent, String tagName ) &rarr; Element

return the first child, if any, with the given tag name.

### Parameters:
parent - the node of the tree.
<br>tagName - the node to look for.

### Returns:
return the child or null if no such child exists.

<a href="https://github.com/autoplot/dev/search?q=getChildElement&unscoped_q=getChildElement">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="restoreState"></a>
# restoreState
restoreState( java.io.File f ) &rarr; Object

restore the XML file, possibly promoting it.

### Parameters:
f - the xml vap file.

### Returns:
the dom object.

<a href="https://github.com/autoplot/dev/search?q=restoreState&unscoped_q=restoreState">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

restoreState( java.io.InputStream in, java.util.LinkedHashMap deltas ) &rarr; Application<br>
restoreState( java.io.InputStream in ) &rarr; Object<br>
***
<a name="saveState"></a>
# saveState
saveState( java.io.File f, Object state ) &rarr; void



### Parameters:
f - a File
<br>state - an Object

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=saveState&unscoped_q=saveState">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

saveState( java.io.File f, Object state, String sscheme ) &rarr; void<br>
saveState( java.io.OutputStream out, Object state, String sscheme ) &rarr; void<br>
***
<a name="writeDocument"></a>
# writeDocument
writeDocument( java.io.OutputStream out, org.w3c.dom.Document document ) &rarr; void

write the document out to the file, hiding the details of the serializer.

### Parameters:
out - outputStream
<br>document - XML document object

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=writeDocument&unscoped_q=writeDocument">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

writeDocument( java.io.File f, org.w3c.dom.Document document ) &rarr; void<br>
