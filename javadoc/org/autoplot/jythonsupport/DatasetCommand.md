# org.autoplot.jythonsupport.DatasetCommand

new implementation of the dataset command allows for keywords in the
 Jython environment.
<blockquote><pre><small>{@code
 dataset( [1,2,3,4,3], title='My Data' )
}</small></pre></blockquote>

# DatasetCommand( )


***
<a name="__doc__"></a>
# __doc__



***
<a name="__call__"></a>
# __call__
__call__( PyObject[] args, java.lang.String[] keywords ) &rarr; PyObject

implement the python call.

### Parameters:
args - the "rightmost" elements are the keyword values.
<br>keywords - the names for the keywords.

### Returns:
Py.None

<a href="https://github.com/autoplot/dev/search?q=__call__&unscoped_q=__call__">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

