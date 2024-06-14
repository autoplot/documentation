Purpose: outline data set traps.

# Introduction

QDataSet is the result of looking at the limitations of data models
attempted over the years, and trying to create a model that was flexible
enough to work in many situations. With this flexibility it is able to
adapt, but people have a tough time understanding it. Further, it has
the problem that it's so unconstrained that the hundreds of methods that
use it might as well be passing Objects around, you don't know which
scheme of any dataset from the interface.

# X,Y,Z,?

When using X, Y, and Z in your model, you will be trapped into locking
your data model to the display, and you won't be able to model high
dimensionality (and also single-dimensionality). Suppose you have Flux
sampled at Time, Energy, and Pitch Angle. Maybe Time is clearly "X" and
Flux is clearly "Z", but you can see why this breaks down quickly.

# Scalars

When using X, Y, and Z in your model, you will be trapped into locking
your data model to the display, and it's not clear how you would
describe scalars (single-dimensionality). Suppose you wish to model
scalars, indicating an event time. Would the interface just have a
getX() method? Suppose you want to indicate an Energy, so should this be
getY()?

# Names for Dimensionality

Tables have two indexes. Qubes have N indexes. In QDataSet, the rank
function returns the number of indices, and you can say rank 2 dataset
instead of Table. What should the thing with one index be called? In the
old Das2 model we called these "Vectors" which was a bad name. Here are
suggested names:

| X             | SDI           | QDataSet       |
| ------------- | ------------- | -------------- |
| Number        |               | Rank 0 DataSet |
| Array         | XYData,Data1D | Rank 1 DataSet |
| Table         | Data2D        | Rank 2 DataSet |
| ThreeQube (?) |               | Rank 3 DataSet |
|               |               | Rank 4 DataSet |

And words to avoid, because they have other definitions that cause
confusion: Scalar, Vector, Matrix

Note in QDataSet, the rank is quite different than the dimensionality.
Both a simple spectrogram and a table of N columns are both rank 2, but
the spectrogram occupies three dimensions, while the table occupies N
dimensions. (The BUNDLE\_1 property is used to differentiate.)

# Zeroth vs First

This still bugs me, where humans want to count things with natural
numbers, but indexes should clearly start at 0. TODO: there must be
guidelines for this, and this should be considered.

# Cadence vs Duration

Cadence is the spacing between measurements, which is different than the
duration of a measurement.

# Ratiometric spacing

Ratiometric spacings come up a lot in our field, where you have channels
whose centers increase logarithmically. "decibels" and "percentIncrease"
are good units for describing the cadence with a single number.

# Times can be modeled as double since Datum

Times can be modeled effectively with a double and a unit that contains
a Datum, such as "seconds since 2010-01-01T00:00."

# Tags should identify centers, Bins identify ranges, but the best is to identify all three

  - When just one number is used to identify a location with an aliasing
    interval, it must be the center of the interval.
  - If an aliasing interval bin must be described, then have a bin with
    a start and end so there is nothing implicit.
  - The best case would be to have all three numbers.

