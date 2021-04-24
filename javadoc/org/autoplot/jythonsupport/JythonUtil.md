# org.autoplot.jythonsupport.JythonUtil

Utilities to support Jython scripting.

# JythonUtil( )


***
<a name="EMPTY"></a>
# EMPTY



***
<a name="createInterpreter"></a>
# createInterpreter
createInterpreter( boolean sandbox ) &rarr; InteractiveInterpreter

create an interpreter object configured for Autoplot contexts:
 <ul>
 <li> QDataSets are wrapped so that operators are overloaded.
 <li> a standard set of names are imported.
 </ul>
 This also adds things to the Jython search path (see
 getLocalJythonAutoplotLib) so imports will find them.

### Parameters:
sandbox - limit symbols to safe symbols for server.

### Returns:
PythonInterpreter ready for commands.

<a href="https://github.com/autoplot/dev/search?q=createInterpreter&unscoped_q=createInterpreter">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="describeScript"></a>
# describeScript
describeScript( String script, java.util.Map params ) &rarr; ScriptDescriptor

return the script description and arguments.

### Parameters:
script - the script Jython code.
<br>params - any operator-defined values.

### Returns:
an org.autoplot.jythonsupport.JythonUtil.ScriptDescriptor


<a href="https://github.com/autoplot/dev/search?q=describeScript&unscoped_q=describeScript">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

describeScript( java.util.Map env, String script, java.util.Map params ) &rarr; ScriptDescriptor<br>
***
<a name="errorScriptDescriptor"></a>
# errorScriptDescriptor
errorScriptDescriptor( PySyntaxError ex ) &rarr; ScriptDescriptor



### Parameters:
ex - a PySyntaxError

### Returns:
org.autoplot.jythonsupport.JythonUtil.ScriptDescriptor


<a href="https://github.com/autoplot/dev/search?q=errorScriptDescriptor&unscoped_q=errorScriptDescriptor">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDocumentation"></a>
# getDocumentation
getDocumentation( java.io.BufferedReader reader ) &rarr; Map

scrape through the script looking for documentation declarations returns
 an map, possibly containing:<ul>
 <li>LABEL few words
 <li>TITLE sentence
 <li>DESCRIPTION short paragraph
 </ul>
 This would originally look for lines like:<br>
 # TITLE: Text Recombinator<br>
 but this has been deprecated and scripts should use setScriptTitle 
 and setScriptDescription

### Parameters:
reader - a BufferedReader

### Returns:
the documentation found.
### See Also:
<a href='#getDocumentation'>getDocumentation(java.io.BufferedReader, java.net.URI)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=getDocumentation&unscoped_q=getDocumentation">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

getDocumentation( java.io.BufferedReader reader, java.net.URI resourceURI ) &rarr; Map<br>
***
<a name="getGetDataSet"></a>
# getGetDataSet
getGetDataSet( java.util.Map env, String script, java.util.Map params ) &rarr; Map

return a list of the getDataSet calls, from index to simplified
 getDataSet call. Experimental--interface may change

### Parameters:
env - a java.util.Map
<br>script - a String
<br>params - a java.util.Map

### Returns:
a java.util.Map


<a href="https://github.com/autoplot/dev/search?q=getGetDataSet&unscoped_q=getGetDataSet">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getGetParams"></a>
# getGetParams
getGetParams( java.io.Reader reader ) &rarr; List

support for the old getGetParams. Note this closes the reader.

### Parameters:
reader - a Reader

### Returns:
a java.util.List


<a href="https://github.com/autoplot/dev/search?q=getGetParams&unscoped_q=getGetParams">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

getGetParams( String script ) &rarr; List<br>
getGetParams( String script, java.util.Map params ) &rarr; List<br>
getGetParams( java.util.Map env, String script, java.util.Map params ) &rarr; List<br>
***
<a name="getLocals"></a>
# getLocals
getLocals( java.io.BufferedReader reader ) &rarr; Map

scrape script for local variables, looking for assignments. The reader is
 closed after reading.

### Parameters:
reader - the source for the script. It is closed when the code
 executes properly.

### Returns:
a map of the local variable name to the line containing it.

<a href="https://github.com/autoplot/dev/search?q=getLocals&unscoped_q=getLocals">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="join"></a>
# join
join( java.lang.String[] list, String delim ) &rarr; String

join the array using the delimiter join( ['a','b'], '_' ) -> a_b Note
 Java 8 finally has a join, and this should be used when Java 8 is
 available.

### Parameters:
list - strings to join
<br>delim - a String

### Returns:
the joined string

<a href="https://github.com/autoplot/dev/search?q=join&unscoped_q=join">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

join( java.util.List list, String delim ) &rarr; String<br>
***
<a name="maybeQuoteString"></a>
# maybeQuoteString
maybeQuoteString( String sval ) &rarr; String

put quotes around values that appear to be strings. We see if it's
 parsable as a double or the keyword True or False.

### Parameters:
sval - the string, for example "2015" "'2015'" or "2015-01-01"

### Returns:
2015, "'2015'", "'2015-01-01'"

