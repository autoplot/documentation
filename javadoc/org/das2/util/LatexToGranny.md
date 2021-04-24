# org.das2.util.LatexToGranny

Lightweight converter for LaTeX expressions to Granny strings, for the
 MMS mission.  This handles strings like:<ul>
 <li> cm^{-3} 
 <li> nA/m^{2} 
 <li> \rho^2 + 2\Gamma_{ij}
 <li> \sqrt{a + b}  (This is not handled by the IDL library either.)
 </ul>
 The IDL project that minimally specifies is: TeXtoIDL, at http://physics.mnstate.edu/craig/textoidl/

# LatexToGranny( )


***
<a name="isLatex"></a>
# isLatex
isLatex( String s ) &rarr; boolean

detect if the string is LaTeX.  This currently looks for ^{ or _{,
 but is expected to be changed in the future.

### Parameters:
s - the string

### Returns:
true if the string appears to be LaTeX.

<a href="https://github.com/autoplot/dev/search?q=isLatex&unscoped_q=isLatex">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="latexToGranny"></a>
# latexToGranny
latexToGranny( String latex ) &rarr; String

for the latex encoded string, return the granny string that 
 implements.

### Parameters:
latex - LaTeX encoded string.  E.g. \rho^2 + 2\Gamma_{ij}

### Returns:
the granny string.  E.g. <code>&rho;!U2!n + 2&Gamma;!Dij!N</code>

<a href="https://github.com/autoplot/dev/search?q=latexToGranny&unscoped_q=latexToGranny">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="main"></a>
# main
main( java.lang.String[] args ) &rarr; void



### Parameters:
args - a java.lang.String[]

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=main&unscoped_q=main">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

