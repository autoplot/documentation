Ed West and Jeremy were talking about how conventions could be
introduced to support reading in multiple datasets in one pass. For
example, with an ascii file you want to read in Y(T). This is common,
and we support doing this in one pass with DEPEND\_0 keywords. But what
if you also want to read in DEPEND\_1? I've added keywords for this too.
Now someone wants to do similar for the binary reader, but can't until I
implement it. What if instead there were conventions for how these are
specified, and they can be specified uniformly?

Instead of:

```
x= vap+bin:/tmp/foo.bin?recLength=16&recOffset=4
y= vap+bin:/tmp/foo.bin?recLength=16&recOffset=8
plot( x,y )
```
You would have:

```
ds= vap+bin:/tmp/foo.bin?recLength=16&dep0.recOffset=4&recOffset=8
plot( ds )
```
This would implicitly create a DEPEND\_0 dataset read in with the same
arguments, except for recOffset. Or more importantly:

```
x= vap+bin:/tmp/foo.bin?recLength=16&recOffset=4&byteOffset=16
z= vap+bin:/tmp/foo.bin?recLength=16&recOffset=8&byteOffset=16
y= vap+bin:/tmp/foo.bin?recLength=16&recOffset=8&byteOffset=0&recCount=1
plot( x,y,z )
```
becomes:

