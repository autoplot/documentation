# org.autoplot.dom.Plot

Represents a 2-D plot with an X and Y axis, and "Z" axis that is often hidden or
 implemented with a color bar.

# Plot( )


***
<a name="PROP_XAXIS"></a>
# PROP_XAXIS



***
<a name="PROP_YAXIS"></a>
# PROP_YAXIS



***
<a name="PROP_ZAXIS"></a>
# PROP_ZAXIS



***
<a name="PROP_TITLE"></a>
# PROP_TITLE

title for the plot.

***
<a name="PROP_FONTSIZE"></a>
# PROP_FONTSIZE



***
<a name="PROP_BACKGROUND"></a>
# PROP_BACKGROUND



***
<a name="PROP_DISPLAYTITLE"></a>
# PROP_DISPLAYTITLE



***
<a name="PROP_LEGENDPOSITION"></a>
# PROP_LEGENDPOSITION



***
<a name="PROP_DISPLAYLEGEND"></a>
# PROP_DISPLAYLEGEND



***
<a name="PROP_AUTOLABEL"></a>
# PROP_AUTOLABEL



***
<a name="PROP_VISIBLE"></a>
# PROP_VISIBLE

false indicates that the plot and its data will not
 be drawn.

***
<a name="PROP_AUTOBINDING"></a>
# PROP_AUTOBINDING

indicates the application is allowed to automatically create bindings to
 the plot, typically when it is first created.

***
<a name="PROP_ISOTROPIC"></a>
# PROP_ISOTROPIC



***
<a name="PROP_COLORTABLE"></a>
# PROP_COLORTABLE



***
<a name="PROP_ROWID"></a>
# PROP_ROWID



***
<a name="PROP_COLUMNID"></a>
# PROP_COLUMNID



***
<a name="PROP_CONTEXT"></a>
# PROP_CONTEXT



***
<a name="PROP_TICKS_URI"></a>
# PROP_TICKS_URI



***
<a name="childNodes"></a>
# childNodes
childNodes(  ) &rarr; List



### Returns:
java.util.List


<a href="https://github.com/autoplot/dev/search?q=childNodes&unscoped_q=childNodes">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="copy"></a>
# copy
copy(  ) &rarr; DomNode



### Returns:
org.autoplot.dom.DomNode


<a href="https://github.com/autoplot/dev/search?q=copy&unscoped_q=copy">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="diffs"></a>
# diffs
diffs( org.autoplot.dom.DomNode node ) &rarr; List



### Parameters:
node - a DomNode

### Returns:
java.util.List


<a href="https://github.com/autoplot/dev/search?q=diffs&unscoped_q=diffs">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getBackground"></a>
# getBackground
getBackground(  ) &rarr; Color



### Returns:
java.awt.Color


<a href="https://github.com/autoplot/dev/search?q=getBackground&unscoped_q=getBackground">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getColortable"></a>
# getColortable
getColortable(  ) &rarr; Type



### Returns:
org.das2.graph.DasColorBar.Type


