# org.autoplot.dom.Options

Bean for holding AP configuration options.  Note there are a few AutoplotUI prefs here that shouldn't be.

# Options( )


***
<a name="PROP_COLOR"></a>
# PROP_COLOR



***
<a name="PROP_FILLCOLOR"></a>
# PROP_FILLCOLOR



***
<a name="VALUE_AUTORANGE_TYPE_RELUCTANT"></a>
# VALUE_AUTORANGE_TYPE_RELUCTANT

try to recycle old axis settings.  If the new range is near the 
 old range, then just use the old range.

***
<a name="PROP_SCRIPTVISIBLE"></a>
# PROP_SCRIPTVISIBLE



***
<a name="PROP_LOGCONSOLEVISIBLE"></a>
# PROP_LOGCONSOLEVISIBLE



***
<a name="PROP_DATAVISIBLE"></a>
# PROP_DATAVISIBLE

true when the data tab is visible.

***
<a name="PROP_LAYOUTVISIBLE"></a>
# PROP_LAYOUTVISIBLE

true when the layout tab is visible.

***
<a name="PROP_SERVERENABLED"></a>
# PROP_SERVERENABLED



***
<a name="PROP_CANVASFONT"></a>
# PROP_CANVASFONT



***
<a name="PROP_WIDTH"></a>
# PROP_WIDTH



***
<a name="PROP_HEIGHT"></a>
# PROP_HEIGHT



***
<a name="PROP_FOREGROUND"></a>
# PROP_FOREGROUND



***
<a name="PROP_BACKGROUND"></a>
# PROP_BACKGROUND



***
<a name="PROP_COLORTABLE"></a>
# PROP_COLORTABLE



***
<a name="PROP_OPPOSITEAXISVISIBLE"></a>
# PROP_OPPOSITEAXISVISIBLE



***
<a name="PROP_TICKLEN"></a>
# PROP_TICKLEN



***
<a name="PROP_LINE_THICKNESS"></a>
# PROP_LINE_THICKNESS



***
<a name="PROP_MULTILINETEXTALIGNMENT"></a>
# PROP_MULTILINETEXTALIGNMENT



***
<a name="PROP_FLIPCOLORBARLABEL"></a>
# PROP_FLIPCOLORBARLABEL



***
<a name="PROP_SPECIALEFFECTS"></a>
# PROP_SPECIALEFFECTS

property specialEffects
 enables/disables things like animated axes, etc.

***
<a name="PROP_DRAWANTIALIAS"></a>
# PROP_DRAWANTIALIAS



***
<a name="PROP_TEXTANTIALIAS"></a>
# PROP_TEXTANTIALIAS



***
<a name="PROP_DRAWGRID"></a>
# PROP_DRAWGRID



***
<a name="PROP_DRAWMINORGRID"></a>
# PROP_DRAWMINORGRID



***
<a name="PROP_OVERRENDERING"></a>
# PROP_OVERRENDERING

overRendering is a hint to the plots that the data outside the visible axis bounds should be rendered
 so that operations like pan are more fluid.

***
<a name="PROP_AUTORANGING"></a>
# PROP_AUTORANGING



***
<a name="PROP_AUTORANGETYPE"></a>
# PROP_AUTORANGETYPE



***
<a name="PROP_AUTOLABELLING"></a>
# PROP_AUTOLABELLING



***
<a name="PROP_AUTOLAYOUT"></a>
# PROP_AUTOLAYOUT



***
<a name="PROP_DAY_OF_YEAR"></a>
# PROP_DAY_OF_YEAR



***
<a name="PROP_USE_TIME_RANGE_EDITOR"></a>
# PROP_USE_TIME_RANGE_EDITOR

Use time range editor instead of Data Set Selector.

***
<a name="PROP_NEARESTNEIGHBOR"></a>
# PROP_NEARESTNEIGHBOR



***
<a name="PROP_MOUSEMODULE"></a>
# PROP_MOUSEMODULE



***
<a name="PROP_SLICEREBINNEDDATA"></a>
# PROP_SLICEREBINNEDDATA



***
<a name="PROP_PRINTINGTAG"></a>
# PROP_PRINTINGTAG



***
<a name="PROP_PRINTINGLOGLEVEL"></a>
# PROP_PRINTINGLOGLEVEL



