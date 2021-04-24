# org.autoplot.datasource.CompletionContext

models a part of a dataset's URI.  This class is used to serve as both the
 input and output of completion engines.  An incomplete completion context is
 passed in, and the engine returns a set of more complete contexts.  This 
 process could be repeated to define a tree, where the leaf nodes are valid 
 datasets urls.

# CompletionContext( )
create an empty completion proposal.

# CompletionContext( Object context, String completable )
Object containing a completion proposal.

# CompletionContext( Object context, String completable, org.autoplot.datasource.DataSourceFactory owner, String implicitName, String label, String doc )
Object containing a completion proposal.

# CompletionContext( Object context, String completable, org.autoplot.datasource.DataSourceFactory owner, String implicitName )
Object containing a completion proposal.

# CompletionContext( Object context, String completable, String doc )
Object containing a completion proposal.

# CompletionContext( Object context, String completable, String label, String doc )
Object containing a completion proposal.

# CompletionContext( Object context, String completable, org.autoplot.datasource.DataSourceFactory owner, String implicitName, String doc )
Object containing a completion proposal.

# CompletionContext( Object context, String completable, org.autoplot.datasource.DataSourceFactory owner, String implicitName, String label, String doc, boolean maybePlot )
Object containing a completion proposal.

***
<a name="CONTEXT_AUTOPLOT_SCHEME"></a>
# CONTEXT_AUTOPLOT_SCHEME



***
<a name="CONTEXT_FILESYSTEM"></a>
# CONTEXT_FILESYSTEM

file resource, which is a URL and doesn't include AP Scheme.

***
<a name="CONTEXT_FILE"></a>
# CONTEXT_FILE

file resource, which is a URL and doesn't include AP Scheme.

***
<a name="CONTEXT_PARAMETER_NAME"></a>
# CONTEXT_PARAMETER_NAME



***
<a name="CONTEXT_PARAMETER_VALUE"></a>
# CONTEXT_PARAMETER_VALUE



***
<a name="surl"></a>
# surl

the url in its incomplete state

***
<a name="surlpos"></a>
# surlpos

the position of the carot within the url

***
<a name="resourceURI"></a>
# resourceURI

resource file URI, no params (and no "vap:" schema), starting with http, sftp, etc.

***
<a name="params"></a>
# params

params parsed

***
<a name="context"></a>
# context

the context identifier enum for the completion. See CONTEXT_FILESYSTEM, CONTEXT_FILE, CONTEXT_PARAMETER_NAME, CONTEXT_PARAMETER_VALUE, etc.

***
<a name="completable"></a>
# completable

The string to be completed

***
<a name="completablepos"></a>
# completablepos

the position of the carot within the string

***
<a name="implicitName"></a>
# implicitName

used to identify the group the parameter implicitly specifies.  For example,
 in ftp://cdaweb.gsfc.nasa.gov/pub/istp/noaa/noaa14/%Y/noaa14_meped1min_sem_%Y%m%d_v01.cdf?T01_gsmB&timerange=2000-01-01
 T01_gsmB is part of the implicit group "id" of the cdf data source factory.

***
<a name="doc"></a>
# doc

one-line documentation

***
<a name="label"></a>
# label

label identifying the proposal, to be understood within the context of 
 surl and the insertion point.

***
<a name="maybePlot"></a>
# maybePlot

hint that this completion should finish a valid URL, so go ahead and try to use it.

***
<a name="get"></a>
# get
get( Object context, org.autoplot.datasource.CompletionContext cc ) &rarr; String

returns the value for the context
 <pre>
 
 cc= new CompletionContext();
 cc.surl= vap:http://www.autoplot.org/data/myfile.dat?param1=aaa&param2=bbb
 cc.completable= b
 cc.surlpos= 63
 get( CONTEXT_PARAMETER_NAME, cc ) ->  param2
 get( CONTEXT_FILE, cc ) ->  http://www.autoplot.org/data/myfile.dat
 
 </pre>

### Parameters:
context - an Object
<br>cc - a CompletionContext

### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=get&unscoped_q=get">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="insert"></a>
# insert
insert( org.autoplot.datasource.CompletionContext cc, org.autoplot.datasource.CompletionContext ccnew ) &rarr; String

"ftp://cdaweb.gsfc.nasa.gov/pub/istp/noaa/noaa14/%Y/noaa14_meped1min_sem_%Y%m%d_v01.cdf?timerange=2000-01-01"
 "ftp://cdaweb.gsfc.nasa.gov/pub/istp/noaa/noaa14/%Y/noaa14_meped1min_sem_%Y%m%d_v01.cdf?Epoch&timerange=2000-01-01"

### Parameters:
cc - a CompletionContext
<br>ccnew - a CompletionContext

### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=insert&unscoped_q=insert">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="toString"></a>
# toString
toString(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=toString&unscoped_q=toString">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