<a href="https://github.com/autoplot/dev/search?q=getColortable&unscoped_q=getColortable">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getColumnId"></a>
# getColumnId
getColumnId(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getColumnId&unscoped_q=getColumnId">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getContext"></a>
# getContext
getContext(  ) &rarr; DatumRange



### Returns:
org.das2.datum.DatumRange


<a href="https://github.com/autoplot/dev/search?q=getContext&unscoped_q=getContext">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getController"></a>
# getController
getController(  ) &rarr; PlotController



### Returns:
org.autoplot.dom.PlotController


<a href="https://github.com/autoplot/dev/search?q=getController&unscoped_q=getController">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getFontSize"></a>
# getFontSize
getFontSize(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getFontSize&unscoped_q=getFontSize">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getLegendPosition"></a>
# getLegendPosition
getLegendPosition(  ) &rarr; LegendPosition



### Returns:
org.das2.graph.LegendPosition


<a href="https://github.com/autoplot/dev/search?q=getLegendPosition&unscoped_q=getLegendPosition">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getRowId"></a>
# getRowId
getRowId(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getRowId&unscoped_q=getRowId">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getTicksURI"></a>
# getTicksURI
getTicksURI(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getTicksURI&unscoped_q=getTicksURI">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getTitle"></a>
# getTitle
getTitle(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getTitle&unscoped_q=getTitle">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getXaxis"></a>
# getXaxis
getXaxis(  ) &rarr; Axis



### Returns:
org.autoplot.dom.Axis


<a href="https://github.com/autoplot/dev/search?q=getXaxis&unscoped_q=getXaxis">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getYaxis"></a>
# getYaxis
getYaxis(  ) &rarr; Axis



### Returns:
org.autoplot.dom.Axis


<a href="https://github.com/autoplot/dev/search?q=getYaxis&unscoped_q=getYaxis">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getZaxis"></a>
# getZaxis
getZaxis(  ) &rarr; Axis



### Returns:
org.autoplot.dom.Axis


<a href="https://github.com/autoplot/dev/search?q=getZaxis&unscoped_q=getZaxis">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isAutoBinding"></a>
# isAutoBinding
isAutoBinding(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isAutoBinding&unscoped_q=isAutoBinding">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isAutoLabel"></a>
# isAutoLabel
isAutoLabel(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isAutoLabel&unscoped_q=isAutoLabel">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isDisplayLegend"></a>
# isDisplayLegend
isDisplayLegend(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isDisplayLegend&unscoped_q=isDisplayLegend">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isDisplayTitle"></a>
# isDisplayTitle
isDisplayTitle(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isDisplayTitle&unscoped_q=isDisplayTitle">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isIsotropic"></a>
# isIsotropic
isIsotropic(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isIsotropic&unscoped_q=isIsotropic">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isVisible"></a>
# isVisible
isVisible(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isVisible&unscoped_q=isVisible">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setAutoBinding"></a>
# setAutoBinding
setAutoBinding( boolean autoBinding ) &rarr; void



### Parameters:
autoBinding - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setAutoBinding&unscoped_q=setAutoBinding">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setAutoLabel"></a>
# setAutoLabel
setAutoLabel( boolean autolabel ) &rarr; void



### Parameters:
autolabel - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setAutoLabel&unscoped_q=setAutoLabel">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setBackground"></a>
# setBackground
setBackground( java.awt.Color background ) &rarr; void

set the background color for the plot.  This is normally transparent, so
 the canvas color is used, and can be reset with Color(0,0,0,0).

### Parameters:
background - a Color

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setBackground&unscoped_q=setBackground">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setColortable"></a>
# setColortable
setColortable( org.das2.graph.DasColorBar.Type colortable ) &rarr; void



### Parameters:
colortable - a DasColorBar.Type

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setColortable&unscoped_q=setColortable">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setColumnId"></a>
# setColumnId
setColumnId( String columnId ) &rarr; void



### Parameters:
columnId - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setColumnId&unscoped_q=setColumnId">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setContext"></a>
# setContext
setContext( DatumRange context ) &rarr; void



### Parameters:
context - a DatumRange

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setContext&unscoped_q=setContext">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setDisplayLegend"></a>
# setDisplayLegend
setDisplayLegend( boolean displayLegend ) &rarr; void



### Parameters:
displayLegend - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setDisplayLegend&unscoped_q=setDisplayLegend">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setDisplayTitle"></a>
# setDisplayTitle
setDisplayTitle( boolean displayTitle ) &rarr; void



### Parameters:
displayTitle - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setDisplayTitle&unscoped_q=setDisplayTitle">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setFontSize"></a>
# setFontSize
setFontSize( String fontSize ) &rarr; void

set the font size relative to the canvas font size.  For example 
 "2em" will be twice the size.  "" is an alias for 1em.

### Parameters:
fontSize - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setFontSize&unscoped_q=setFontSize">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setIsotropic"></a>
# setIsotropic
setIsotropic( boolean isotropic ) &rarr; void



### Parameters:
isotropic - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setIsotropic&unscoped_q=setIsotropic">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setLegendPosition"></a>
# setLegendPosition
setLegendPosition( org.das2.graph.LegendPosition legendPosition ) &rarr; void



### Parameters:
legendPosition - a LegendPosition

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setLegendPosition&unscoped_q=setLegendPosition">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setRowId"></a>
# setRowId
setRowId( String rowId ) &rarr; void



### Parameters:
rowId - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setRowId&unscoped_q=setRowId">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setTicksURI"></a>
# setTicksURI
setTicksURI( String ticksURI ) &rarr; void



### Parameters:
ticksURI - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setTicksURI&unscoped_q=setTicksURI">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setTitle"></a>
# setTitle
setTitle( String title ) &rarr; void



### Parameters:
title - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setTitle&unscoped_q=setTitle">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setVisible"></a>
# setVisible
setVisible( boolean visible ) &rarr; void



### Parameters:
visible - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setVisible&unscoped_q=setVisible">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setXaxis"></a>
# setXaxis
setXaxis( org.autoplot.dom.Axis xaxis ) &rarr; void



### Parameters:
xaxis - an Axis

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setXaxis&unscoped_q=setXaxis">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setYaxis"></a>
# setYaxis
setYaxis( org.autoplot.dom.Axis yaxis ) &rarr; void



### Parameters:
yaxis - an Axis

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setYaxis&unscoped_q=setYaxis">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setZaxis"></a>
# setZaxis
setZaxis( org.autoplot.dom.Axis zaxis ) &rarr; void



### Parameters:
zaxis - an Axis

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setZaxis&unscoped_q=setZaxis">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="syncTo"></a>
# syncTo
syncTo( org.autoplot.dom.DomNode n ) &rarr; void



### Parameters:
n - a DomNode

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=syncTo&unscoped_q=syncTo">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

syncTo( org.autoplot.dom.DomNode n, java.util.List exclude ) &rarr; void<br>
