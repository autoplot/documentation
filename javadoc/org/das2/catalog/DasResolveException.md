# org.das2.catalog.DasResolveException

Exception thrown if a path can not be resolved.
 
 These are handled internally by the catalog package if possible, but some 
 paths just aren't resolvable no matter how many catalog branches are inspected.

# DasResolveException( String msg, String sPath )
Construct a das2 catalog resolution exception

# DasResolveException( String msg, java.lang.Throwable ex, String sPath )
Construct a das2 catalog resolution exception, and attache a cause.

