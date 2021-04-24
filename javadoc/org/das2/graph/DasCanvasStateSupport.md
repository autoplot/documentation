# org.das2.graph.DasCanvasStateSupport

DasCanvasStateSupport is a registery where objects can tell the canvas they
 intend to mutate the canvas, so canvas clients should know that its result 
 may be incomplete.  This is first introduced to support server-side 
 processing, where in Autoplot the Autolayout feature knows then layout is 
 going to be adjusted, but doesn't have enough information to perform the 
 function.  
 
 Also, this may be used to address bugs like 
 https://bugs-pw.physics.uiowa.edu/mantis/view.php?id=303, 
 "strange intermediate states in transitions," since canvas painting can
 be halted while the change is being performed.

***
<a name="PROP_PENDINGCHANGES"></a>
# PROP_PENDINGCHANGES

someone has registered a pending change.

***
<a name="isPendingChanges"></a>
# isPendingChanges
isPendingChanges(  ) &rarr; boolean



### Returns:
boolean


<a href="https://github.com/autoplot/dev/search?q=isPendingChanges&unscoped_q=isPendingChanges">[search for examples]</a>
<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

