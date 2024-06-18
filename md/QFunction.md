# Definitive Guide to QFunctions

A QFunction is a representation for a data function that tries to reuse
as much of the QDataSet interface as possible. A QFunction takes N
parameters as input and returns M parameters as output. The QFunction
interface is simply a value() method that takes a rank 1 dataset as
input and returns a rank 1 dataset as output. Also a method
exampleInput() returns an example of an input used for the function.
This allows for discovery of the function, identifying units, valid
ranges, and cadences for inputs.

```
 interface QFunction {
   QDataSet value( QDataSet in );   // rank 1 input of N parameters and rank 1 output of M values.
   QDataSet exampleInput();
 }

 class DemoFunction implements QFunction {
   public QDataSet value( QDataSet in ) {
       return Ops.sin( in );
   }
   public QDataSet exampleInput() {
       MutablePropertyDataSet bds= new DDataSet(2,1);
       bds.putProperty( 0, QDataSet.UNITS, Units.dimensionless );
       bds.putProperty( 0, QDataSet.TYPICAL_MIN, -Math.PI );
       bds.putProperty( 0, QDataSet.TYPICAL_MAX, Math.PI );
       DDataSet v= DDataSet.wrap( 0. );
       v.putProperty( QDataSet.BUNDLE_0, bds );        
       return v;
 }
```
This is slightly extended to simplify implementations and allow for more
efficient use when multiple invocations will be made:

```
 interface QFunction {
   QDataSet value( QDataSet in );   //
   QDataSet values( QDataSet in );  // rank 2 input and rank 2 output.
   QDataSet exampleInput();         // 
   QDataSet exampleOutput();        // call this when you just need the output.
 }
```
Note that implementations of a QFunction may simply check the BUNDLE\_0
property has not changed to know that none of the properties have
changed.

Here is how QDataSet properties are interpreted in this case:

```
    * discover an example input.  Result is a rank 1 bundle QDataSet.
    *   QFunction ff= TestFunction();
    *   ff.exampleInput().length();  // how many parameters the function takes
    *   QDataSet bds= ff.exampleInput().property( QDataSet.BUNDLE_0 );  // get the bundle descriptor
    *   ; to discover properties of the first (0th) parameter:
    *   bds.slice(0).property( QDataSet.UNITS )       // function should handle convertible units (e.g. TimeAxes Ephemeris).
    *   bds.slice(0).property( QDataSet.VALID_MIN )   // absolute limits of domain of the function
    *   bds.slice(0).property( QDataSet.VALID_MAX )
    *   bds.slice(0).property( QDataSet.TYPICAL_MIN ) // domain of the function parameter
    *   bds.slice(0).property( QDataSet.TYPICAL_MAX )
    *   bds.slice(0).property( QDataSet.CADENCE ) // granularity of the function parameter
    *   bds.slice(0).property( QDataSet.LABEL )   // label for the parameter
    * slice(0) is the first argument, slice(1) would be the second, etc.
    * This would be a bundle.
```
# Rank handling

QFunctions have two methods: value() and values(). `value` always takes
a rank 1 bundle. Even if this is just one parameter, then this must be a
bundle of the one parameter. `values` is always a rank 2. The class
AbstractQFunction is intended to simply writing QFunctions by
implementing a values method that calls the value method for each input
of the rank 2 array. This allows the QFunctions to be implemented more
efficiently when a lookup must be done before a result can be formed.
For example, at the Plasma Wave group, we implement functions by posting
the input to a server and then returning the result.

