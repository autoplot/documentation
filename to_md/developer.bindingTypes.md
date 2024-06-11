Purpose: Place for thinking about more types of bindings than simple
two-way synchronization.

I just came across a place where it would be nice to be able to bind two
automatically-set properties as long as neither is set manually. This
starts to hint at the need for a more formal convention for having
properties that are manually and automatically set. (Currently the
DomNode has a second property autoX for property X, e.g. label and
autoLabel.)
