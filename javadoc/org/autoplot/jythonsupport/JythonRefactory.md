# org.autoplot.jythonsupport.JythonRefactoryProvide one class that manages backwards compatibility as package names
 are changed.  See https://sourceforge.net/p/autoplot/feature-requests/528/
JythonRefactory( )


***
<a name="fixImports"></a>
# fixImports
fixImports( String s ) &rarr; String

Convert old names to modern names, for example "org.virbo.autoplot" to
 "org.autoplot".  Autoplot became its own project early on, but the code
 was slow to update.

### Parameters:
s - the script

### Returns:
the script with new names.

<a href="https://github.com/autoplot/dev/search?q=fixImports&unscoped_q=fixImports">[search for examples]</a>

fixImports( String s, String name ) &rarr; String<br>
fixImports( java.io.InputStream in ) &rarr; InputStream<br>
fixImports( java.io.InputStream in, String name ) &rarr; InputStream<br>
***
<a name="main"></a>
# main
main( java.lang.String[] args ) &rarr; void



### Parameters:
args - a java.lang.String[]

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=main&unscoped_q=main">[search for examples]</a>

