# org.autoplot.servlet.JnlpServlet

Alternative to the CGI/Perl based solutions for dynamically creating the JNLP to
 launch into a specific Autoplot configuration.
 
 This uses the following rules:
 <li>version parameter indicates the version of Autoplot to run.
 <li>max-heap-size parameter indicates the heap size to use, 1G is the default to support 32 bit machines.
 <li>URI or URL parameter is the Autoplot URI or vap file.  Everything following this considered to be part of the URI, so no further servlet parameters can be specified.
 <li>open parameter is also an alias for URI, but I'm not sure if it is used. 
 <li>If the parameter appears to be a URI, then it and everything following it is considered to be part of the URI.
 
 This allows the following URLs, see http://autoplot.org/hudson/job/autoplot-test-jnlp-server/:
  http://autoplot.org/autoplot.jnlp
  http://autoplot.org/autoplot.jnlp?version=devel
  http://autoplot.org/autoplot.jnlp?http://autoplot.org/data.txt
  http://autoplot.org/autoplot.jnlp?version=hudson&URI=http://autoplot.org/data.txt
  http://autoplot.org/autoplot.jnlp?version=hudson&http://autoplot.org/data.txt
  http://autoplot.org/autoplot.jnlp?version=hudson&samp=true
  http://autoplot.org/autoplot.jnlp?version=hudson&samp=true
  http://autoplot.org/autoplot.jnlp?version=hudson&vap+cdaweb:filter=polar
  http://autoplot.org/autoplot.jnlp?vap+bin:http://www-pw.physics.uiowa.edu/voyager/data/pra/v1790205?reportOffset=yes&open=rank2=6:262&recLength=528&type=ushort&byteOrder=big
  http://autoplot.org/autoplot.jnlp?max-heap-size=4G'

# JnlpServlet( )


***
<a name="getServletInfo"></a>
# getServletInfo
getServletInfo(  ) &rarr; String

Returns a short description of the servlet.

### Returns:
a String containing servlet description

<a href="https://github.com/autoplot/dev/search?q=getServletInfo&unscoped_q=getServletInfo">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

