# org.autoplot.JythonMainSupport for invoking Jython script.  This is Just ".../AutoplotUI --script ..." stripped down, and was rewritten after Bob and Jeremy
 would see inconsistent behavior between:<pre>
  /usr/local/jre1.6.0_25/bin/java -cp ./autoplot.jar -Djava.awt.headless=true org.autoplot.JythonMain `pwd`/testVars.jy   (and)
  /usr/local/jre1.6.0_25/bin/java -cp ./autoplot.jar -Djava.awt.headless=true org.autoplot.AutoplotUI --script=`pwd`/testVars.jy
 </pre>
JythonMain( )


***
<a name="main"></a>
# main
main( java.lang.String[] args ) &rarr; void

org.virbo.autoplot.JythonMain 
 <ul>
 <li>no args, get input from stdin
 <li>one arg is the name of a local file containing the script.
 </ul>

### Parameters:
args - zero or one command line argument.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=main&unscoped_q=main">[search for examples]</a>

