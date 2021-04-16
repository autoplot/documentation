# org.autoplot.bookmarks.UtilUtility functions for the DataSetSelector.
Util( )


***
<a name="getRecent"></a>
# getRecent
getRecent( org.autoplot.datasource.DataSetSelector sel ) &rarr; List

return the recent entries.

### Parameters:
sel - the selector containing the recent entries.

### Returns:
the list.

<a href="https://github.com/autoplot/dev/search?q=getRecent&unscoped_q=getRecent">[search for examples]</a>

***
<a name="loadRecent"></a>
# loadRecent
loadRecent( String nodeName, org.autoplot.datasource.DataSetSelector sel, java.util.List deft ) &rarr; void

load and maintain recent entries in the context name.  This will also add
 a listener to save recent entries.

### Parameters:
nodeName - the context
<br>sel - the recent entries are added to this selector.
<br>deft - the deft to use with the first invocation.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=loadRecent&unscoped_q=loadRecent">[search for examples]</a>

***
<a name="setRecent"></a>
# setRecent
setRecent( org.autoplot.datasource.DataSetSelector sel, java.util.List recent ) &rarr; void

Convenience method allowing List&lt;Bookmark&gt; to be used.  Note presently, this drops any folders.

### Parameters:
sel - the select
<br>recent - the list of bookmarks

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setRecent&unscoped_q=setRecent">[search for examples]</a>

