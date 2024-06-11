Purpose: define behavior of PyQDataSet.\_\_getItem\_\_(x) for all x. We
wish to have indexing similar to IDL and Matlab indexing, so scripts can
be ported and to reduce confusion. We wish to have strongly-typed index
lists as QDataSets, so that for example, the output of "where" can be
used to index data.

Index Types:

  - Python or Java scalar
  - Python or Java array
  - Python slice (QDataSet trim)
  - Rank 0 QDataSet for slicing.
  - Rank N QDataSet
  - "index trim" descriptor QDataSet
  - "indexes list" QDataSet

The expression SRC\[IDX\] will result in the following:

# IDX is a scalar

Dereference that element. This would create a rank N-1 dataset. This
would be converted to a double if rank 0 and used like a double, but
this creates a double right now.

# array, or N-index array

Coerce to QDataSet, use that logic.

# IDX

rank 0 dataset =

SRC=rank 0 dataset: rank limit exception.

SRC=rank 1 dataset: return scalar (not rank 0 dataset) at the index.

SRC=rank N dataset: return slice at the index.

Note for Rank 3 dataset, SRC\[0\] is equivalent to SRC\[0,:,:\]

# IDX

rank 1 dataset =

SRC=rank 0 dataset: rank limit exception.

SRC=rank 1 dataset: return rank 1 dataset that is the subset.

SRC=rank N dataset: return rank N dataset that is the join of the slices
at each index.

# IDX

rank N dataset with geometry G =

SRC=rank 0 dataset: rank limit exception.

SRC=rank 1 dataset: return rank N dataset with geometry G, with values
from rank 1 dataset.

SRC=rank 2 dataset: rank limit exception.

# IDX

rank 2 qube dataset with qube size=\[N,R\] with BUNDLE\_1 set. ("indexes
list") =

SRC=rank 0 dataset: rank limit exception.

SRC=rank 1 dataset and R=1: return rank 1 dataset that is the subset
containing N points.

SRC=rank R dataset: return rank 1 dataset that is the subset containing
N points.

Notes: BUNDLE\_1 should have length R. length(i)=0 (bundle of rank 1).
property(VALID\_MAX,i)=ds.length might be used to hint at the dimension
size it should index. property( FILL,0 )=ds.length

# IDX is a tuple (SRC(IDX0,IDX1,...,IDXR))

  - if R does not equal SRC rank, rank exception.

<!-- end list -->

  - If each IDXi is a rank 0 dataset (scalar), return the value at this
    index.

<!-- end list -->

  - For each IDXi, if IDXi is a rank 0 dataset, perform the slice on
    this dimension.

<!-- end list -->

  - For each IDXi, if IDXi is a trim (slice in python, rank 1 bins
    dataset in QDataSet), perform the trim on this dimension. This
    should also include the cases where an all-element slice is used
    (SRC\[2,3,:\]).

<!-- end list -->

  - The remaining IDXi that are arrays of indexes must have the same
    geometry. The result dataset will have this geometry. (NOTE: this
    does not match IDL, for which this is only the case when all the
    indices are arrays of indexes.)

# Notes

Represent Python slice object (e.g. 3:11:2 in SRC\[3:11:2\]): rank 1
dataset. length=2. property(BINS\_0)="min,max". value\[0\]=3.
value\[1\]= 11. property(CADENCE)=2. A value \> property(VALID\_MAX)
indicates the start or stop is implicitly 0 or length.

Jeremy has started a script for the tests to verify this logic
(/home/jbf/ct/autoplot/tests/weigel/PythonIndexing.jy).

See <http://jfaden.net:8080/hudson/job/autoplot-test037/ws/indexing.jy>
