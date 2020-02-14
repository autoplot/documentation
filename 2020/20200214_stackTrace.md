# How to Interpret Java Stack Traces in Jython 
The currentLine() function returns the location of its call in a string.  Take the following example:

~~~~~
print 'enter code'
print currentLine()
~~~~~

If this is saved in the file /tmp/currentLineDemo.jy it will print out:
~~~~~
enter code
file:///tmp/currentLineDemo.jy:2
~~~~~

Sometimes the Jython code developer will need to interpret Java stack traces, and this document shows how this is done.

## Jython code locations are kept in stack traces
The Jython creators conveniently store the Jython code location within a Java stack trace.  Instead of using currentLine(), let's do this manually, saving the following as /tmp/currentLineDemo2.jy and running it:

~~~~~
print 'enter code'
from java.lang import Exception
Exception('xxx').printStackTrace()
~~~~~

Run this and you will see the output:
~~~~~
enter code
java.lang.Exception: xxx
	at sun.reflect.NativeConstructorAccessorImpl.newInstance0(Native Method)
	at sun.reflect.NativeConstructorAccessorImpl.newInstance(NativeConstructorAccessorImpl.java:62)
	at sun.reflect.DelegatingConstructorAccessorImpl.newInstance(DelegatingConstructorAccessorImpl.java:45)
	at java.lang.reflect.Constructor.newInstance(Constructor.java:423)
	at org.python.core.PyReflectedConstructor.__call__(PyReflectedConstructor.java:183)
	at org.python.core.PyJavaInstance.__init__(PyJavaInstance.java:73)
	at org.python.core.PyJavaClass.__call__(PyJavaClass.java:883)
	at org.python.core.PyObject.__call__(PyObject.java:482)
	at org.python.pycode._pyx30.f$0(currentLineDemo2.jy:3)
	at org.python.pycode._pyx30.call_function(currentLineDemo2.jy)
	at org.python.core.PyTableCode.call(PyTableCode.java:217)
	at org.python.core.PyCode.call(PyCode.java:14)
	at org.python.core.Py.runCode(Py.java:1224)
	at org.python.util.PythonInterpreter.execfile(PythonInterpreter.java:165)
	at org.autoplot.scriptconsole.ScriptPanelSupport$9.run(ScriptPanelSupport.java:925)
	at java.lang.Thread.run(Thread.java:748)

~~~~~

The exception is created deep within Java, and you need to walk up the stack to see what Jython code was used.  The top line is the deepest call, where the Exception is created.  If you scan down the list, you will see around the middle "org.python.pycode" and in parenthesis (currentLineDemo2.jy:3).  This is what the currentLine() function does.

## Catching exceptions
You may need to handle cases where a process usually works, but when it doesn't you need to take special action.  This is done using a try/except loop like so:

~~~~~
try:
  fil=downloadResourceAsTempFile(URL('http://autoplot.org/data/nofile.dat'),monitor)
except:
  import traceback
  traceback.print_exc()
~~~~~

Another method for doing this is:

~~~~~
import java.io.IOException
try:
  fil=downloadResourceAsTempFile(URL('http://autoplot.org/data/nofile.dat'),monitor)
except java.io.IOException,ex:
  print 'file not found'
  print ex.printStackTrace()
~~~~~
Either method may work for you.
