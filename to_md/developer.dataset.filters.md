Purpose: Define interface for dataset filter extensions for QDataSet,
Autoplot, and TSDS. The goal is to have an interface that allows for the
definition of high and low level data operators. High level operators
use timetags and other metadata. Low level operators simply work on the
data in an array.

Audience: Autoplot power users and TSDS server team, TSDS power users.

# Definition of a filter

## Zero-parameter filter

Dataset piped through a filter yields another dataset.

` DataSet | Filter -> DataSet`

This example removes spikes using median-of-three filter:

` DensityDS | median3 -> cleanDensityDS `

## One-parameter filter

Dataset piped through a filter yields another dataset. The filter itself
takes a parameter, in parenthesis:

` DataSet | Filter(param) -> DataSet`

Here we smooth the data by running a 5-element boxcar average over the
data:

` DensityDS | boxcar(5) -> SmoothDensityDS`

## Streamable filter

A streaming filter is one where the processing is done locally on the
dataset, and the entire dataset needn't be accessible. The boxcar
filter,

` DensityDS | boxcar(5) -> SmoothDensityDS`

is streaming because once the boxcar calculation for point i is
complete, we needn't access point i-2 again.

## Non-Streamable filter

A non-streaming filter is one where all of the input data must be
available before processing can be performed. For example the fft
filter,

` WaveformDS | fft > FFTResultDS`

is non-streamable.

## Filters cannot have datasets as parameters

No. When multiple datasets are to be processed, for example with cross
correllation, the two datasets should be bundled (QDataSet parlance,
aggregated in NetCDF) into one dataset that is the argument:

` DS= bundle( Density1, Density2 )`  
` DS | innerProduct > Rho`

(Note Rho is a rank zero dataset.)

## Filters can change data structure

Filters can change data structure, for example changing rank in
QDataSet. In the above example, the bundle of rank 1 datasets is input,
and the rank zero Rho is output.

## Filter rank

A filter's rank is the rank, or number of dimensions, of its input. The
canonical filter has rank 1 and returns a rank 1 dataset. When the
output dataset rank is less than the input, then this is a
"rank-reducing" filter. When the dataset rank is the same, then it is a
"rank-preserving" filter.

## Filter rank promotion

Any filter's rank can be promoted to handle higher-rank datasets. For
example, the rank 1 filter fft can be used to handle a rank 2 input
(double\[\]\[\], an array of arrays) by applying the filter to each of
its rank 1 double array elements.

# Implementation API

We specify the API with a Java interface. The goal is to allow for
filter specification in Java and Python. High-level filters should be
created using low-level filters when possible.

## Arrays

Filters can be defined using Java double arrays. This may seem verbose,
and we would like for the canonical double\[\] in, double\[\] out to be
easy to define. Note that if the output is rank zero, then a one-element
double array is returned and outputRank() should return 0.

` interface ArrayFilter {`  
`    String name();   // Java identifier: [a-z,A-Z,_][a-z,A-Z,0-9,_]*`  
`    String label();  // Human consumable label for the filter, often the same as name()`  
`    String title();  // One-line description of the filter`  
`    int rank();        // number of dimensions of the input.`  
`    int outputRank();  // number of dimensions (0..4) of the result`  
`    Object doFilter( double[] in, ... );`  
`    Object doFilter( double[][] in, ... );`  
`    Object doFilter( double[][][] in, ... );`  
`    Object doFilter( double[][][][] in, ... );`  
` }`

An abstract class is used so that just two methods need to be defined:

` class NoOp extends AbstractFilter {`  
`    Object doFilter( double[] in ) {`  
`        return in;`  
`    }`  
` }`

In AbstractFilter:

  - name() returns the name of the class, without the package name.
  - label() returns name().
  - title() returns label().
  - rank() returns 1.
  - outputRank() returns rank();
  - each doFilter() implementation throws IllegalArgumentException, and
    rank() defines which must be defined.

## QDataSets

Syntax is more concise when using QDataSet:

` interface QDataSetFilter {`  
`    String name();   // Java identifier: [a-z,A-Z,_][a-z,A-Z,0-9,_]*`  
`    String label();  // Human consumable label for the filter, often the same as name()`  
`    String title();  // One-line description of the filter`  
`    int rank();      // number of dimensions of the input`  
`    int outputFilter();  // number of dimensions (0..4) of the result`  
`    QDataSet doFilter( QDataSet in );`  
` }`

## Python

We wish to provide a language for defining filters that is as efficient
as possible.

` class accum:`  
`    def doFilter( self, a ):`  
`       result= zeros(len(a))`  
`       result[0]= a[0]`  
`       for i in range(1,len(a)):`  
`          result[i]= result[i-1]+a[i]`  
`       return result`

# Examples

## Java using double arrays

median3 filter. Not for use, unverified\!

`public class Median3 extends AbstractFilter {`  
`  double median3( double a1, double a2, double a3 );  // implementation removed for brevity`  
`  Object doFilter( double[] in ) {`  
`      double t1= in[1];`  
`      double t2= in[2];                               // not verified, do not use`  
`      double[] result= new double[in.length];`  
`      for ( int i=0; i<in.length; i++ ) {`  
`         result[i]= median3( t1,t2,in[i] );           `  
`         t1= t2;`  
`         t2= in[i];`  
`      }`  
`      return result;`  
`  }`  
`}`

## Python with double array

`class Median3(AbstractFilter): `  
`   def doFilter( in ):`  
`      t1= in[1]`  
`      t2= in[2]`  
`      n= len(in)`  
`      result= zeros(n)`  
`      for i in range(n):`  
`         result[i]= median3( t1,t2,in[i] )`  
`         (t1,t2)= (t2,in[i])`  
`      return result   `

## Python with QDataSet (note it's very similar to the array code)

`class Median3(AbstractFilter): `  
`   def doFilter( in ):`  
`      t1= in[1]`  
`      t2= in[2]`  
`      n= len(in)`  
`      result= zeros(n)`  
`      for i in range(n):`  
`         result[i]= median3( t1,t2,in[i] )`  
`         (t1,t2)= (t2,in[i])`  
`      return result`

# Use Cases

## Autoplot URIs

[http://www.autoplot.org/data/noisy.cdf?BGM|median3](http://www.autoplot.org/data/noisy.cdf?BGM%7Cmedian3)

\== TSDS Data Requests =
