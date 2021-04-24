# org.autoplot.servlet.SecureScriptServlet

This provides a generic method for adding a function to the server via Jython scripts.  Introduced
 to support wildcard-de-globing, this could be used for a number of different ways.
 
 Unlike the ScriptServlet, this requires a reference to a script that already exists on the server, instead of 
 running possibly malicious updated code.

 http://localhost:8084/AutoplotServlet/ScriptServlet2?resourceURI=http://autoplot.org/data/versioning/data_$Y_$m_$d_v$v.qds&timerange=2010-03

# SecureScriptServlet( )


***
<a name="getServletInfo"></a>
# getServletInfo
getServletInfo(  ) &rarr; String

Returns a short description of the servlet.

### Returns:
a String containing servlet description

<a href="https://github.com/autoplot/dev/search?q=getServletInfo&unscoped_q=getServletInfo">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

