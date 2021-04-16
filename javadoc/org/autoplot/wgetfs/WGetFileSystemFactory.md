# org.autoplot.wgetfs.WGetFileSystemFactoryImplemented to relieve all the annoying http problems we see at LANL.  If
 the system is a Mac, then curl is used, otherwise wget is used.  Either
 way, if the system environment property AP_WGET, WGET, AP_CURL, CURL is set
 then the implied executable is used.
WGetFileSystemFactory( )


***
<a name="createFileSystem"></a>
# createFileSystem
createFileSystem( java.net.URI root ) &rarr; FileSystem



### Parameters:
root - an URI

### Returns:
org.das2.util.filesystem.FileSystem


<a href="https://github.com/autoplot/dev/search?q=createFileSystem&unscoped_q=createFileSystem">[search for examples]</a>

