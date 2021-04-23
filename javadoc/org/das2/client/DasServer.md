# org.das2.client.DasServer

Represents a remote Das 2.1 compliant server.  

 Use the create() method to instantiate new Das 2 server objects.  Each call to
 create() will only allocate a new server instance if no server matching the given URL
 has already been created.

***
<a name="authenticate"></a>
# authenticate
authenticate( String user, String passCrypt ) &rarr; Key

Handles key based authentication

### Parameters:
user - a String
<br>passCrypt - a String

### Returns:
org.das2.client.Key


<a href="https://github.com/autoplot/dev/search?q=authenticate&unscoped_q=authenticate">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="changePassword"></a>
# <del>changePassword</del>
Deprecated: 
***
<a name="create"></a>
# create
create( java.net.URL url ) &rarr; DasServer

Get a Das2 server instance.

### Parameters:
url - A Das2 resource URL.  Only the protocol, host, port and path information
            are used.  All other items, such as a GET query are ignored.

### Returns:
If a server matching the given url's protocol, host and path has already
 been created, that instance is returned, otherwise a new instance is created.

<a href="https://github.com/autoplot/dev/search?q=create&unscoped_q=create">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="createPlasmaWaveGroup"></a>
# createPlasmaWaveGroup
createPlasmaWaveGroup(  ) &rarr; DasServer

return one DasServer to serve as an example.

### Returns:
an org.das2.client.DasServer


<a href="https://github.com/autoplot/dev/search?q=createPlasmaWaveGroup&unscoped_q=createPlasmaWaveGroup">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDataSetList"></a>
# getDataSetList
getDataSetList(  ) &rarr; TreeModel



### Returns:
javax.swing.tree.TreeModel


<a href="https://github.com/autoplot/dev/search?q=getDataSetList&unscoped_q=getDataSetList">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDataSetListWithDiscovery"></a>
# getDataSetListWithDiscovery
getDataSetListWithDiscovery(  ) &rarr; TreeModel



### Returns:
javax.swing.tree.TreeModel


<a href="https://github.com/autoplot/dev/search?q=getDataSetListWithDiscovery&unscoped_q=getDataSetListWithDiscovery">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getHost"></a>
# getHost
getHost(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getHost&unscoped_q=getHost">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getKey"></a>
# getKey
getKey( String resource ) &rarr; Key



### Parameters:
resource - a String

### Returns:
org.das2.client.Key


<a href="https://github.com/autoplot/dev/search?q=getKey&unscoped_q=getKey">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getLogo"></a>
# getLogo
getLogo(  ) &rarr; ImageIcon



### Returns:
javax.swing.ImageIcon


<a href="https://github.com/autoplot/dev/search?q=getLogo&unscoped_q=getLogo">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getName"></a>
# getName
getName(  ) &rarr; String

Query the remote DasServer for it's id string.
 For Das 2.1 servers this is handled by sending the GET query ?server=id.

### Returns:
A string containing the id, or the empty string if the query failed

<a href="https://github.com/autoplot/dev/search?q=getName&unscoped_q=getName">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getPath"></a>
# getPath
getPath(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getPath&unscoped_q=getPath">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getPort"></a>
# getPort
getPort(  ) &rarr; int



### Returns:
int


<a href="https://github.com/autoplot/dev/search?q=getPort&unscoped_q=getPort">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getProto"></a>
# getProto
getProto(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getProto&unscoped_q=getProto">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getStandardDataStreamSource"></a>
# getStandardDataStreamSource
getStandardDataStreamSource( java.net.URL url ) &rarr; StandardDataStreamSource



### Parameters:
url - an URL

### Returns:
org.das2.client.StandardDataStreamSource


<a href="https://github.com/autoplot/dev/search?q=getStandardDataStreamSource&unscoped_q=getStandardDataStreamSource">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getStreamDescriptor"></a>
# getStreamDescriptor
getStreamDescriptor( java.net.URL dataSetID ) &rarr; StreamDescriptor



### Parameters:
dataSetID - an URL

### Returns:
org.das2.stream.StreamDescriptor


<a href="https://github.com/autoplot/dev/search?q=getStreamDescriptor&unscoped_q=getStreamDescriptor">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getURL"></a>
# getURL
getURL(  ) &rarr; String

Provide the Das2 Server location.  
 Note that more than one Das2 server may be present on a single host web-site.

### Returns:
A URL string containing protocol, host and path information.

<a href="https://github.com/autoplot/dev/search?q=getURL&unscoped_q=getURL">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

getURL( String formData ) &rarr; URL<br>
***
<a name="groups"></a>
# <del>groups</del>
Deprecated: this is not used.
***
<a name="readServerResponse"></a>
# <del>readServerResponse</del>
Deprecated: 
***
<a name="setKey"></a>
# setKey
setKey( org.das2.client.Key key ) &rarr; void



### Parameters:
key - a Key

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setKey&unscoped_q=setKey">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="toString"></a>
# toString
toString(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=toString&unscoped_q=toString">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

