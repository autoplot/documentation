# org.das2.catalog.DasSrcNodeSource nodes add extra functions to generic catalog nodes
***
<a name="query"></a>
# query
query( java.util.Map dQuery ) &rarr; QDataSet

Given a parameter query string, get the access information.  
 
 In an ideal world this would just return the dataset itself.  But that is the 
 point of the org.autoplot.DataSource interface and it's on the fly factory
 discovery.

### Parameters:
dQuery - a java.util.Map

### Returns:
a QDataSet


<a href="https://github.com/autoplot/dev/search?q=query&unscoped_q=query">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="queryVerify"></a>
# queryVerify
queryVerify( java.util.Map dQuery ) &rarr; boolean

Determine if the given list of query parameters are valid

### Parameters:
dQuery - a java.util.Map

### Returns:
True if this set of parameters is valid, false otherwise

<a href="https://github.com/autoplot/dev/search?q=queryVerify&unscoped_q=queryVerify">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

