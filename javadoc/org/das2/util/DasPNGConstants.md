# org.das2.util.DasPNGConstants
***
<a name="DEFAULT_GAMMA"></a>
# DEFAULT_GAMMA



***
<a name="KEYWORD_TITLE"></a>
# KEYWORD_TITLE



***
<a name="KEYWORD_AUTHOR"></a>
# KEYWORD_AUTHOR



***
<a name="KEYWORD_DESCRIPTION"></a>
# KEYWORD_DESCRIPTION



***
<a name="KEYWORD_COPYRIGHT"></a>
# KEYWORD_COPYRIGHT



***
<a name="KEYWORD_CREATION_TIME"></a>
# KEYWORD_CREATION_TIME



***
<a name="KEYWORD_SOFTWARE"></a>
# KEYWORD_SOFTWARE



***
<a name="KEYWORD_DISCLAIMER"></a>
# KEYWORD_DISCLAIMER



***
<a name="KEYWORD_WARNING"></a>
# KEYWORD_WARNING



***
<a name="KEYWORD_SOURCE"></a>
# KEYWORD_SOURCE



***
<a name="KEYWORD_COMMENT"></a>
# KEYWORD_COMMENT



***
<a name="KEYWORD_PLOT_INFO"></a>
# KEYWORD_PLOT_INFO

dasCanvas has a method for generating a JSON string describing the plots,
 and this is the tag that data should be inserted with.

***
<a name="getGamma"></a>
# getGamma
getGamma(  ) &rarr; int



### Returns:
int


<a href="https://github.com/autoplot/dev/search?q=getGamma&unscoped_q=getGamma">[search for examples]</a>

***
<a name="getText"></a>
# getText
getText( String keyword ) &rarr; List

Returns an unmodifiable java.util.List containing the contents of
 all of the tEXT chunks with the specified keyword.  The return value
 is guaranteed to be non-null.  If no tEXT chunks with the specified
 keyword exist, then an empty list is returned.

### Parameters:
keyword - the specified keyword

### Returns:
a java.util.List of the contents of tEXT chunks.

<a href="https://github.com/autoplot/dev/search?q=getText&unscoped_q=getText">[search for examples]</a>

