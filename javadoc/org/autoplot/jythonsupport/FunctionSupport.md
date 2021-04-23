# org.autoplot.jythonsupport.FunctionSupport

Code to support writing Python Functions.

# FunctionSupport( String name, java.lang.String[] parameters )


# FunctionSupport( String name, java.lang.String[] parameters, PyObject[] defaults )


# FunctionSupport( String name, java.lang.String[] parameters, PyObject[] defaults, String extraPositionalParameters, String extraKeywordParameters )


***
<a name="args"></a>
# args
args( PyObject[] args, java.lang.String[] keywords ) &rarr; Map

Processes the arguments for a jython method invocation in a way that
 mimics the way arguments are process for native python defined method.
 This algorithm is based on the description of the process given in
 section 5.3.4 of the version 2.4.4 Python Reference Manual.

 http://www.python.org/doc/2.4.4/ref/calls.html

### Parameters:
args - a PyObject[]
<br>keywords - a java.lang.String[]

### Returns:
a java.util.Map


<a href="https://github.com/autoplot/dev/search?q=args&unscoped_q=args">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

