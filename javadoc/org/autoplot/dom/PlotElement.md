# org.autoplot.dom.PlotElement

Represents the method for painting data on to a plot, and filters that
 are applied to the data before plotting.

# PlotElement( )


***
<a name="PROP_DATASOURCEFILTERID"></a>
# PROP_DATASOURCEFILTERID



***
<a name="PROP_STYLE"></a>
# PROP_STYLE



***
<a name="PROP_PLOT_DEFAULTS"></a>
# PROP_PLOT_DEFAULTS



***
<a name="PROP_RENDERTYPE"></a>
# PROP_RENDERTYPE



***
<a name="PROP_RENDERCONTROL"></a>
# PROP_RENDERCONTROL



***
<a name="PROP_CADENCECHECK"></a>
# PROP_CADENCECHECK



***
<a name="PROP_PLOTID"></a>
# PROP_PLOTID



***
<a name="PROP_PARENT"></a>
# PROP_PARENT

id of this plotElement's parent, which groups the plotElements into one abstract
 plot.  The parent and children must share the same dataSourceFilter.

***
<a name="PROP_COMPONENT"></a>
# PROP_COMPONENT



***
<a name="PROP_LEGENDLABEL"></a>
# PROP_LEGENDLABEL



***
<a name="PROP_DISPLAYLEGEND"></a>
# PROP_DISPLAYLEGEND



***
<a name="PROP_AUTOLABEL"></a>
# PROP_AUTOLABEL

true indicates the axis label hasn't been changed manually and may/should be set automatically.

***
<a name="PROP_AUTORENDERTYPE"></a>
# PROP_AUTORENDERTYPE

true indicates that the renderType hasn't been changed manually and may/should be set automatically.

***
<a name="PROP_AUTOCOMPONENT"></a>
# PROP_AUTOCOMPONENT



***
<a name="PROP_ACTIVE"></a>
# PROP_ACTIVE



***
<a name="childNodes"></a>
# childNodes
childNodes(  ) &rarr; List



### Returns:
java.util.List


<a href="https://github.com/autoplot/dev/search?q=childNodes&unscoped_q=childNodes">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="clone"></a>
# clone
clone(  ) &rarr; Object



### Returns:
java.lang.Object


