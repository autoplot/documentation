# org.das2.graph.dnd.TransferableRenderer
TransferableRenderer( org.das2.graph.Renderer renderer )
Creates a new instance of TransferableRenderer

***
<a name="RENDERER_FLAVOR"></a>
# RENDERER_FLAVOR



***
<a name="getTransferData"></a>
# getTransferData
getTransferData( java.awt.datatransfer.DataFlavor flavor ) &rarr; Object

Returns an object which represents the data to be transferred.  The class
 of the object returned is defined by the representation class of the flavor.

### Parameters:
flavor - the requested flavor for the data

### Returns:
java.lang.Object

### See Also:
<a href='DataFlavor.md#getRepresentationClass'>DataFlavor#getRepresentationClass</a> <br>

<a href="https://github.com/autoplot/dev/search?q=getTransferData&unscoped_q=getTransferData">[search for examples]</a>

***
<a name="getTransferDataFlavors"></a>
# getTransferDataFlavors
getTransferDataFlavors(  ) &rarr; DataFlavor

Returns an array of DataFlavor objects indicating the flavors the data
 can be provided in.  The array should be ordered according to preference
 for providing the data (from most richly descriptive to least descriptive).

### Returns:
an array of data flavors in which this data can be transferred

<a href="https://github.com/autoplot/dev/search?q=getTransferDataFlavors&unscoped_q=getTransferDataFlavors">[search for examples]</a>

***
<a name="isDataFlavorSupported"></a>
# isDataFlavorSupported
isDataFlavorSupported( java.awt.datatransfer.DataFlavor flavor ) &rarr; boolean

Returns whether or not the specified data flavor is supported for
 this object.

### Parameters:
flavor - the requested flavor for the data

### Returns:
boolean indicating whether or not the data flavor is supported

<a href="https://github.com/autoplot/dev/search?q=isDataFlavorSupported&unscoped_q=isDataFlavorSupported">[search for examples]</a>

