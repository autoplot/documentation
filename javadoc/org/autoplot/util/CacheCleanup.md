# org.autoplot.util.CacheCleanupThis was intended to provide a mechanism to remove old files from
 an enduser's cache, where version number updates result in files which
 will never be seen.
***
<a name="deleteOldVersions"></a>
# deleteOldVersions
deleteOldVersions(  ) &rarr; void



### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=deleteOldVersions&unscoped_q=deleteOldVersions">[search for examples]</a>

***
<a name="findAggs"></a>
# findAggs
findAggs(  ) &rarr; String

find aggregations within the user's history.  This currently looks for $Y, but aggregations
 can also be $y, etc.

### Returns:
list of aggregations.

<a href="https://github.com/autoplot/dev/search?q=findAggs&unscoped_q=findAggs">[search for examples]</a>

***
<a name="findOldVersions"></a>
# findOldVersions
findOldVersions(  ) &rarr; String

Return an array of files where newer versions prevent the older from being used.  This will
 not look for version constraints (e.g. $(v,lt=2)), so use with some care.

### Returns:
an array of files where newer versions prevent the older from being used.

<a href="https://github.com/autoplot/dev/search?q=findOldVersions&unscoped_q=findOldVersions">[search for examples]</a>