<a href="https://github.com/autoplot/dev/search?q=maybeQuoteString&unscoped_q=maybeQuoteString">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="maybeUnquoteString"></a>
# maybeUnquoteString
maybeUnquoteString( String sval ) &rarr; String

pop off the quotes to get the text inside.

### Parameters:
sval - "'2015-01-01'"

### Returns:
"2015-01-01"

<a href="https://github.com/autoplot/dev/search?q=maybeUnquoteString&unscoped_q=maybeUnquoteString">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="pyDictionaryToMap"></a>
# pyDictionaryToMap
pyDictionaryToMap( PyDictionary pd ) &rarr; Map

return a Java Map for a Jython dictionary.

### Parameters:
pd - a PyDictionary

### Returns:
a java.util.Map


<a href="https://github.com/autoplot/dev/search?q=pyDictionaryToMap&unscoped_q=pyDictionaryToMap">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="pythonLint"></a>
# pythonLint
pythonLint( java.net.URI uri, java.util.List errs ) &rarr; boolean

check the script that it doesn't redefine symbol names like "str"

### Parameters:
uri - an URI
<br>errs - an empty list where the errors can be logged.

### Returns:
true if an err is suspected.

<a href="https://github.com/autoplot/dev/search?q=pythonLint&unscoped_q=pythonLint">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

pythonLint( java.io.LineNumberReader reader, java.util.List errs ) &rarr; boolean<br>
***
<a name="readScript"></a>
# readScript
readScript( java.io.Reader reader ) &rarr; String

read all the lines of a script into a string. The reader will be closed.

### Parameters:
reader - a Reader

### Returns:
a String


<a href="https://github.com/autoplot/dev/search?q=readScript&unscoped_q=readScript">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="removeSideEffects"></a>
# <del>removeSideEffects</del>
Deprecated: this should not be used, because newer codes use the
 fully-implemented Jython parser.
***
<a name="setParams"></a>
# setParams
setParams( PythonInterpreter interp, java.util.Map paramsl ) &rarr; void

put each parameter into the dictionary autoplot.params.

### Parameters:
interp - a PythonInterpreter
<br>paramsl - a java.util.Map

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setParams&unscoped_q=setParams">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setupInterp"></a>
# setupInterp
setupInterp( PythonInterpreter interp, String pwd, String resourceUri, java.util.Map paramsl, ProgressMonitor mon ) &rarr; void

set up the interp variables scripts will often use, such as PWD and
 monitor.

### Parameters:
interp - a PythonInterpreter
<br>pwd - a String
<br>resourceUri - a String
<br>paramsl - a java.util.Map
<br>mon - a ProgressMonitor

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setupInterp&unscoped_q=setupInterp">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="simplifyScriptToGetParams"></a>
# simplifyScriptToGetParams
simplifyScriptToGetParams( java.lang.String[] ss, stmtType[] stmts, java.util.HashSet variableNames, int beginLine, int lastLine, int depth ) &rarr; String

Extracts the parts of the program that get parameters or take a trivial
 amount of time to execute.  This may call itself recursively when if
 blocks are encountered. 
 
 This scans through, where acceptLine is the first line we'll accept
 to the currentLine, copying over script from acceptLine to currentLine.
 
 See test038 (https://jfaden.net/jenkins/job/autoplot-test038/)

### Parameters:
ss - the entire script, ss[0] is empty string so that ss[1] is the first line of the script.
<br>stmts - statements being processed.
<br>variableNames - variable names that have been resolved.
<br>beginLine - first line of the script being processed.
<br>lastLine - INCLUSIVE last line of the script being processed.
<br>depth - recursion depth, for debugging.

### Returns:
a String

### See Also:
<a href='SimplifyScriptSupport.md#simplifyScriptToGetCompletions'>SimplifyScriptSupport#simplifyScriptToGetCompletions(java.lang.String[], org.python.parser.ast.stmtType[], java.util.HashSet, int, int, int)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=simplifyScriptToGetParams&unscoped_q=simplifyScriptToGetParams">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

simplifyScriptToGetParams( String script, boolean addSort ) &rarr; String<br>
***
<a name="splitCodeIntoLines"></a>
# splitCodeIntoLines
splitCodeIntoLines( String zerothLine, String script ) &rarr; String

one-stop place for splitting a script into lines for simplifyScriptToGetParams
 This was all motivated by a busy number of lineNumber-1's in the code
 that would handle the refactorings.

### Parameters:
zerothLine - null or the line to use for the first element in the array.
<br>script - the script

### Returns:
the script with the first line of the script in array[1].
### See Also:
<a href='#simplifyScriptToGetParams'>simplifyScriptToGetParams(java.lang.String[], org.python.parser.ast.stmtType[], java.util.HashSet, int, int, int)</a> <br>
<a href='SimplifyScriptSupport.md#simplifyScriptToGetCompletions'>SimplifyScriptSupport#simplifyScriptToGetCompletions(java.lang.String[], org.python.parser.ast.stmtType[], java.util.HashSet, int, int, int)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=splitCodeIntoLines&unscoped_q=splitCodeIntoLines">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

