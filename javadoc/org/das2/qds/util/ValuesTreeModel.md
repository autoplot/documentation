# org.das2.qds.util.ValuesTreeModel

provides a TreeModel representation of the dataset's properties.

# ValuesTreeModel( QDataSet ds )


# ValuesTreeModel( String prefix, QDataSet ds )


***
<a name="valuesTreeNode"></a>
# valuesTreeNode
valuesTreeNode( String prefix, javax.swing.tree.MutableTreeNode aroot, QDataSet ds, int sizeLimit ) &rarr; MutableTreeNode

return a tree node for the values of a dataset.

### Parameters:
prefix - prefix added to the each node, e.g. "value("
<br>aroot - the parent to which the nodes are added.
<br>ds - the dataset to represent.
<br>sizeLimit - the number of nodes to represent, e.g. 20, and ellipses (...) will represent the values not shown.

### Returns:
the node (aroot) is returned.

<a href="https://github.com/autoplot/dev/search?q=valuesTreeNode&unscoped_q=valuesTreeNode">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="valuesTreeNode2"></a>
# valuesTreeNode2
valuesTreeNode2( String prefix, javax.swing.tree.TreeNode parent, QDataSet ds ) &rarr; TreeNode

The valuesTreeNode implementation that uses MutableTreeNodes cannot scale to very large datasets, since all
 nodes are created immediately.  This implementation only queries the dataset as children are opened, and
 should eventually allow for exploration of any dataset.  This is not used right now in the metadata
 tab of Autoplot because the root node of the tree is a MutableTreeNode and all children must therefore
 be MutableTreeNodes.

### Parameters:
prefix - string prefix, a number of spaces to indent
<br>parent - the parent node
<br>ds - the dataset source of the values.

### Returns:
the tree node

<a href="https://github.com/autoplot/dev/search?q=valuesTreeNode2&unscoped_q=valuesTreeNode2">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

