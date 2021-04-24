# org.das2.graph.Auralizor

Stream QDataSet to the sound system, using DEPEND_0 to control
 sampling rate.  Note this does not support the new waveform packet 
 scheme introduced a few years ago, and can easily be made to support 
 it.

# Auralizor( QDataSet ds )
create an Auralizor for rendering the dataset to the sound system.

***
<a name="PROP_POSITION"></a>
# PROP_POSITION



***
<a name="PROP_SCALE"></a>
# PROP_SCALE



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

addPropertyChangeListener( String propname, java.beans.PropertyChangeListener listener ) &rarr; void<br>
***
<a name="getControlPanel"></a>
# getControlPanel
getControlPanel(  ) &rarr; JPanel



### Returns:
javax.swing.JPanel


<a href="https://github.com/autoplot/dev/search?q=getControlPanel&unscoped_q=getControlPanel">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getPosition"></a>
# getPosition
getPosition(  ) &rarr; Datum



### Returns:
org.das2.datum.Datum


<a href="https://github.com/autoplot/dev/search?q=getPosition&unscoped_q=getPosition">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="isScale"></a>
# isScale
isScale(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isScale&unscoped_q=isScale">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="playSound"></a>
# playSound
playSound(  ) &rarr; void

begin streaming the sound.  This will block the current
 thread until complete.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=playSound&unscoped_q=playSound">[search for examples]</a>
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

removePropertyChangeListener( String propname, java.beans.PropertyChangeListener listener ) &rarr; void<br>
***
<a name="reset"></a>
# reset
reset(  ) &rarr; void



### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=reset&unscoped_q=reset">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setDataSet"></a>
# setDataSet
setDataSet( QDataSet ds ) &rarr; void

set the dataset to stream.  The dataset should be 
 rank 1 or a rank 2 waveform, and have DEPEND_0 which is convertible
 to seconds or be a time location unit.

### Parameters:
ds - the rank 1 dataset with DEPEND_0 convertible to seconds or be a time location unit, or rank 2 waveform.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setDataSet&unscoped_q=setDataSet">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setPosition"></a>
# setPosition
setPosition( Datum position ) &rarr; void



### Parameters:
position - a Datum

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setPosition&unscoped_q=setPosition">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setScale"></a>
# setScale
setScale( boolean scale ) &rarr; void



### Parameters:
scale - a boolean

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setScale&unscoped_q=setScale">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

