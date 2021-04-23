# org.das2.graph.GrannyTickLabeller

TickLabeller based on the formatting and bounding-box capabilities of the
 GrannyTextRenderer.  This class by default creates a DatumFormatter for
 the tickDescriptor it receives, and then uses the grannyFormat method to
 get the label.  This object is useful as-is, but provides an easy way to
 get complex labels (e.g. TCAs) by overriding init and getLabel.

# GrannyTickLabeller( )


***
<a name="PROP_FORMATTER"></a>
# PROP_FORMATTER



***
<a name="addPropertyChangeListener"></a>
# addPropertyChangeListener
addPropertyChangeListener( java.beans.PropertyChangeListener listener ) &rarr; void



### Parameters:
listener - a PropertyChangeListener

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=addPropertyChangeListener&unscoped_q=addPropertyChangeListener">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="finished"></a>
# finished
finished(  ) &rarr; void



### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=finished&unscoped_q=finished">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getFormatter"></a>
# getFormatter
getFormatter(  ) &rarr; DatumFormatter

the formatter.

### Returns:
the formatter

<a href="https://github.com/autoplot/dev/search?q=getFormatter&unscoped_q=getFormatter">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="init"></a>
# init
init( org.das2.graph.TickVDescriptor ticks ) &rarr; void

sets the ticks and DatumFormatter before drawing.

### Parameters:
ticks - a TickVDescriptor

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=init&unscoped_q=init">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="labelMajorTick"></a>
# labelMajorTick
labelMajorTick( java.awt.Graphics g, int tickNumber, java.awt.geom.Line2D tickLine ) &rarr; Rectangle



### Parameters:
g - a Graphics
<br>tickNumber - an int
<br>tickLine - a Line2D

### Returns:
java.awt.Rectangle


<a href="https://github.com/autoplot/dev/search?q=labelMajorTick&unscoped_q=labelMajorTick">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="removePropertyChangeListener"></a>
# removePropertyChangeListener
removePropertyChangeListener( java.beans.PropertyChangeListener listener ) &rarr; void



### Parameters:
listener - a PropertyChangeListener

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=removePropertyChangeListener&unscoped_q=removePropertyChangeListener">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setFormatter"></a>
# setFormatter
setFormatter( org.das2.datum.format.DatumFormatter df ) &rarr; void

override the formatter in the TickVDescriptor.

### Parameters:
df - the formatter to use

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setFormatter&unscoped_q=setFormatter">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