<a href="https://github.com/autoplot/dev/search?q=clone&unscoped_q=clone">[search for examples]</a>
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
<a name="getComponent"></a>
# getComponent
getComponent(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getComponent&unscoped_q=getComponent">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getController"></a>
# getController
getController(  ) &rarr; PlotElementController



### Returns:
org.autoplot.dom.PlotElementController


<a href="https://github.com/autoplot/dev/search?q=getController&unscoped_q=getController">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDataSourceFilterId"></a>
# getDataSourceFilterId
getDataSourceFilterId(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getDataSourceFilterId&unscoped_q=getDataSourceFilterId">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getLegendLabel"></a>
# getLegendLabel
getLegendLabel(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getLegendLabel&unscoped_q=getLegendLabel">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getParent"></a>
# getParent
getParent(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getParent&unscoped_q=getParent">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getPlotDefaults"></a>
# getPlotDefaults
getPlotDefaults(  ) &rarr; Plot



### Returns:
org.autoplot.dom.Plot


<a href="https://github.com/autoplot/dev/search?q=getPlotDefaults&unscoped_q=getPlotDefaults">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getPlotId"></a>
# getPlotId
getPlotId(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getPlotId&unscoped_q=getPlotId">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getRenderControl"></a>
# getRenderControl
getRenderControl(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getRenderControl&unscoped_q=getRenderControl">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getRenderType"></a>
# getRenderType
getRenderType(  ) &rarr; RenderType



### Returns:
org.autoplot.RenderType


<a href="https://github.com/autoplot/dev/search?q=getRenderType&unscoped_q=getRenderType">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getStyle"></a>
# getStyle
getStyle(  ) &rarr; PlotElementStyle



### Returns:
org.autoplot.dom.PlotElementStyle


<a href="https://github.com/autoplot/dev/search?q=getStyle&unscoped_q=getStyle">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isActive"></a>
# isActive
isActive(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isActive&unscoped_q=isActive">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isAutoComponent"></a>
# isAutoComponent
isAutoComponent(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isAutoComponent&unscoped_q=isAutoComponent">[search for examples]</a>
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
<a name="isAutoRenderType"></a>
# isAutoRenderType
isAutoRenderType(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isAutoRenderType&unscoped_q=isAutoRenderType">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isCadenceCheck"></a>
# isCadenceCheck
isCadenceCheck(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isCadenceCheck&unscoped_q=isCadenceCheck">[search for examples]</a>
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
<a name="setActive"></a>
# setActive
setActive( boolean active ) &rarr; void



### Parameters:
active - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setActive&unscoped_q=setActive">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setAutoComponent"></a>
# setAutoComponent
setAutoComponent( boolean autoComponent ) &rarr; void



### Parameters:
autoComponent - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setAutoComponent&unscoped_q=setAutoComponent">[search for examples]</a>
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
<a name="setAutoRenderType"></a>
# setAutoRenderType
setAutoRenderType( boolean autoRenderType ) &rarr; void



### Parameters:
autoRenderType - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setAutoRenderType&unscoped_q=setAutoRenderType">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setCadenceCheck"></a>
# setCadenceCheck
setCadenceCheck( boolean cadenceCheck ) &rarr; void



### Parameters:
cadenceCheck - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setCadenceCheck&unscoped_q=setCadenceCheck">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setComponent"></a>
# setComponent
setComponent( String component ) &rarr; void



### Parameters:
component - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setComponent&unscoped_q=setComponent">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setComponentAutomatically"></a>
# setComponentAutomatically
setComponentAutomatically( String component ) &rarr; void

Set the property, and also set the autoComponent property.  Note setComponent will clear the property.
 TODO: this should probably be in the controller.

### Parameters:
component - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setComponentAutomatically&unscoped_q=setComponentAutomatically">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setDataSourceFilterId"></a>
# setDataSourceFilterId
setDataSourceFilterId( String dataSourceFilterId ) &rarr; void



### Parameters:
dataSourceFilterId - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setDataSourceFilterId&unscoped_q=setDataSourceFilterId">[search for examples]</a>
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
<a name="setLegendLabel"></a>
# setLegendLabel
setLegendLabel( String legendLabel ) &rarr; void



### Parameters:
legendLabel - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setLegendLabel&unscoped_q=setLegendLabel">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setLegendLabelAutomatically"></a>
# setLegendLabelAutomatically
setLegendLabelAutomatically( String legendLabel ) &rarr; void



### Parameters:
legendLabel - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setLegendLabelAutomatically&unscoped_q=setLegendLabelAutomatically">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setParent"></a>
# setParent
setParent( String parent ) &rarr; void



### Parameters:
parent - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setParent&unscoped_q=setParent">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setPlotDefaults"></a>
# setPlotDefaults
setPlotDefaults( org.autoplot.dom.Plot plot ) &rarr; void



### Parameters:
plot - a Plot

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setPlotDefaults&unscoped_q=setPlotDefaults">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setPlotId"></a>
# setPlotId
setPlotId( String plotId ) &rarr; void



### Parameters:
plotId - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setPlotId&unscoped_q=setPlotId">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setRenderControl"></a>
# setRenderControl
setRenderControl( String renderUri ) &rarr; void



### Parameters:
renderUri - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setRenderControl&unscoped_q=setRenderControl">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setRenderType"></a>
# setRenderType
setRenderType( org.autoplot.RenderType renderType ) &rarr; void



### Parameters:
renderType - a RenderType

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setRenderType&unscoped_q=setRenderType">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setRenderTypeAutomatically"></a>
# setRenderTypeAutomatically
setRenderTypeAutomatically( org.autoplot.RenderType renderType ) &rarr; void



### Parameters:
renderType - a RenderType

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setRenderTypeAutomatically&unscoped_q=setRenderTypeAutomatically">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setStyle"></a>
# setStyle
setStyle( org.autoplot.dom.PlotElementStyle style ) &rarr; void



### Parameters:
style - a PlotElementStyle

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setStyle&unscoped_q=setStyle">[search for examples]</a>
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

syncTo( org.autoplot.dom.DomNode node, java.util.List exclude ) &rarr; void<br>
***
<a name="toString"></a>
# toString
toString(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=toString&unscoped_q=toString">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

