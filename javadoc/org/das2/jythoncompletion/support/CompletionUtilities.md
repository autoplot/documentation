# org.das2.jythoncompletion.support.CompletionUtilities

Various code completion utilities including completion item
 contents rendering.

***
<a name="getPreferredWidth"></a>
# getPreferredWidth
getPreferredWidth( String leftHtmlText, String rightHtmlText, java.awt.Graphics g, java.awt.Font defaultFont ) &rarr; int

Get preferred width of the item by knowing its left and right html texts.
 <br/>
 It is supposed that the item will have an icon 16x16 and an appropriate
 space is reserved for it.

### Parameters:
leftHtmlText - html text displayed on the left side of the item
  next to the icon. It may be null which means no left text will be displayed.
<br>rightHtmlText - html text aligned on the right edge of the item's
  rendering area. It may be null which means no right text will be displayed.
<br>g - a Graphics
<br>defaultFont - a Font

### Returns:
&gt;=0 preferred rendering width of the item.

<a href="https://github.com/autoplot/dev/search?q=getPreferredWidth&unscoped_q=getPreferredWidth">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="renderHtml"></a>
# renderHtml
renderHtml( javax.swing.ImageIcon icon, String leftHtmlText, String rightHtmlText, java.awt.Graphics g, java.awt.Font defaultFont, java.awt.Color defaultColor, int width, int height, boolean selected ) &rarr; void

Render a completion item using the provided icon and left and right
 html texts.

### Parameters:
icon - icon 16x16 that will be displayed on the left. It may be null
  which means that no icon will be displayed but the space for the icon
  will still be reserved (to properly align with other items
  that will provide an icon).
<br>leftHtmlText - html text that will be displayed on the left side
  of the item's rendering area next to the icon.
  <br/>
  It may be null which indicates that no left text will be displayed.
  <br/>
  If there's not enough horizontal space in the rendering area
  the text will be shrinked and "..." will be displayed at the end.
<br>rightHtmlText - html text that will be aligned to the right edge
  of the item's rendering area.
  <br/>
  It may be null which means that no right text will be displayed.
  <br/>
  The right text is always attempted to be fully displayed unlike
  the left text that may be shrinked if there's not enough rendering space
  in the horizontal direction.
  <br/>
  If there's not enough space even for the right text it will be shrinked
  and "..." will be displayed at the end of the rendered string.
<br>g - non-null graphics through which the rendering happens.
<br>defaultFont - non-null default font to be used for rendering.
<br>defaultColor - non-null default color to be used for rendering.
<br>width - &gt;=0 available width for rendering.
<br>height - &gt;=0 available height for rendering.
<br>selected - whether the item being rendered is currently selected
  in the completion's JList. If selected the foreground color is forced
  to be black for all parts of the rendered strings.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=renderHtml&unscoped_q=renderHtml">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

