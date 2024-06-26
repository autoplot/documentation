Purpose: Serve as a place for notes about the science data interace
developed with Jon V. and others at APL.

Audience: Jon V and others at APL, Jeremy

# The Task

Provide a simplified dataset interface that is strongly typed and easier
to use than QDataSet. QDataSet is intentionally weakly typed, so that it
can be translated to many environments. This has made it difficult to
use.

# Names for things

## Physical Dimensions

Number of physical dimensions. The arrows (→) should be read "yields."
Lower case i,j,and k refer to an indices.

| \# of Dimensions |                                             | SDI                 | QDataSet                                                                       |
| ---------------- | ------------------------------------------- | ------------------- | ------------------------------------------------------------------------------ |
| 2                | X(i)→Y(i)                                   | XYData,BinnedData1D | Rank 1 DataSet with DEPEND\_0                                                  |
| 3                | X(i),Y(j)→Z(i,j)                            | BinnedData2D        | Rank 2 DataSet with DEPEND\_0 and DEPEND\_1                                    |
| 3                | X(i),Y(i)→Z(i)                              | XYZData             | Rank 2 DataSet with BUNDLE\_1=\[X,Y,Z\]                                        |
| 4                | T(i)→X(i),Y(i),Z(i)                         |                     | Rank 2 DataSet with BUNDLE\_1=\[T,X,Y,Z\] X has property DEPENDNAME\_0=T, etc. |
| 4                | Time(i),Energy(j),PitchAngle(k)→Flux(i,j,k) |                     | Rank 3 DataSet with DEPEND\_0=Time, DEPEND\_1=Energy, DEPEND\_2=PitchAngle     |

## Contiguous Coverage

Is the dimension coverage contiguous? We can define interfaces that
assert the contiguous coverage by only allowing access to the lower
boundary and the highest bin boundary.

## Simple and Rich Datasets

We break up data into two classes, not having metadata (SimpleXXX) and
having metadata (XXX). In addition to having metadata, rich datasets
provide a FillDetector and UncertaintyProvider.

# Glossary

Here is a pile of commonly used words.

**Cadence** The expected spacing between measurements. QDataSet.CADENCE
is this value, and is a rank 0 dataset, but rank 1 may be allowed a
future version.

**Aliasing Interval** accumulation time for the measurement, meaning the
measurement should be applied with equal probability during this time.

**Duration** Another word for **Aliasing Interval**

**Units** define a physical dimension. E.g. "seconds since
2000-01-01T00:00" or "Kg"

**Datum** defines a point within a physical dimension. E.g.
"2015-03-15T14:45" or "95.2 Kg"

**Basis** Special point within a physical dimension that is 0. For
example in "seconds since 2000-01-01T00:00" the basis is
"2000-01-01T00:00"

**DatumRange** defines an interval within a physical dimension. Used
throughout Das2 and Autoplot.

**Bin** defines an interval within a physical dimension, but also
contains a reference Datum.

**Rank** QDataSet term for the number of integers needed to index a
value in a dataset.

**Dimensionality** The number of physical dimensions a dataset occupies.
