# org.das2.jythoncompletion.ui.LazyListModelModel that can compute its values lazily and moreover handle some
 kind of filtering.

 Made public just to test an impl of Children.EntrySource based on this
 filtering list.
***
<a name="addListDataListener"></a>
# addListDataListener
addListDataListener( javax.swing.event.ListDataListener l ) &rarr; void



### Parameters:
l - a ListDataListener

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=addListDataListener&unscoped_q=addListDataListener">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="contentsChanged"></a>
# contentsChanged
contentsChanged( javax.swing.event.ListDataEvent listDataEvent ) &rarr; void



### Parameters:
listDataEvent - a ListDataEvent

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=contentsChanged&unscoped_q=contentsChanged">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="create"></a>
# create
create( javax.swing.ListModel listModel, org.das2.jythoncompletion.ui.LazyListModel.Filter f, double expectedRadio, Object defValue ) &rarr; LazyListModel

Factory method to create new filtering lazy model.

### Parameters:
listModel - a javax.swing.ListModel
<br>f - a LazyListModel.Filter
<br>expectedRadio - a double
<br>defValue - an Object

### Returns:
org.das2.jythoncompletion.ui.LazyListModel


<a href="https://github.com/autoplot/dev/search?q=create&unscoped_q=create">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getElementAt"></a>
# getElementAt
getElementAt( int index ) &rarr; Object

If value is not know for given index and CREATE.get() is Boolean.FALSE it returns defaultValue.

### Parameters:
index - an int

### Returns:
java.lang.Object


<a href="https://github.com/autoplot/dev/search?q=getElementAt&unscoped_q=getElementAt">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getSize"></a>
# getSize
getSize(  ) &rarr; int



### Returns:
int


<a href="https://github.com/autoplot/dev/search?q=getSize&unscoped_q=getSize">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="intervalAdded"></a>
# intervalAdded
intervalAdded( javax.swing.event.ListDataEvent listDataEvent ) &rarr; void



### Parameters:
listDataEvent - a ListDataEvent

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=intervalAdded&unscoped_q=intervalAdded">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="intervalRemoved"></a>
# intervalRemoved
intervalRemoved( javax.swing.event.ListDataEvent listDataEvent ) &rarr; void



### Parameters:
listDataEvent - a ListDataEvent

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=intervalRemoved&unscoped_q=intervalRemoved">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="removeListDataListener"></a>
# removeListDataListener
removeListDataListener( javax.swing.event.ListDataListener l ) &rarr; void



### Parameters:
l - a ListDataListener

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=removeListDataListener&unscoped_q=removeListDataListener">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="run"></a>
# run
run(  ) &rarr; void

When executed, updateYourAssumeptions.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=run&unscoped_q=run">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

