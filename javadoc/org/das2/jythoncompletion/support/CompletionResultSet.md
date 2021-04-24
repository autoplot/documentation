# org.das2.jythoncompletion.support.CompletionResultSet

Listener interface for passing the query results.

***
<a name="PRIORITY_SORT_TYPE"></a>
# PRIORITY_SORT_TYPE

Sort type returned from {@link #getSortType()}
 that prefers priority of the item ({@link CompletionItem#getSortPriority()})
 over the text of the item ({@link CompletionItem#getSortText()}).

***
<a name="TEXT_SORT_TYPE"></a>
# TEXT_SORT_TYPE

Sort type returned from {@link #getSortType()}
 that prefers text of the item ({@link CompletionItem#getSortText()}).
 over the priority of the item ({@link CompletionItem#getSortPriority()})

***
<a name="addAllItems"></a>
# addAllItems
addAllItems( java.util.Collection items ) &rarr; boolean

Add the collection of the completion items to this result set.
 <br>
 This method can be called multiple times until
 all the items have been added to ths result set.
 <br>
 After the adding is completed @link #finish()} must be called to confirm
 that the result set will no longer be modified.

### Parameters:
items - collection of items to be added.

### Returns:
true if adding of the items can continue
  or false if there is already too many items
  to be practical to display in the listbox so subsequent
  adding should preferably be discontinued.

<a href="https://github.com/autoplot/dev/search?q=addAllItems&unscoped_q=addAllItems">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="addItem"></a>
# addItem
addItem( org.das2.jythoncompletion.support.CompletionItem item ) &rarr; boolean

Add the completion item to this result set.
 <br>
 This method can be called multiple times until
 all the items have been added to ths result set.
 <br>
 After the adding is completed @link #finish()} must be called to confirm
 that the result set will no longer be modified.

### Parameters:
item - non-null completion item.

### Returns:
true if adding of the items can continue
  or false if there is already too many items
  to be practical to display in the listbox so subsequent
  adding should preferably be discontinued.

<a href="https://github.com/autoplot/dev/search?q=addItem&unscoped_q=addItem">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="estimateItems"></a>
# estimateItems
estimateItems( int estimatedItemCount, int estimatedItemWidth ) &rarr; void

Indicate that adding of the items to this result set
 will likely need a long time so the resulting number of items
 and their visual size should be estimated so that
 the completion infrastructure can estimate the size
 of the popup window and display the items added subsequently
 without changing its bound extensively.
 <br>
 Without calling of this method the completion infrastructure
 will wait until {@link #finish()} gets called on this result set
 before displaying any of the items added to this result set.

 <p>
 By calling of this method the task also confirms
 that the items added by {@link #addItem(CompletionItem)} subsequently
 are already in the order corresponding to the {@link #getSortType()}.

### Parameters:
estimatedItemCount - estimated number of the items that will
  be added to this result set by {@link #addItem(CompletionItem)}.
  If the estimate is significantly lower than the reality then
  the vertical scrollbar granularity may be decreased or the vertical
  scrollbar can be removed completely once the result set is finished.
  If the estimate is significantly higher than the reality then
  the vertical scrollbar granularity may be increased
  once the result set is finished.
<br>estimatedItemWidth - estimated maximum visual width of a completion item.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=estimateItems&unscoped_q=estimateItems">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="finish"></a>
# finish
finish(  ) &rarr; void

Mark that this result set is finished and there will be no more
 modifications done to it.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=finish&unscoped_q=finish">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getSortType"></a>
# getSortType
getSortType(  ) &rarr; int

Get the sort type currently used by the code completion.
 <br>
 It's one of the {@link #PRIORITY_SORT_TYPE} or {@link #TEXT_SORT_TYPE}.

### Returns:
int


<a href="https://github.com/autoplot/dev/search?q=getSortType&unscoped_q=getSortType">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isFinished"></a>
# isFinished
isFinished(  ) &rarr; boolean

Check whether this result set is finished.

### Returns:
true if the result set is already finished by previous call
  to {@link #finish()}.

<a href="https://github.com/autoplot/dev/search?q=isFinished&unscoped_q=isFinished">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setAnchorOffset"></a>
# setAnchorOffset
setAnchorOffset( int anchorOffset ) &rarr; void

Set the document offset to which the returned completion items
 or documentation or tooltip should be anchored.
 <br>
 If there will be multiple completion providers setting this property
 for the given mime-type then only the first one
 (according to the xml-layer registration order)
 will be taken into account.

### Parameters:
anchorOffset - an int

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setAnchorOffset&unscoped_q=setAnchorOffset">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setDocumentation"></a>
# setDocumentation
setDocumentation( org.das2.jythoncompletion.support.CompletionDocumentation documentation ) &rarr; void

Set the documentation to this result set.
 <br>
 Calling this method is only relevant for tasks
 created by {@link CompletionProvider#createTask(int, javax.swing.text.JTextComponent)}
 with {@link CompletionProvider#DOCUMENTATION_QUERY_TYPE}
 or for {@link CompletionItem#createDocumentationTask()}.

### Parameters:
documentation - a CompletionDocumentation

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setDocumentation&unscoped_q=setDocumentation">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setHasAdditionalItems"></a>
# setHasAdditionalItems
setHasAdditionalItems( boolean value ) &rarr; void

Indicate that additional items could be added to this result set. However,
 adding of these items will likely need a long time to complete so it is
 preferred to add them only on the special code completion invocation
 denoted by {@link CompletionProvider#COMPLETION_ALL_QUERY_TYPE}.
 <br>
 Calling this method is relevant only for tasks
 created by {@link CompletionProvider#createTask(int, javax.swing.text.JTextComponent)}
 with {@link CompletionProvider#COMPLETION_QUERY_TYPE}.

### Parameters:
value - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setHasAdditionalItems&unscoped_q=setHasAdditionalItems">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setTitle"></a>
# setTitle
setTitle( String title ) &rarr; void

Set title that will be assigned to the completion popup window.
 <br>
 It's only relevant to set the title when providing completion items
 for {@link CompletionProvider#COMPLETION_QUERY_TYPE}.
 <br>
 If there will be multiple completion providers setting this property
 for the given mime-type then only the first one
 (according to the xml-layer registration order)
 will be taken into account.

### Parameters:
title - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setTitle&unscoped_q=setTitle">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setToolTip"></a>
# setToolTip
setToolTip( javax.swing.JToolTip toolTip ) &rarr; void

Set the tooltip to this result set.
 <br>
 Calling this method is only relevant for tasks
 created by {@link CompletionProvider#createTask(int, javax.swing.text.JTextComponent)}
 with {@link CompletionProvider#TOOLTIP_QUERY_TYPE}
 or for {@link CompletionItem#createToolTipTask()}.

### Parameters:
toolTip - a JToolTip

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setToolTip&unscoped_q=setToolTip">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setWaitText"></a>
# setWaitText
setWaitText( String waitText ) &rarr; void

Set the explicit value displayed in a label when the completion results
 do not get computed during a certain timeout (e.g. 250ms).
 <br>
 If not set explicitly the completion infrastructure will use
 the default text.

### Parameters:
waitText - description of what the query copmutation
  is currently (doing or waiting for).
  <br>
  After previous explicit setting <code>null</code> can be passed
  to restore using of the default text.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setWaitText&unscoped_q=setWaitText">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="toString"></a>
# toString
toString(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=toString&unscoped_q=toString">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

