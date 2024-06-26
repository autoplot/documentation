Introduction of DOM. ApplicationModel is gutted, factoring out code into
the dom package. ApplicationModel fields are factored out into dom
elements like Panel, Axis, DataSourceFilter, and Options. Its methods
are factored out into dom element controllers like PanelController and
DataSourceFilterController. This allows Autoplot to represent complex
states with many panels, and sorts out the mess of code in
ApplicationModel out into agents that just what they need to know.

# What's a DOM node?

DomNodes should contain either immutable properties (such as String or
Datum), or other DomNodes as children. They can contain other fields,
but the accessors should not use "get" and "set" which identify
properties.

Often nodes will have a getController() method. The controller has
methods that affect the node, and contains data implementing the DOM
node's state. For example, the Panel node contains information about the
dataset and rendering options, but it is the PanelController that
contains the das2 Renderer object and ensures it contains the correct
QDataSet.

# Pitfalls

## Node copy

### Deep Copy

A deep copy is needed to make state support and serialization work. It's
easy to fail to make a deep copy, because clone will create a shallow
copy that seems to work.

Solution: Clients should use "copy" to make copies of DOM elements, even
though they are Clonable.

### Property Change Support Copied

Clone is used for Node copy, which copied the propertyChangeSupport as
well. Changes to the copy notified listeners to the original. Same thing
for the controller...

Solution: All nodes should call the DomNode base class' copy, which will
clone and replace the propertyChangeSupport. This means copy is no
longer abstract, and implementers must be careful to copy and not clone
when children exist.

### Initialization actions in Constructor

Stuff happens (renaming the property change events) in the constructor,
so the copy needs to do this as well.

## Panels and Plots identity

copy and sync need to preserve object identity in copy and sync.

Solution: be careful and assert getPanels().contains(getPanel())
