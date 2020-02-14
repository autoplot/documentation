= How to Interpret Java Stack Traces in Jython =
The currentLine() function returns the location of its call in a string.  Take the following example:

~~~~~
print 'enter code'
print currentLine()
~~~~~

If this is saved in the file /tmp/currentLineDemo.jy it will print out:
~~~~~
enter code

~~~~~
