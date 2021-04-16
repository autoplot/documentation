# org.autoplot.jythonsupport.SimplifyScriptSupportAST support for Jython completions. This is not meant to be thorough, but instead should be helpful when working with scripts.
SimplifyScriptSupport( )


***
<a name="alligatorParse"></a>
# alligatorParse
alligatorParse( String script ) &rarr; String

eat away at the end of the script until it can be parsed

### Parameters:
script - a Jython script.

### Returns:
the script with lines at the end removed such that the script can compile.
### See Also:
<a href='JythonCompletionTask.md#trimLinesToMakeValid'>JythonCompletionTask#trimLinesToMakeValid(java.lang.String)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=alligatorParse&unscoped_q=alligatorParse">[search for examples]</a>

***
<a name="getIndent"></a>
# getIndent
getIndent( String line ) &rarr; String

return the indent for a line, for example the " " in " continue "

### Parameters:
line - a String

### Returns:
the indent

<a href="https://github.com/autoplot/dev/search?q=getIndent&unscoped_q=getIndent">[search for examples]</a>

***
<a name="getSourceForStatement"></a>
# getSourceForStatement
getSourceForStatement( java.lang.String[] ss, stmtType o ) &rarr; String

Using the stmtType get the line, or lines. If the last line contains a single triple-quote, we need to kludge a little and
 look for the preceding triple-quote in previous lines.

### Parameters:
ss - a java.lang.String[]
<br>o - a stmtType

### Returns:
a String


<a href="https://github.com/autoplot/dev/search?q=getSourceForStatement&unscoped_q=getSourceForStatement">[search for examples]</a>

***
<a name="removeSideEffects"></a>
# removeSideEffects
removeSideEffects( String script ) &rarr; String

Remove parts of the script which are expensive so that the script can be run and completions offered. TODO: What is the
 difference between this and simplifyScriptToCompletions?

### Parameters:
script - Jython script

### Returns:
simplified version of the script.
### See Also:
<a href='#simplifyScriptToCompletions'>simplifyScriptToCompletions(java.lang.String)</a> <br>
<a href='https://github.com/autoplot/dev/tree/master/bugs/sf/1687'>https://github.com/autoplot/dev/tree/master/bugs/sf/1687</a> <br>

<a href="https://github.com/autoplot/dev/search?q=removeSideEffects&unscoped_q=removeSideEffects">[search for examples]</a>

***
<a name="simplifyScriptToCompletions"></a>
# simplifyScriptToCompletions
simplifyScriptToCompletions( String script ) &rarr; String

extracts the parts of the program that are quickly executed, generating a code which can be run and then queried for
 completions. This uses a Jython syntax tree (AST), so the code must be free of syntax errors. This will remove lines from the
 end of the code until the code compiles, in case the script has a partially defined def or class.

### Parameters:
script - the entire python program

### Returns:
the python program with lengthy calls removed.
### See Also:
<a href='#removeSideEffects'>removeSideEffects(java.lang.String)</a> <br>
<a href='JythonUtil.md#simplifyScriptToGetParams'>JythonUtil#simplifyScriptToGetParams(java.lang.String, boolean)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=simplifyScriptToCompletions&unscoped_q=simplifyScriptToCompletions">[search for examples]</a>

***
<a name="simplifyScriptToGetCompletions"></a>
# simplifyScriptToGetCompletions
simplifyScriptToGetCompletions( java.lang.String[] ss, stmtType[] stmts, java.util.HashSet variableNames, int beginLine, int lastLine, int depth ) &rarr; String

Extracts the parts of the program that get parameters or take a trivial amount of time to execute. This may call itself
 recursively when if blocks are encountered. See test038.

### Parameters:
ss - the entire script, with a null at index 0.
<br>stmts - statements being processed.
<br>variableNames - variable names that have been resolved.
<br>beginLine - first line of the script being processed, or -1 to use stmts[0].beginLine
<br>lastLine - INCLUSIVE last line of the script being processed.
<br>depth - recursion depth, for debugging.

### Returns:
the simplified script
### See Also:
<a href='JythonUtil.md#simplifyScriptToGetParams'>JythonUtil#simplifyScriptToGetParams(java.lang.String[], org.python.parser.ast.stmtType[], java.util.HashSet, int, int,
 int)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=simplifyScriptToGetCompletions&unscoped_q=simplifyScriptToGetCompletions">[search for examples]</a>

