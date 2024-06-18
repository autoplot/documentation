# Overview

  - Autoplot may be run as a servlet where the input parameter is the
    URI to data.
  - Demo: <http://jfaden.net/AutoplotServlet/simple.jsp>

# Installation

## Basic

  - Download
    <https://jfaden.net/jenkins/job/autoplot-jar-servlet/lastSuccessfulBuild/artifact/autoplot/AutoplotServlet/dist/AutoplotServlet.war>
  - Put the war file in the webapps folder and see
    `http://server:8080/AutoplotServlet` for examples. (Will work with
    an Apache Tomcat version 5.5.20 and up.)
  - Oracle Java 1.8 is required.

Note that an install script is available that installs Oracle Java and
Tomcat on Linux: <https://github.com/autoplot/servlet>

# Parameters

See [api\#Common](api.md#common "wikilink") for the list of all parameters.
Check the [history](http://autoplot.org/servlet_guide&action=history)
for recent additions. The code for the servlet is here:
[1](https://autoplot.svn.sourceforge.net/svnroot/autoplot/autoplot/trunk/AutoplotServlet/src/java/org/virbo/autoplot/SimpleServlet.java)

Servlet-only parameters:

  - **format** specifies the return format type
      - image/png
      - application/pdf
      - image/svg+xml
  - **canvas.aspect**. Aspect ratio for the canvas. Aspect is
    width/height, and simple expressions like '10/3' are handled.
  - **width** and **height** (servlet only - applets should specify
    width and height in <applet> tag.)
  - **process** specifies a process to apply to the loaded data.
      - histogram performs a 100-bin histogram on the data. The data is
        autoranged to establish min, max and scale type.
      - magnitude(fft) displays the frequency content of the data
  - **drawGrid=true** turns on the grid at axis major ticks.

# Caching

If images take a long time to generate, use `mod_disk_cache` to allow a
cached version of the image to be used if it exists.

If the servlet is at

```
http://server/AutoplotServlet/SimpleServlet?url=...
```

use the URL

```
http://server/cache/AutoplotServlet/SimpleServlet?url=...
```

to use a cached image if it exists by adding the following to the Apache
configuration file:

```
 CacheRoot /var/cache/apache2/mod_disk_cache                                                                                                                                                                                                
 CacheEnable disk /cache                                                                                                                                                                                                                    
 CacheDirLevels 5                                                                                                                                                                                                                           
 CacheDirLength 3                                                                                                                                                                                                                           
 CacheIgnoreNoLastMod On                                                                                                                                                                                                                    
 CacheIgnoreCacheControl On                                                                                                                                                                                                                 
 ExpiresActive on                                                                                                                                                                                                                           
 ExpiresDefault "access plus 1 year"                                                                                                                                                                                                        
 CacheMaxFileSize 1000000                                                                                                                                                                                                                   
 CacheMinFileSize 0                                                                                                                                                                                                                         
                                                                                                                                                                                                                                            
 # Better alternative is used by using a second ProxyPass                                                                                                                                                                                   
 # NE means no escape (prevents double escaping of URL).                                                                                                                                                                                    
 # RewriteRule ^/cache/AutoplotServlet(.*)$ /AutoplotServlet$1 [R,NE]                                                                                                                                                                       
                                                                                                                                                                                                                                            
 Options Indexes FollowSymLinks MultiViews                                                                                                                                                                                                  
 <Proxy *>                                                                                                                                                                                                                                  
   Order Allow,Deny                                                                                                                                                                                                                         
   Allow from all                                                                                                                                                                                                                           
 `</Proxy>`                                                                                                                                                                                                                                   
 ProxyPass /AutoplotServlet ajp://localhost:8009/AutoplotServlet                                                                                                                                                                            
 ProxyPassReverse /AutoplotServlet ajp://localhost:8009/AutoplotServlet                                                                                                                                                                     
                                                                                                                                                                                                                                            
 # This second proxy pass causes the following warning:                                                                                                                                                                                     
 # (Otherwise caching works as expected.)                                                                                                                                                                                                   
 # [warn] worker ajp://localhost:8009/AutoplotServlet already used by another worker                                                                                                                                                        
 # I think this is ok given what I am                                                                                                                                                                                                       
 # using this for (caching).  An explanation of the reason is                                                                                                                                                                               
 # here:                                                                                                                                                                                                                                    
 # `<https://issues.apache.org/bugzilla/show_bug.cgi?id=44350#c6>`                                                                                                                                                                              
                                                                                                                                                                                                                                            
 # If we make it down here, then no image was cached                                                                                                                                                                                        
 ProxyPass /cache/AutoplotServlet ajp://localhost:8009/AutoplotServlet                                                                                                                                                                      
 ProxyPassReverse /cache/AutoplotServlet ajp://localhost:8009/AutoplotServlet
```

# Server Configuration

When the server is first installed, there are a number of security
restrictions on the server. This is because, for example, running a jyds
URI has the effect of running arbitrary code on the server. (Note we
continue to tighten security on jyds scripts, and ideally they could be
shown to be "safe," but this is not a trivial problem.) Also, local
files cannot be plotted. This is because the Autoplot server could be
made to plot the contents of a file that is intended to be restricted to
those who can log into the machine. The servlet should be run as an
unprivileged user and not root\! There may be additional security holes,
and the software must be used your own discretion.

.../AutoplotServlet/ServletInfo shows the server configuration. (Note
this shows the world private server-side information, and will be
restricted at some point.)

The default configation is that Autoplot is able to plot data from
anywhere, but data from local files is not allowed. Local vap files are
allowed, since they are under the control of the administrator, but
cannot contain references to local files.

The whitelist file shows which URLs the server is allowed to access
.jyds scripts from.

The file ids.txt allow a reference to an arbitrary URI by defining
identifiers in a table. For example:

```
bat1   /home/jbf/fun/sounds/BatFlying31109.wav
boom(.*)   /home/jbf/fun/sounds/boom$1.wav
```

in ids.txt will make it so that
.../AutoplotServlet/SimpleServlet?id=bat1 will plot
/home/jbf/fun/sounds/BatFlying31109.wav and
.../AutoplotServlet/SimpleServlet?id=boom3 will plot
/home/jbf/fun/sounds/boom3.wav . Note for security, no id can contain
.., so it is not necessary to test for this.

# Security

  - No remote .jyds scripts are allowed. This is because it's not
    trivial to ensure that a .jyds script isn't malicious, and this may
    be relaxed in the future.
  - No local .jyds scripts are allowed.
  - local vap files, under the server's control, can be used to plot
    local data.
  - local data cannot be plotted directly. (A malicious client could
    plot vap+bin:/etc/passwd, for example.)
  - HOME/autoplot\_data/server/whitelist.txt file allows the server
    administrator to allow scripts from some locations.
  - HOME/autoplot\_data/server/id.txt allows a mapping from string to
    URI. This allows implementation details to be completely hidden from
    clients.
  - HOME/autoplot\_data/server/data/ is used for relative references.

However, there may be additional security holes, and the software must
be used your own discretion.

Presently the ServletInfo script indicates server-side information, for
debugging purposes. This will probably be remove as the server matures.

## Encumbering the Server

This is computationally intensive and a small number of malicious
clients could easy overwhelm the system.

## Overloading the Server

Data is cached as it is read in to produce images, and there is no
mechanism to unload the cache. Malicious clients could cause Autoplot to
fill its disk storage.

People who wish to serve their data in images alongside their digital
data can use "ro\_cache.txt" files within the servlet file cache so that
copies are not made.

