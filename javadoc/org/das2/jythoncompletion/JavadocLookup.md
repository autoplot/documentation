# org.das2.jythoncompletion.JavadocLookupProvide a class for keeping track of the Javadoc lookups, 
 so this is not buried in code (so much).
JavadocLookup( )


***
<a name="getInstance"></a>
# getInstance
getInstance(  ) &rarr; JavadocLookup

get the one instance

### Returns:
the instance

<a href="https://github.com/autoplot/dev/search?q=getInstance&unscoped_q=getInstance">[search for examples]</a>

***
<a name="getLinkForJavaSignature"></a>
# getLinkForJavaSignature
getLinkForJavaSignature( String signature ) &rarr; String

return a link to the documentation for a java signature.  For standard library
 things, this goes to Oracle's website.  For other things, this goes
 to the Autoplot/Das2 javadocs.
 Java8 http://docs.oracle.com/javase/8/docs/api/java/io/File.html#createTempFile-java.lang.String-java.lang.String-java.io.File-

### Parameters:
signature - signature like javax.swing.JCheckBox#paramString()

### Returns:
null or the link, like http://docs.oracle.com/javase/6/docs/api/javax/swing/JCheckBox#paramString()
 TODO: it appears that this needs /x/y/z.html!

<a href="https://github.com/autoplot/dev/search?q=getLinkForJavaSignature&unscoped_q=getLinkForJavaSignature">[search for examples]</a>

***
<a name="searchForSignature"></a>
# searchForSignature
searchForSignature( String clas ) &rarr; List

given a class name, what are fully-qualified class names which match?

### Parameters:
clas - a String

### Returns:
a java.util.List


<a href="https://github.com/autoplot/dev/search?q=searchForSignature&unscoped_q=searchForSignature">[search for examples]</a>

***
<a name="setLinkForJavaSignature"></a>
# setLinkForJavaSignature
setLinkForJavaSignature( String signatureStart, String link ) &rarr; void

add the location of the javadocs for the given path.  The path should
 be / separated, not period separated.

### Parameters:
signatureStart - e.g. "gov/nasa/gsfc/spdf/cdfj"
<br>link - e.g. "https://cdaweb.sci.gsfc.nasa.gov/~nand/cdfj/docs/"

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setLinkForJavaSignature&unscoped_q=setLinkForJavaSignature">[search for examples]</a>

