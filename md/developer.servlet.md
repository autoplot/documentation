Purpose: Notes regarding servlet development.

Audience: Autoplot developers working on performance and reliability of
the servlet.

# debugging

The servlet can be run within Netbeans using the debugger.

For the SimpleServlet, requestId can be an integer, and log information
will be dumped into "/tmp/testservlet/log" + requestId + ".txt"

# caching

Firefox seems to cache the results nicely. This method can also be used
to add server-side caching of images.

