# org.autoplot.jythonsupport.JythonToJavaConverterexperiment with code which converts the Jython AST (syntax tree) into Java
 code.
JythonToJavaConverter( )


***
<a name="addImport"></a>
# addImport
addImport( javax.swing.text.Document doc, String pkg, String name ) &rarr; void

add the class to the list of imports.

### Parameters:
doc - the document
<br>pkg - the Java package
<br>name - the Java class name.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=addImport&unscoped_q=addImport">[search for examples]</a>

addImport( javax.swing.text.Document doc, String pkg, String name, int cursorPosition ) &rarr; void<br>
addImport( String src, String pkg, String name ) &rarr; String<br>
***
<a name="convert"></a>
# convert
convert( String script ) &rarr; String



### Parameters:
script - a String

### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=convert&unscoped_q=convert">[search for examples]</a>

***
<a name="convertReverse"></a>
# convertReverse
convertReverse( String javaCode ) &rarr; String

The goal is to take Java snippets and turn them into Jython code.
 This is all overly simplistic and should be done properly.  Cheesy!
 
 More TODOs:
 throw IllegalArgumentException -> raise exception
 Character.isDigit -> string.isnumeric
 "".startsWith -> "".startswith
 "".trim() -> "".strip()
 || -> or
 && -> and
 ! -> not
 int[] d -> d
 System.arraycopy -> for i in range(0,6): a[i]=a[i+6]

### Parameters:
javaCode - a String

### Returns:
conversion to Jython-like code.

<a href="https://github.com/autoplot/dev/search?q=convertReverse&unscoped_q=convertReverse">[search for examples]</a>

***
<a name="guessCompletions"></a>
# guessCompletions
guessCompletions( String clas ) &rarr; List

return a list of classes which are reasonable completions for the class
 provided. For example, "JP" would result in "JPanel" and "JPasswordField"
 TODO: what if this were to run through all the known JavaDoc

### Parameters:
clas - a String

### Returns:
list of completions.

<a href="https://github.com/autoplot/dev/search?q=guessCompletions&unscoped_q=guessCompletions">[search for examples]</a>

***
<a name="guessPackage"></a>
# guessPackage
guessPackage( String clas ) &rarr; String

scan through the list of imports in /importLookup.jy, to see
 if the symbol can be imported.  This will return null (None) if
 there are no suggestions, or the name of the package.

### Parameters:
clas - the class name, for example "JSlider"

### Returns:
the package or null, for example "javax.swing"

<a href="https://github.com/autoplot/dev/search?q=guessPackage&unscoped_q=guessPackage">[search for examples]</a>

***
<a name="hasImport"></a>
# hasImport
hasImport( String src, String pkg, String name ) &rarr; boolean

return true if the class has been imported.  Note this is not thorough
 and should be reviewed at some point.

### Parameters:
src - the Jython source
<br>pkg - the Java package
<br>name - the Java class name.

### Returns:
true if the class has been imported already.

<a href="https://github.com/autoplot/dev/search?q=hasImport&unscoped_q=hasImport">[search for examples]</a>

***
<a name="main"></a>
# main
main( java.lang.String[] args ) &rarr; void



### Parameters:
args - a java.lang.String[]

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=main&unscoped_q=main">[search for examples]</a>

