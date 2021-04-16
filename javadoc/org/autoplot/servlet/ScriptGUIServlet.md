# org.autoplot.servlet.ScriptGUIServletRun a script on the server side, and produce a client-side GUI for the 
 getParam calls.
 Note this has logging installed which is set up in code, which is bad practice.  This should be 
 removed should this be used in production!
ScriptGUIServlet( )


***
<a name="getServletInfo"></a>
# getServletInfo
getServletInfo(  ) &rarr; String

Returns a short description of the servlet.

### Returns:
a String containing servlet description

<a href="https://github.com/autoplot/dev/search?q=getServletInfo&unscoped_q=getServletInfo">[search for examples]</a>

***
<a name="writeToPng"></a>
# writeToPng
writeToPng( org.autoplot.dom.Application dom, java.io.OutputStream out ) &rarr; void

write out the current canvas to stdout.  This is introduced to support servers.
 TODO: this has issues with the size.  See writeToPng(filename).

### Parameters:
dom - an Application
<br>out - the OutputStream accepting the data, which is not closed.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=writeToPng&unscoped_q=writeToPng">[search for examples]</a>

