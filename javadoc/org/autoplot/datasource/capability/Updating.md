# org.autoplot.datasource.capability.UpdatingUpdating allows the data sources to notify clients that a different dataset
 will be returned if they call getDataSet again.  Implementations should
 take into account that excessive update notifications may be ignored.

 Updates should be made by calling the registered listeners' propertyChange
 method, with an appropriate PropertyChangeEvent:

 listener.propertyChange( new PropertyChangeEvent( this, Updating.PROP_DATASET, null, null ) )
 to force the client to post a new request, or
    new PropertyChangeEvent( this, "dataSet", null, ds )
 if the dataset is trivially available.

 Developers should consider using java.beans.PropertyChangeSupport to
 implement this capability, so that it's firePropertyChange method can be used.
***
<a name="PROP_DATASET"></a>
# PROP_DATASET



***
<a name="addPropertyChangeListener"></a>
# addPropertyChangeListener
addPropertyChangeListener( java.beans.PropertyChangeListener listener ) &rarr; void



### Parameters:
listener - a PropertyChangeListener

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=addPropertyChangeListener&unscoped_q=addPropertyChangeListener">[search for examples]</a>

***
<a name="removePropertyChangeListener"></a>
# removePropertyChangeListener
removePropertyChangeListener( java.beans.PropertyChangeListener listener ) &rarr; void



### Parameters:
listener - a PropertyChangeListener

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=removePropertyChangeListener&unscoped_q=removePropertyChangeListener">[search for examples]</a>

