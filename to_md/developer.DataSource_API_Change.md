Presently the DataSourceFactory objects get a URL and return a
DataSource object. This means that though Autoplot uses URIs, URIS like

` vap+data:1,2,3,4,5,6,7`  
` vap+jbdc:mysql://192.168.0.203:3306/db=orbits&table=cluster1&column=orbitnum&dep0=time`  
` vap+dat:spawn://home/jbf/readers/cluster.sh`

are excluded.

# Proposal

DataSourceFactory should get a URI and should return a DataSource.

DataSource just has a getDataSet(monitor) method, so this API is fine.

AbstractDataSource is URL-based. Should the subclasses see URI or the
string after the scheme (scheme-specific part)?

TimeSeriesBrowse is URL based and there's kludgy code in there to add
and remove the vap+dat scheme.

AggregatingDataSource is URL based and should use fully-resolved URIs

# Issues Encountered

## Spaces in Filenames

Not surprisingly, spaces in filenames cause problems again. This is a
break-it-to-fix-it, because surely the situation is better now without
the URL\<--\>URI conversions as well. Fortunately a number of
once-working URIs are documented and we can fix the problem. Clearly the
spaces logic will be handled in the conversion to and from URIs, since
URIs are pretty specific about how to encode spaces. The
pluses-are-spaces logic should be implemented at the presentation
layer...
