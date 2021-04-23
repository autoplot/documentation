# org.autoplot.help.AutoplotHelpViewer

<p>Extends the BasicContentViewerUI to allow the use of external links in
 the JavaHelp html.  Any link with an explicitly specified protocol of <code>http</code>,
 <code>ftp</code>, or <code>mailto</code> will be opened in the desktop
 default application.</p>

 <p>This class never need be instantiated directly; the JavaHelp system is told
 to use it as the viewer.</p>

# AutoplotHelpViewer( JHelpContentViewer x )


***
<a name="createUI"></a>
# createUI
createUI( javax.swing.JComponent x ) &rarr; ComponentUI



### Parameters:
x - a JComponent

### Returns:
javax.swing.plaf.ComponentUI


<a href="https://github.com/autoplot/dev/search?q=createUI&unscoped_q=createUI">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="hyperlinkUpdate"></a>
# hyperlinkUpdate
hyperlinkUpdate( javax.swing.event.HyperlinkEvent he ) &rarr; void



### Parameters:
he - a HyperlinkEvent

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=hyperlinkUpdate&unscoped_q=hyperlinkUpdate">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

