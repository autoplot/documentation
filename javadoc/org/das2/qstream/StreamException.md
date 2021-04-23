# org.das2.qstream.StreamException

This odd class seems to communication information in two directions.
 First, in the streamException method of StreamHandler it is used to communicate that
 something went wrong in the source.  For example, a data file was not found.
 Second, each of the StreamHandler methods can throe StreamExceptions, so they
 could communicate that the client had a problem.
 TODO: this should probably be split up into two exceptions...

# StreamException( String message )
Creates a new instance of StreamException

# StreamException( java.lang.Exception cause )


# StreamException( String message, java.lang.Throwable cause )


***
<a name="NO_DATA_IN_INTERVAL"></a>
# NO_DATA_IN_INTERVAL



***
<a name="EMPTY_RESPONSE_FROM_READER"></a>
# EMPTY_RESPONSE_FROM_READER



