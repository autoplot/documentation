# org.autoplot.JythonUtil

Utilities for Jython functions, such as a standard way to initialize
 an interpreter and invoke a script asynchronously.  See also 1310.
 TODO: this needs review, since the autoplot.py was added to the imports.

# JythonUtil( )


***
<a name="createInterpreter"></a>
# createInterpreter
createInterpreter( boolean appContext, boolean sandbox ) &rarr; InteractiveInterpreter

create an interpreter object configured for Autoplot contexts:
 <ul>
   <li> QDataSets are wrapped so that operators are overloaded.
   <li> a standard set of names are imported.
 </ul>

### Parameters:
appContext - load in additional symbols that make sense in application context.
<br>sandbox - limit symbols to safe symbols for server.

### Returns:
PythonInterpreter ready for commands.

<a href="https://github.com/autoplot/dev/search?q=createInterpreter&unscoped_q=createInterpreter">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

createInterpreter( boolean appContext, boolean sandbox, org.autoplot.dom.Application dom, ProgressMonitor mon ) &rarr; InteractiveInterpreter<br>
***
<a name="invokeScript20181217"></a>
# invokeScript20181217
invokeScript20181217( java.net.URI uri, java.io.File file, org.autoplot.dom.Application dom, java.util.Map fparams, ProgressMonitor mon ) &rarr; void

Invoke the script on the current thread.

### Parameters:
uri - the URI, providing pwd.
<br>file - null or the file to use.
<br>dom - the application
<br>fparams - parameters to pass into the script.
<br>mon - feedback monitor for the thread.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=invokeScript20181217&unscoped_q=invokeScript20181217">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="invokeScriptNow"></a>
# invokeScriptNow
invokeScriptNow( java.util.Map environ, java.io.File file ) &rarr; void

Do a search for the number of places where JythonUtil.createInterpreter
 is called and it should be clear that there's a need for one code that
 does this.  There probably is one such code, but I can't find it right 
 now.

### Parameters:
environ - a java.util.Map
<br>file - a File

### Returns:
void (returns nothing)

### See Also:
<a href='#runScript'>runScript(org.autoplot.ApplicationModel, java.lang.String, java.lang.String[], java.lang.String)</a> which doesn't allow for control of the environ (and arbitrary parameters).<br>

<a href="https://github.com/autoplot/dev/search?q=invokeScriptNow&unscoped_q=invokeScriptNow">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="invokeScriptSoon"></a>
# <del>invokeScriptSoon</del>
Deprecated: use invokeScriptSoon with URI.
invokeScriptSoon( java.net.URI uri ) &rarr; void<br>
invokeScriptSoon( java.net.URL url, org.autoplot.dom.Application dom, ProgressMonitor mon ) &rarr; void<br>
invokeScriptSoon( java.net.URI uri, org.autoplot.dom.Application dom, ProgressMonitor mon ) &rarr; void<br>
invokeScriptSoon( java.net.URL url, org.autoplot.dom.Application dom, java.util.Map params, boolean askParams, boolean makeTool, ProgressMonitor mon1 ) &rarr; int<br>
invokeScriptSoon( java.net.URI uri, org.autoplot.dom.Application dom, java.util.Map vars, boolean askParams, boolean makeTool, ProgressMonitor mon1 ) &rarr; int<br>
invokeScriptSoon( java.net.URL url, org.autoplot.dom.Application dom, java.util.Map params, boolean askParams, boolean makeTool, org.autoplot.scriptconsole.JythonScriptPanel scriptPanel, ProgressMonitor mon1 ) &rarr; int<br>
invokeScriptSoon( java.net.URI uri, org.autoplot.dom.Application dom, java.util.Map params, boolean askParams, boolean makeTool, org.autoplot.scriptconsole.JythonScriptPanel scriptPanel, ProgressMonitor mon1 ) &rarr; int<br>
invokeScriptSoon( java.net.URI uri, java.io.File file, org.autoplot.dom.Application dom, java.util.Map params, boolean askParams, boolean makeTool, org.autoplot.scriptconsole.JythonScriptPanel scriptPanel, ProgressMonitor mon1 ) &rarr; int<br>
***
<a name="runScript"></a>
# runScript
runScript( org.autoplot.dom.Application dom, java.io.InputStream in, String name, java.lang.String[] argv, String pwd ) &rarr; void

Run the script in the input stream.

### Parameters:
dom - provides the dom to the environment.
<br>in - stream containing script. This will be left open.
<br>name - the name of the file for human reference, or null.
<br>argv - parameters passed into the script, each should be name=value, or positional.  The name of the script should not be the zeroth element.
<br>pwd - the present working directory, if available.  Note this is a String because pwd can be a remote folder.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=runScript&unscoped_q=runScript">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="showScriptDialog"></a>
# showScriptDialog
showScriptDialog( java.awt.Component parent, java.util.Map env, java.io.File file, java.util.Map fparams, boolean makeTool, java.net.URI resourceUri ) &rarr; int

show the script and the variables (like we have always done with jyds scripts), and offer to run the script.

### Parameters:
parent - parent GUI to follow
<br>env - a java.util.Map
<br>file - file containing the script.
<br>fparams - parameters for the script.
<br>makeTool - the dialog is always shown and the user can have the script installed as a tool.
<br>resourceUri - when the user decides to make a tool, we need the source location.

### Returns:
JOptionPane.OK_OPTION or JOptionPane.CANCEL_OPTION if the user cancels.

<a href="https://github.com/autoplot/dev/search?q=showScriptDialog&unscoped_q=showScriptDialog">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

