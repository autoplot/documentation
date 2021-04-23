# org.autoplot.RecentUrisDialogPresent GUI showing history of plotted URIs with buttons for
 ok, plotting below, as an overplot, or editing.  The getModifiers()
 method is called to see which action was pressed:
<pre>
   0                    replace plot
   KeyEvent.CTRL_MASK   plot below
   KeyEvent.SHIFT_MASK  overplot
   KeyEvent.ALT_MASK    edit this URI.
 </pre>
RecentUrisDialog( java.awt.Frame parent, boolean modal )
Creates new form RecentUrisDialog

***
<a name="PROP_CANCELLED"></a>
# PROP_CANCELLED



***
<a name="PROP_MODIFIERS"></a>
# PROP_MODIFIERS



***
<a name="getModifiers"></a>
# getModifiers
getModifiers(  ) &rarr; int



### Returns:
int


<a href="https://github.com/autoplot/dev/search?q=getModifiers&unscoped_q=getModifiers">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getSelectedURI"></a>
# getSelectedURI
getSelectedURI(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getSelectedURI&unscoped_q=getSelectedURI">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isCancelled"></a>
# isCancelled
isCancelled(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isCancelled&unscoped_q=isCancelled">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="main"></a>
# main
main( java.lang.String[] args ) &rarr; void



### Parameters:
args - the command line arguments

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=main&unscoped_q=main">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setExpertMode"></a>
# setExpertMode
setExpertMode( boolean expert ) &rarr; void



### Parameters:
expert - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setExpertMode&unscoped_q=setExpertMode">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setFilter"></a>
# setFilter
setFilter( String filter ) &rarr; void

set the filter constraining the list.

### Parameters:
filter - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setFilter&unscoped_q=setFilter">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setModifiers"></a>
# setModifiers
setModifiers( int modifiers ) &rarr; void



### Parameters:
modifiers - an int

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setModifiers&unscoped_q=setModifiers">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

