# org.autoplot.datasource.ui.Util

taken from http://www.jguru.com/faq/view.jsp?EID=87579 (see code towards the bottom, view source).

***
<a name="enableComponents"></a>
# enableComponents
enableComponents( java.awt.Container container, boolean enabled, java.awt.Component exclude ) &rarr; void

enable or disable all the components in a container.  
 Thanks to http://stackoverflow.com/questions/10985734/java-swing-enabling-disabling-all-components-in-jpanel

### Parameters:
container - the container
<br>enabled - true to enable, false to disable
<br>exclude - null, or a component to exclude.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=enableComponents&unscoped_q=enableComponents">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isRowHeaderVisible"></a>
# isRowHeaderVisible
isRowHeaderVisible( javax.swing.JTable table ) &rarr; boolean



### Parameters:
table - a JTable

### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isRowHeaderVisible&unscoped_q=isRowHeaderVisible">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="makeJTextFieldLookLikeJLabel"></a>
# makeJTextFieldLookLikeJLabel
makeJTextFieldLookLikeJLabel( javax.swing.JTextField tf ) &rarr; void

make JTextField look like a JLabel.  We don't use JLabels because they don't size nicely, and they don't
 allow user to select text.  Note on Linux, this still doesn't quite get it, but at least this provides one
 place to set the configuration.

### Parameters:
tf - a JTextField

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=makeJTextFieldLookLikeJLabel&unscoped_q=makeJTextFieldLookLikeJLabel">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="removeRowHeader"></a>
# removeRowHeader
removeRowHeader( javax.swing.JTable table ) &rarr; void

Creates row header for table with row number (starting with 1) displayed

### Parameters:
table - a JTable

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=removeRowHeader&unscoped_q=removeRowHeader">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setRowHeader"></a>
# setRowHeader
setRowHeader( javax.swing.JTable table ) &rarr; void

Creates row header for table with row number (starting with 1) displayed

### Parameters:
table - a JTable

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setRowHeader&unscoped_q=setRowHeader">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

