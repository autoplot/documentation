# org.autoplot.jythonsupport.StaticCodeAnalysis



# StaticCodeAnalysis( )


***
<a name="showReadButNotAssigned"></a>
# showReadButNotAssigned
showReadButNotAssigned( String script, boolean appContext, String pwd ) &rarr; List

return any node where a name is read but has not been assigned.  This is an
 error which would show when the code is run.

### Parameters:
script - the script code (not the filename).
<br>appContext - true if application codes are loaded
<br>pwd - null or the value of the working directory.

### Returns:
a java.util.List


<a href="https://github.com/autoplot/dev/search?q=showReadButNotAssigned&unscoped_q=showReadButNotAssigned">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="showUsage"></a>
# showUsage
showUsage( String script, String symbol ) &rarr; List

get the nodes where the symbol is used.

### Parameters:
script - the jython script which is parsed.
<br>symbol - the symbol to look for.

### Returns:
the AST nodes which contain location information.

<a href="https://github.com/autoplot/dev/search?q=showUsage&unscoped_q=showUsage">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="showWriteWithoutRead"></a>
# showWriteWithoutRead
showWriteWithoutRead( String script ) &rarr; List

return any node where a variable is assigned but then not later read.  This is 
 not an error, but is a nice way to flag suspicious code.

### Parameters:
script - the script code (not the filename).

### Returns:
a java.util.List


<a href="https://github.com/autoplot/dev/search?q=showWriteWithoutRead&unscoped_q=showWriteWithoutRead">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

