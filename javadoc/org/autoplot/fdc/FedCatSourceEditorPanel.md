# org.autoplot.fdc.FedCatSourceEditorPanel
FedCatSourceEditorPanel( )
Creates new form FedCatSourceEditorPanel

***
<a name="getPanel"></a>
# getPanel
getPanel(  ) &rarr; JPanel



### Returns:
javax.swing.JPanel


<a href="https://github.com/autoplot/dev/search?q=getPanel&unscoped_q=getPanel">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getURI"></a>
# getURI
getURI(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getURI&unscoped_q=getURI">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="markProblems"></a>
# markProblems
markProblems( java.util.List problems ) &rarr; void



### Parameters:
problems - a java.util.List

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=markProblems&unscoped_q=markProblems">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="prepare"></a>
# prepare
prepare( String sFullUri, java.awt.Window parent, ProgressMonitor mon ) &rarr; boolean

Gather any node definitions that will be needed for the dialog box
 
 URI examples that we may have to edit:
 
   vap+dc:tag:das2.org,2012:test:/swri/mars_express/aspera3/els?radius=2,3
   vap+dc:site:/uiowa/juno/survey/wav/das2?band=LFRL&time=2017-01-01,2017-01-02,60
   vap+dc:http://random.site.edu/~person/mysource.json?some_key=some_value

### Parameters:
sFullUri - The full Autoplot URI, examples above
<br>parent - The window parent, in case we need to pop a dlg with a cancel button
<br>mon - A progress monitor

### Returns:
true, since at present there is no way to cancel

<a href="https://github.com/autoplot/dev/search?q=prepare&unscoped_q=prepare">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="reject"></a>
# reject
reject( String sFullUri ) &rarr; boolean



### Parameters:
sFullUri - a String

### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=reject&unscoped_q=reject">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setURI"></a>
# setURI
setURI( String sFullUri ) &rarr; void

Provides a starting full URI to the editor and trigger a runnable to show the
 editor GUI.
 
 In general both the catalog panel and the source options panel are displayed
 together, however if this is a standalone root of type source, that has no 
 parents, then only the source controls are displayed

### Parameters:
sFullUri - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setURI&unscoped_q=setURI">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

