# org.autoplot.datasource.DataSourceRegistry

The DataSourceRegistry keeps the map from extension (like .cdf) to 
 the handler for .cdf files.

***
<a name="getDataSourceEditorByExt"></a>
# getDataSourceEditorByExt
getDataSourceEditorByExt( String ext ) &rarr; Object

returns a String of DataSourceEditor for the extention.  This should be
 used via DataSourceEditorPanelUtil. (This is introduced to remove the
 dependence on the swing library for clients that don't wish to use swing.)

### Parameters:
ext - a String

### Returns:
an Object


<a href="https://github.com/autoplot/dev/search?q=getDataSourceEditorByExt&unscoped_q=getDataSourceEditorByExt">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDataSourceFormatEditorByExt"></a>
# getDataSourceFormatEditorByExt
getDataSourceFormatEditorByExt( String ext ) &rarr; Object



### Parameters:
ext - a String

### Returns:
java.lang.Object


<a href="https://github.com/autoplot/dev/search?q=getDataSourceFormatEditorByExt&unscoped_q=getDataSourceFormatEditorByExt">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDescriptionFor"></a>
# getDescriptionFor
getDescriptionFor( String vapext ) &rarr; String

return a description of the data source, if available.
 TODO: in the export data GUI, there's a bunch of these coded by hand.

### Parameters:
vapext - a String

### Returns:
a String


<a href="https://github.com/autoplot/dev/search?q=getDescriptionFor&unscoped_q=getDescriptionFor">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getFormatByExt"></a>
# getFormatByExt
getFormatByExt( String extension ) &rarr; DataSourceFormat

return the formatter based on the extension.

### Parameters:
extension - the extension, e.g. .cdf

### Returns:
the formatter found for this extension.

<a href="https://github.com/autoplot/dev/search?q=getFormatByExt&unscoped_q=getFormatByExt">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getFormatterExtensions"></a>
# getFormatterExtensions
getFormatterExtensions(  ) &rarr; List

return a list of registered extensions the can format.  These will contain the dot prefix.

### Returns:
a list of registered extensions.

<a href="https://github.com/autoplot/dev/search?q=getFormatterExtensions&unscoped_q=getFormatterExtensions">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getInstance"></a>
# getInstance
getInstance(  ) &rarr; DataSourceRegistry

get the single instance of this class.

### Returns:
the single instance of this class.

<a href="https://github.com/autoplot/dev/search?q=getInstance&unscoped_q=getInstance">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getInstanceFromClassName"></a>
# getInstanceFromClassName
getInstanceFromClassName( String o ) &rarr; Object

get an instance of a class given the class name.

### Parameters:
o - the class name, e.g. org.autoplot.netCDF.HDF5DataSourceFormatEditorPanel

### Returns:
an instance of the class.

<a href="https://github.com/autoplot/dev/search?q=getInstanceFromClassName&unscoped_q=getInstanceFromClassName">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getPlugins"></a>
# getPlugins
getPlugins(  ) &rarr; List



### Returns:
java.util.List


<a href="https://github.com/autoplot/dev/search?q=getPlugins&unscoped_q=getPlugins">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getPluginsText"></a>
# getPluginsText
getPluginsText(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getPluginsText&unscoped_q=getPluginsText">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getSource"></a>
# getSource
getSource( String extension ) &rarr; DataSourceFactory

look up the source by its id.  If a filename is provided, then the
 filename's extension is used, otherwise ".ext" or "ext" are accepted.

### Parameters:
extension - the extension, (e.g. ".cdf" or "/tmp/myfile.cdf")

### Returns:
the DataSourceFactory which will create the reader.

<a href="https://github.com/autoplot/dev/search?q=getSource&unscoped_q=getSource">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getSourceByMime"></a>
# getSourceByMime
getSourceByMime( String mime ) &rarr; DataSourceFactory



### Parameters:
mime - a String

### Returns:
org.autoplot.datasource.DataSourceFactory


<a href="https://github.com/autoplot/dev/search?q=getSourceByMime&unscoped_q=getSourceByMime">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getSourceEditorExtensions"></a>
# getSourceEditorExtensions
getSourceEditorExtensions(  ) &rarr; List

return a list of registered extensions.  These will contain the dot prefix.

### Returns:
a list of registered extensions.

<a href="https://github.com/autoplot/dev/search?q=getSourceEditorExtensions&unscoped_q=getSourceEditorExtensions">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getSourceExtensions"></a>
# getSourceExtensions
getSourceExtensions(  ) &rarr; List

return a list of registered extensions.  These will contain the dot prefix.

### Returns:
a list of registered extensions.

<a href="https://github.com/autoplot/dev/search?q=getSourceExtensions&unscoped_q=getSourceExtensions">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="hasParamOrder"></a>
# hasParamOrder
hasParamOrder( String vapScheme ) &rarr; boolean

returns true if the vap scheme is known to require an order to the 
 parameters.  This was introduced to support makeCanonical, which would
 like to sort the URI parameters so the order does not matter, but then
 you cannot do this operation with vap+inline which is essentially a 
 program where the order matters.

### Parameters:
vapScheme - a String

### Returns:
true if the order of parameters matters.

<a href="https://github.com/autoplot/dev/search?q=hasParamOrder&unscoped_q=hasParamOrder">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="hasResourceUri"></a>
# hasResourceUri
hasResourceUri( String vapScheme ) &rarr; boolean

returns true if the vap scheme requires a resource URL.  For example,
 vap+cdf: needs a resource URI (the file) but vap+inline doesn't.

### Parameters:
vapScheme - the scheme part of the Autoplot URI, or a URI.

### Returns:
true if the vapScheme needs a URL.

<a href="https://github.com/autoplot/dev/search?q=hasResourceUri&unscoped_q=hasResourceUri">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="hasSourceByExt"></a>
# hasSourceByExt
hasSourceByExt( String ext ) &rarr; boolean

return true if the source is registered.

### Parameters:
ext - a String

### Returns:
if the source is registered.

<a href="https://github.com/autoplot/dev/search?q=hasSourceByExt&unscoped_q=hasSourceByExt">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="hasSourceByMime"></a>
# hasSourceByMime
hasSourceByMime( String mime ) &rarr; boolean

return true if the source is registered by mime type.  
 This is not used much.

### Parameters:
mime - a String

### Returns:
true if the source is registered by mime type.

<a href="https://github.com/autoplot/dev/search?q=hasSourceByMime&unscoped_q=hasSourceByMime">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="register"></a>
# register
register( org.autoplot.datasource.DataSourceFactory factory, String extension ) &rarr; void

register the data source factory by extension

### Parameters:
factory - the factory (org.autoplot.foo.FooReaderFactory)
<br>extension - the extension (e.g. ".foo")

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=register&unscoped_q=register">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

register( org.autoplot.datasource.DataSourceFactory factory, String extension, String mime ) &rarr; void<br>
register( String className, String extension, String mime ) &rarr; void<br>
***
<a name="registerDataSourceJar"></a>
# registerDataSourceJar
registerDataSourceJar( String ext, java.net.URL jarFile ) &rarr; void

Register a data source at runtime, allowing the user to 
 override the internal extentions.  This allows, for example, a new version
 of a data source to be compared to the production.

### Parameters:
ext - if non-null, use this extension instead.
<br>jarFile - the jar file, which must contain META-INF/org.autoplot.datasource.DataSourceFactory.extensions.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=registerDataSourceJar&unscoped_q=registerDataSourceJar">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="registerEditor"></a>
# registerEditor
registerEditor( String className, String extension ) &rarr; void

register the data source editor by extension.

### Parameters:
className - the class name of the editor (e.g. "org.autoplot.cdf.CdfDataSourceEditorPanel")
<br>extension - the  extension (e.g. "cdf")

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=registerEditor&unscoped_q=registerEditor">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="registerExtension"></a>
# registerExtension
registerExtension( String className, String extension, String description ) &rarr; void

register the data source factory by extension.  The name of the
 factory class is given, so that the class is not accessed until first
 use.

### Parameters:
className - the class name of the factory. (e.g. "org.autoplot.cdf.CdfJavaDataSourceFactory")
<br>extension - the  extension (e.g. "cdf")
<br>description - a description of the format (e.g. "CDF files using java based reader")

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=registerExtension&unscoped_q=registerExtension">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="registerFormatEditor"></a>
# registerFormatEditor
registerFormatEditor( String className, String extension ) &rarr; void

register the data source format editor by extension.  This implements an
 editor for formatting.

### Parameters:
className - the class name of the editor (e.g. "org.autoplot.cdf.CdfDataSourceFormatEditorPanel")
<br>extension - the  extension (e.g. "cdf")

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=registerFormatEditor&unscoped_q=registerFormatEditor">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="registerFormatter"></a>
# registerFormatter
registerFormatter( String className, String extension ) &rarr; void

register the data source factory by extension.  The name of the
 factory class is given, so that the class is not accessed until first
 use.

### Parameters:
className - the class name of the formatter
<br>extension - the  extension (e.g. "cdf")

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=registerFormatter&unscoped_q=registerFormatter">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="registerMimeType"></a>
# registerMimeType
registerMimeType( String className, String mimeType ) &rarr; void



### Parameters:
className - a String
<br>mimeType - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=registerMimeType&unscoped_q=registerMimeType">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

