# org.das2.jythoncompletion.ui.LazyListModel.FilterInterface for those that wish to filter content of the list.
 This filter is expected to always return the same result for
 the same object - e.g. either always exclude or include it.
***
<a name="accept"></a>
# accept
accept( Object obj ) &rarr; boolean



### Parameters:
obj - an Object

### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=accept&unscoped_q=accept">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="scheduleUpdate"></a>
# scheduleUpdate
scheduleUpdate( java.lang.Runnable run ) &rarr; void

This method is called when the list needs update. It's goal is
 usually to do SwingUtilities.invokeLater, even more rafined 
 methods are allowed.

### Parameters:
run - a Runnable

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=scheduleUpdate&unscoped_q=scheduleUpdate">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