***
<a name="PROP_DISPLAYLOGLEVEL"></a>
# PROP_DISPLAYLOGLEVEL



***
<a name="PROP_LOGMESSAGETIMEOUTSEC"></a>
# PROP_LOGMESSAGETIMEOUTSEC



***
<a name="PROP_SCANENABLED"></a>
# PROP_SCANENABLED



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
<a name="getAutorangeType"></a>
# getAutorangeType
getAutorangeType(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getAutorangeType&unscoped_q=getAutorangeType">[search for examples]</a>
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
<a name="getCanvasFont"></a>
# getCanvasFont
getCanvasFont(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getCanvasFont&unscoped_q=getCanvasFont">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getColor"></a>
# getColor
getColor(  ) &rarr; Color

Getter for property color.

### Returns:
Value of property color.

<a href="https://github.com/autoplot/dev/search?q=getColor&unscoped_q=getColor">[search for examples]</a>
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
<a name="getController"></a>
# getController
getController(  ) &rarr; OptionsPrefsController



### Returns:
org.autoplot.dom.OptionsPrefsController


<a href="https://github.com/autoplot/dev/search?q=getController&unscoped_q=getController">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getDisplayLogLevel"></a>
# getDisplayLogLevel
getDisplayLogLevel(  ) &rarr; Level



### Returns:
java.util.logging.Level


<a href="https://github.com/autoplot/dev/search?q=getDisplayLogLevel&unscoped_q=getDisplayLogLevel">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getFillColor"></a>
# getFillColor
getFillColor(  ) &rarr; Color

Getter for property fillColor.

### Returns:
Value of property fillColor.

<a href="https://github.com/autoplot/dev/search?q=getFillColor&unscoped_q=getFillColor">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getForeground"></a>
# getForeground
getForeground(  ) &rarr; Color



### Returns:
java.awt.Color


<a href="https://github.com/autoplot/dev/search?q=getForeground&unscoped_q=getForeground">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getHeight"></a>
# getHeight
getHeight(  ) &rarr; int



### Returns:
int


<a href="https://github.com/autoplot/dev/search?q=getHeight&unscoped_q=getHeight">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getLineThickness"></a>
# getLineThickness
getLineThickness(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getLineThickness&unscoped_q=getLineThickness">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getLogMessageTimeoutSec"></a>
# getLogMessageTimeoutSec
getLogMessageTimeoutSec(  ) &rarr; int



### Returns:
int


<a href="https://github.com/autoplot/dev/search?q=getLogMessageTimeoutSec&unscoped_q=getLogMessageTimeoutSec">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getMouseModule"></a>
# getMouseModule
getMouseModule(  ) &rarr; MouseModuleType



### Returns:
org.autoplot.MouseModuleType


<a href="https://github.com/autoplot/dev/search?q=getMouseModule&unscoped_q=getMouseModule">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getMultiLineTextAlignment"></a>
# getMultiLineTextAlignment
getMultiLineTextAlignment(  ) &rarr; float



### Returns:
float


<a href="https://github.com/autoplot/dev/search?q=getMultiLineTextAlignment&unscoped_q=getMultiLineTextAlignment">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getPrintingLogLevel"></a>
# getPrintingLogLevel
getPrintingLogLevel(  ) &rarr; Level



### Returns:
java.util.logging.Level


<a href="https://github.com/autoplot/dev/search?q=getPrintingLogLevel&unscoped_q=getPrintingLogLevel">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getPrintingTag"></a>
# getPrintingTag
getPrintingTag(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getPrintingTag&unscoped_q=getPrintingTag">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getTicklen"></a>
# getTicklen
getTicklen(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=getTicklen&unscoped_q=getTicklen">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getWidth"></a>
# getWidth
getWidth(  ) &rarr; int



### Returns:
int


<a href="https://github.com/autoplot/dev/search?q=getWidth&unscoped_q=getWidth">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isAutolabelling"></a>
# isAutolabelling
isAutolabelling(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isAutolabelling&unscoped_q=isAutolabelling">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isAutolayout"></a>
# isAutolayout
isAutolayout(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isAutolayout&unscoped_q=isAutolayout">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isAutoranging"></a>
# isAutoranging
isAutoranging(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isAutoranging&unscoped_q=isAutoranging">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isDataVisible"></a>
# isDataVisible
isDataVisible(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isDataVisible&unscoped_q=isDataVisible">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isDayOfYear"></a>
# isDayOfYear
isDayOfYear(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isDayOfYear&unscoped_q=isDayOfYear">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isDrawAntiAlias"></a>
# isDrawAntiAlias
isDrawAntiAlias(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isDrawAntiAlias&unscoped_q=isDrawAntiAlias">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isDrawGrid"></a>
# isDrawGrid
isDrawGrid(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isDrawGrid&unscoped_q=isDrawGrid">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isDrawMinorGrid"></a>
# isDrawMinorGrid
isDrawMinorGrid(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isDrawMinorGrid&unscoped_q=isDrawMinorGrid">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isFlipColorbarLabel"></a>
# isFlipColorbarLabel
isFlipColorbarLabel(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isFlipColorbarLabel&unscoped_q=isFlipColorbarLabel">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isLayoutVisible"></a>
# isLayoutVisible
isLayoutVisible(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isLayoutVisible&unscoped_q=isLayoutVisible">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isLogConsoleVisible"></a>
# isLogConsoleVisible
isLogConsoleVisible(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isLogConsoleVisible&unscoped_q=isLogConsoleVisible">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isNearestNeighbor"></a>
# isNearestNeighbor
isNearestNeighbor(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isNearestNeighbor&unscoped_q=isNearestNeighbor">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isOppositeAxisVisible"></a>
# isOppositeAxisVisible
isOppositeAxisVisible(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isOppositeAxisVisible&unscoped_q=isOppositeAxisVisible">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isOverRendering"></a>
# isOverRendering
isOverRendering(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isOverRendering&unscoped_q=isOverRendering">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isScanEnabled"></a>
# isScanEnabled
isScanEnabled(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isScanEnabled&unscoped_q=isScanEnabled">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isScriptVisible"></a>
# isScriptVisible
isScriptVisible(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isScriptVisible&unscoped_q=isScriptVisible">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isServerEnabled"></a>
# isServerEnabled
isServerEnabled(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isServerEnabled&unscoped_q=isServerEnabled">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isSliceRebinnedData"></a>
# isSliceRebinnedData
isSliceRebinnedData(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isSliceRebinnedData&unscoped_q=isSliceRebinnedData">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isSpecialEffects"></a>
# isSpecialEffects
isSpecialEffects(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isSpecialEffects&unscoped_q=isSpecialEffects">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isTextAntiAlias"></a>
# isTextAntiAlias
isTextAntiAlias(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isTextAntiAlias&unscoped_q=isTextAntiAlias">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isUseTimeRangeEditor"></a>
# isUseTimeRangeEditor
isUseTimeRangeEditor(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isUseTimeRangeEditor&unscoped_q=isUseTimeRangeEditor">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setAutolabelling"></a>
# setAutolabelling
setAutolabelling( boolean autolabelling ) &rarr; void



### Parameters:
autolabelling - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setAutolabelling&unscoped_q=setAutolabelling">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setAutolayout"></a>
# setAutolayout
setAutolayout( boolean autolayout ) &rarr; void



### Parameters:
autolayout - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setAutolayout&unscoped_q=setAutolayout">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setAutorangeType"></a>
# setAutorangeType
setAutorangeType( String autorangeType ) &rarr; void



### Parameters:
autorangeType - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setAutorangeType&unscoped_q=setAutorangeType">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setAutoranging"></a>
# setAutoranging
setAutoranging( boolean newautoranging ) &rarr; void



### Parameters:
newautoranging - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setAutoranging&unscoped_q=setAutoranging">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setBackground"></a>
# setBackground
setBackground( java.awt.Color background ) &rarr; void



### Parameters:
background - a Color

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setBackground&unscoped_q=setBackground">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setCanvasFont"></a>
# setCanvasFont
setCanvasFont( String canvasFont ) &rarr; void



### Parameters:
canvasFont - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setCanvasFont&unscoped_q=setCanvasFont">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setColor"></a>
# setColor
setColor( java.awt.Color color ) &rarr; void

Setter for property color.

### Parameters:
color - New value of property color.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setColor&unscoped_q=setColor">[search for examples]</a>
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
<a name="setDataVisible"></a>
# setDataVisible
setDataVisible( boolean dataVisible ) &rarr; void



### Parameters:
dataVisible - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setDataVisible&unscoped_q=setDataVisible">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setDayOfYear"></a>
# setDayOfYear
setDayOfYear( boolean dayOfYear ) &rarr; void



### Parameters:
dayOfYear - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setDayOfYear&unscoped_q=setDayOfYear">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setDisplayLogLevel"></a>
# setDisplayLogLevel
setDisplayLogLevel( java.util.logging.Level displayLogLevel ) &rarr; void



### Parameters:
displayLogLevel - a Level

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setDisplayLogLevel&unscoped_q=setDisplayLogLevel">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setDrawAntiAlias"></a>
# setDrawAntiAlias
setDrawAntiAlias( boolean drawAntiAlias ) &rarr; void



### Parameters:
drawAntiAlias - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setDrawAntiAlias&unscoped_q=setDrawAntiAlias">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setDrawGrid"></a>
# setDrawGrid
setDrawGrid( boolean drawGrid ) &rarr; void



### Parameters:
drawGrid - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setDrawGrid&unscoped_q=setDrawGrid">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setDrawMinorGrid"></a>
# setDrawMinorGrid
setDrawMinorGrid( boolean drawMinorGrid ) &rarr; void



### Parameters:
drawMinorGrid - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setDrawMinorGrid&unscoped_q=setDrawMinorGrid">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setFillColor"></a>
# setFillColor
setFillColor( java.awt.Color fillColor ) &rarr; void

Setter for property fillColor.

### Parameters:
fillColor - New value of property fillColor.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setFillColor&unscoped_q=setFillColor">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setFlipColorbarLabel"></a>
# setFlipColorbarLabel
setFlipColorbarLabel( boolean flipColorbarLabel ) &rarr; void



### Parameters:
flipColorbarLabel - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setFlipColorbarLabel&unscoped_q=setFlipColorbarLabel">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setForeground"></a>
# setForeground
setForeground( java.awt.Color foreground ) &rarr; void



### Parameters:
foreground - a Color

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setForeground&unscoped_q=setForeground">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setHeight"></a>
# setHeight
setHeight( int height ) &rarr; void

set the initial height of the canvases in pixels

### Parameters:
height - an int

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setHeight&unscoped_q=setHeight">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setLayoutVisible"></a>
# setLayoutVisible
setLayoutVisible( boolean layoutVisible ) &rarr; void



### Parameters:
layoutVisible - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setLayoutVisible&unscoped_q=setLayoutVisible">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setLineThickness"></a>
# setLineThickness
setLineThickness( String lineThickness ) &rarr; void

lineThickness is the thickness of axes and ticks.

### Parameters:
lineThickness - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setLineThickness&unscoped_q=setLineThickness">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setLogConsoleVisible"></a>
# setLogConsoleVisible
setLogConsoleVisible( boolean logConsoleVisible ) &rarr; void



### Parameters:
logConsoleVisible - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setLogConsoleVisible&unscoped_q=setLogConsoleVisible">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setLogMessageTimeoutSec"></a>
# setLogMessageTimeoutSec
setLogMessageTimeoutSec( int logMessageTimeoutSec ) &rarr; void



### Parameters:
logMessageTimeoutSec - an int

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setLogMessageTimeoutSec&unscoped_q=setLogMessageTimeoutSec">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setMouseModule"></a>
# setMouseModule
setMouseModule( org.autoplot.MouseModuleType mouseModule ) &rarr; void



### Parameters:
mouseModule - a MouseModuleType

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setMouseModule&unscoped_q=setMouseModule">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setMultiLineTextAlignment"></a>
# setMultiLineTextAlignment
setMultiLineTextAlignment( float multiLineTextAlignment ) &rarr; void



### Parameters:
multiLineTextAlignment - a float

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setMultiLineTextAlignment&unscoped_q=setMultiLineTextAlignment">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setNearestNeighbor"></a>
# setNearestNeighbor
setNearestNeighbor( boolean nearestNeighbor ) &rarr; void



### Parameters:
nearestNeighbor - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setNearestNeighbor&unscoped_q=setNearestNeighbor">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setOppositeAxisVisible"></a>
# setOppositeAxisVisible
setOppositeAxisVisible( boolean oppositeAxisVisible ) &rarr; void



### Parameters:
oppositeAxisVisible - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setOppositeAxisVisible&unscoped_q=setOppositeAxisVisible">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setOverRendering"></a>
# setOverRendering
setOverRendering( boolean overRendering ) &rarr; void



### Parameters:
overRendering - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setOverRendering&unscoped_q=setOverRendering">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setPrintingLogLevel"></a>
# setPrintingLogLevel
setPrintingLogLevel( java.util.logging.Level printingLogLevel ) &rarr; void



### Parameters:
printingLogLevel - a Level

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setPrintingLogLevel&unscoped_q=setPrintingLogLevel">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setPrintingTag"></a>
# setPrintingTag
setPrintingTag( String printingTag ) &rarr; void



### Parameters:
printingTag - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setPrintingTag&unscoped_q=setPrintingTag">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setScanEnabled"></a>
# setScanEnabled
setScanEnabled( boolean scanEnabled ) &rarr; void



### Parameters:
scanEnabled - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setScanEnabled&unscoped_q=setScanEnabled">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setScriptVisible"></a>
# setScriptVisible
setScriptVisible( boolean scriptVisible ) &rarr; void



### Parameters:
scriptVisible - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setScriptVisible&unscoped_q=setScriptVisible">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setServerEnabled"></a>
# setServerEnabled
setServerEnabled( boolean serverEnabled ) &rarr; void



### Parameters:
serverEnabled - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setServerEnabled&unscoped_q=setServerEnabled">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setSliceRebinnedData"></a>
# setSliceRebinnedData
setSliceRebinnedData( boolean sliceRebinnedData ) &rarr; void



### Parameters:
sliceRebinnedData - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setSliceRebinnedData&unscoped_q=setSliceRebinnedData">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setSpecialEffects"></a>
# setSpecialEffects
setSpecialEffects( boolean specialEffects ) &rarr; void



### Parameters:
specialEffects - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setSpecialEffects&unscoped_q=setSpecialEffects">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setTextAntiAlias"></a>
# setTextAntiAlias
setTextAntiAlias( boolean textAntiAlias ) &rarr; void



### Parameters:
textAntiAlias - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setTextAntiAlias&unscoped_q=setTextAntiAlias">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setTicklen"></a>
# setTicklen
setTicklen( String ticklen ) &rarr; void



### Parameters:
ticklen - a String

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setTicklen&unscoped_q=setTicklen">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setUseTimeRangeEditor"></a>
# setUseTimeRangeEditor
setUseTimeRangeEditor( boolean useTimeRangeEditor ) &rarr; void



### Parameters:
useTimeRangeEditor - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setUseTimeRangeEditor&unscoped_q=setUseTimeRangeEditor">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setWidth"></a>
# setWidth
setWidth( int width ) &rarr; void

set the initial width of the canvases in pixels

### Parameters:
width - an int

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setWidth&unscoped_q=setWidth">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="syncTo"></a>
# syncTo
syncTo( org.autoplot.dom.DomNode n, java.util.List exclude ) &rarr; void

synchronizes to another node, except unlike other nodes where this is
 thorough by default, this is the minimal set of properties that 
 will provide a usable display.  These include the colors and the fonts,
 and the timeRange editor mode, flip colorbar label, the ticklen, and last
 scanEnabled.

### Parameters:
n - the node
<br>exclude - the properties to exclude.

### Returns:
void (returns nothing)

### See Also:
<a href='https://sourceforge.net/p/autoplot/bugs/2175/'>https://sourceforge.net/p/autoplot/bugs/2175/</a> <br>

<a href="https://github.com/autoplot/dev/search?q=syncTo&unscoped_q=syncTo">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

syncTo( org.autoplot.dom.DomNode n ) &rarr; void<br>
***
<a name="syncToAll"></a>
# syncToAll
syncToAll( org.autoplot.dom.DomNode n, java.util.List exclude ) &rarr; void

synchronizes any property having to do with the appearance of the
 plot.  This includes user preferences like the axis grid, and also performance
 switches which may have a minor effect on appearance such as overrendering.
 This was introduced to support createPngWalk, which should have an appearance
 as close as possible to the vap.

### Parameters:
n - the node
<br>exclude - the properties to exclude.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=syncToAll&unscoped_q=syncToAll">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

