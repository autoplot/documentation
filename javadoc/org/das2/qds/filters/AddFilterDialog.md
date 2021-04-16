# org.das2.qds.filters.AddFilterDialogDialog for picking a new filter to add.  This uses a tree to sort the filters, based on
 http://emfisis.physics.uiowa.edu/pub/jy/filters/filters.xml
 at U. Iowa, and keeps track of opened nodes.
AddFilterDialog( )
Creates new form AddFilterDialog

***
<a name="build"></a>
# build
build( java.io.InputStream in ) &rarr; DefaultMutableTreeNode

return the tree of filters in the file.

### Parameters:
in - an InputStream

### Returns:
a javax.swing.tree.DefaultMutableTreeNode


<a href="https://github.com/autoplot/dev/search?q=build&unscoped_q=build">[search for examples]</a>

***
<a name="getValue"></a>
# getValue
getValue(  ) &rarr; String

return the selected filter, such as "|smooth(5)"

### Returns:
the selected filter.

<a href="https://github.com/autoplot/dev/search?q=getValue&unscoped_q=getValue">[search for examples]</a>

***
<a name="main"></a>
# main
main( java.lang.String[] args ) &rarr; void



### Parameters:
args - a java.lang.String[]

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=main&unscoped_q=main">[search for examples]</a>

