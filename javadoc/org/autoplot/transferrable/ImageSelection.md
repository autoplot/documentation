# org.autoplot.transferrable.ImageSelection

Transferable for Images.
 <code>
 ImageSelection imageSelection = new ImageSelection();
 DasCanvas c = parent.applicationModel.canvas;
 Image i = c.getImage(c.getWidth(), c.getHeight());
 imageSelection.setImage(i);
 Clipboard clipboard = Toolkit.getDefaultToolkit().getSystemClipboard();
 clipboard.setContents(imageSelection, ImageSelection.getNullClipboardOwner() )
 </code>

# ImageSelection( )


***
<a name="createTransferable"></a>
# createTransferable
createTransferable( javax.swing.JComponent comp ) &rarr; Transferable



### Parameters:
comp - a JComponent

### Returns:
java.awt.datatransfer.Transferable


<a href="https://github.com/autoplot/dev/search?q=createTransferable&unscoped_q=createTransferable">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getNullClipboardOwner"></a>
# getNullClipboardOwner
getNullClipboardOwner(  ) &rarr; ClipboardOwner



### Returns:
java.awt.datatransfer.ClipboardOwner


<a href="https://github.com/autoplot/dev/search?q=getNullClipboardOwner&unscoped_q=getNullClipboardOwner">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getSourceActions"></a>
# getSourceActions
getSourceActions( javax.swing.JComponent c ) &rarr; int



### Parameters:
c - a JComponent

### Returns:
int


<a href="https://github.com/autoplot/dev/search?q=getSourceActions&unscoped_q=getSourceActions">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getTransferData"></a>
# getTransferData
getTransferData( java.awt.datatransfer.DataFlavor flavor ) &rarr; Object



### Parameters:
flavor - a DataFlavor

### Returns:
java.lang.Object


<a href="https://github.com/autoplot/dev/search?q=getTransferData&unscoped_q=getTransferData">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getTransferDataFlavors"></a>
# getTransferDataFlavors
getTransferDataFlavors(  ) &rarr; DataFlavor



### Returns:
java.awt.datatransfer.DataFlavor[]


<a href="https://github.com/autoplot/dev/search?q=getTransferDataFlavors&unscoped_q=getTransferDataFlavors">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="importData"></a>
# importData
importData( javax.swing.JComponent comp, java.awt.datatransfer.Transferable t ) &rarr; boolean



### Parameters:
comp - a JComponent
<br>t - a Transferable

### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=importData&unscoped_q=importData">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isDataFlavorSupported"></a>
# isDataFlavorSupported
isDataFlavorSupported( java.awt.datatransfer.DataFlavor flavor ) &rarr; boolean



### Parameters:
flavor - a DataFlavor

### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isDataFlavorSupported&unscoped_q=isDataFlavorSupported">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setImage"></a>
# setImage
setImage( java.awt.Image i ) &rarr; void



### Parameters:
i - an Image

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setImage&unscoped_q=setImage">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

