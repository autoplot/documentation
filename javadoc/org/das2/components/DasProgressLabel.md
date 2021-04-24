# org.das2.components.DasProgressLabel

One-line Label component prints the update progress to a
 JLabel component.  This is either created by the client and set with 
 setLabelComponent, or this class will also create one with getLabelComponent.

# DasProgressLabel( String taskLabel )
create the DasProgessLabel with the given label for the task.

***
<a name="finished"></a>
# finished
finished(  ) &rarr; void



### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=finished&unscoped_q=finished">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="getLabelComponent"></a>
# getLabelComponent
getLabelComponent(  ) &rarr; JLabel

get the assigned label component, or create one if one has not been assigned.

### Returns:
the assigned label component

<a href="https://github.com/autoplot/dev/search?q=getLabelComponent&unscoped_q=getLabelComponent">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="setLabelComponent"></a>
# setLabelComponent
setLabelComponent( javax.swing.JLabel label ) &rarr; void

set the label to use for the progress monitor.

### Parameters:
label - the assigned label component

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=setLabelComponent&unscoped_q=setLabelComponent">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

