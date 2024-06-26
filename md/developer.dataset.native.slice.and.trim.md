Purpose: discuss the rationale for "native," or implementation specific,
slice and trim operations that are attached to the datasets, and how
they should be implemented.

# Define Slice and Trim

Consider a rank 3 dataset. This is a set of rank 2 datasets (and each of
those is a set of rank 1, and so on). Slicing is extracting one of the
rank 2 datasets. Analogies:

```
  "hello".charAt(4)='o'
  ([[2,3,4],[4,5,6],[6,7,8]])[1]= [4,5,6]
```
DataSetUtil.slice0(QDataSet,int) has defined slicing thus far.

Trimming is taking a subset of a dataset. It takes to integer arguments,
the start and end.

```
  "hello".trim(1,3)= "el"
  ([22,23,24,25,26,27,28]])[1:3]= [23,24]
```
There is no stride argument for subsetting.
DataSetUtil.trim(QDataSet,int,int). Negative indexes are allowed.

Iterating is accessing each value of the dataset sequentially, and
should be considered as well. This is a depth-first decent, so the first
index of the rank 3 dataset will be \[0,0,0\], the second will be
\[0,0,1\], and etc. (The last index elements should be packed tightest
in memory, and have the most relevance to one another.) See
QubeDataSetIterator.

Issues to consider with iteration: should the dependencies be reflected
as well? Iterator can return a sequence of rank 0 datums with CONTEXT
property set to retain all dataset information and to provide "flatten"
operation as well. (Often clients just want the physical dimensions.)
This can also be thought of as slicing down to rank 0 for each point.
Alternatively, this can be seen as an alternate way to access all the
numbers, for example to do statistics. Should invalid points be skipped?
This would simplify client codes...

# Current Implementation

These are implemented presently by wrapping datasets. For example,
DataSetOps.slice0(ds) returns a Slice0DataSet that wraps ds, reducing
its rank and hiding the first dimension. This means that as each element
of the sliced dataset is accessed, a stack of method calls accesses the
original dataset. We've found over the years that Java does this
efficiently and it's been reasonable to "code it once correctly" than to
worry about efficient access. As higher rank datasets are introduced
(rank 4 was introduced four months ago), it seems likely that a
significant performance gain is to be had, justifying the use of
dataset-implemention specific slice, trim, and iterator operators.

# Proposed Extensions to QDataSet as implemented in Java

## Capabilities Method

The capabilities method allows the dataset to be queried to see if it
supports an interface. Presently this is done by inheritance and
instanceof is used to check.

```
 QDataSet<-MutablePropertiesDataSet<-WritableDataSet
```
Instead, we use calls to the capabilities method:

```
 ds= DDataSet.createRank1(100);
 WriteCapability write= ds.capability( WriteCapability.class );
 write.putValue( 99, -1e31 );
```
This has the virtue of allowing capabilities to be removed, and existing
objects extended. (We need to consider putCapability as well.)

This also allows datasets to advertise capabilities that they are very
good at. For example, a rank 3 DDataSet is implemented with a 1-D double
array, yet a complex DataSetIterator is typically used to iterate
through the points.

Note the use of capabilities should be limited to when the implementor
can clearly write a superior implementation to the default
implementation. Any client code must handle the typical case when a
capability is not available.

## Should Slice and Trim be Capabilities or Extensions to the QDataSet Interface

Slice and trim are very basic dataset operations. As of now, these are
only performed by wrapping existing datasets, and are not "native"
operations. Clearly these native operations need to be made accessible,
but should this be through the capabilities interface or as an extension
to QDataSet? Here it is as a capability:

```
 ds= DDataSet.createRank2( 5,30 );
 Slice s= ds.capability( Slice.class );
 if ( s!=null ) s.slice( 1 )
```
The lookup could be buried in DataSetOps.slice0, and the dataset wrapper
avoided. So there is no additional syntax burden here.

If it were an extension to the interface:

```
 ds= DDataSet.createRank2( 5,30 );
 ds.slice( 1 )
```
but then dataset implementations must implement this as well. Note that
most datasets extend AbstractDataSet, and this is not overly burdensome.

**NOTE:** slice and trim were added to the QDataSet interface a while
back.

