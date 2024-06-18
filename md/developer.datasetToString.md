Purpose: lock down behavior of toString in QDataSet

Audience: developers and power users

# Introduction

A script of Sebastian's uses the rank zero toString() to grab the
formatted value and insert it into a vap+inline URI:

```
ds= dataset('2015-01-01T00:00')
ds= putProperty( ds, QDataSet.NAME, 'startTime' )
print ds  # prints startTime=2015-01-01T00:00:00.000Z

dsst= ds.toString()
i= dsst.index('=')
print dsst[i+1:]
```
I've been thinking for a while about what the toString method should
print for toString on a rank 0 dataset. This is loose and colloquial,
but clearly this code from the wild shows that some thought and
standardization is needed.

Note that just about every dataset implementation uses
org.virbo.dataset.DataSetUtil.toString( QDataSet ds ) to represent the
dataset.

# Rank 0 Datasets

Note that Datums and Rank 0 datasets are very similar, and should be the
same where they can be. For example, the output of the script:

```
datm= datum('2015-01-01T00:00')
ds= dataset('2015-01-01T00:00')
dsn= putProperty( copy(ds), QDataSet.NAME, 'dsn' )
print 'Datum: ', datm
print 'Dataset: ', ds
print 'Named Dataset: ', dsn
```
is:

```
Datum:  2015-01-01T00:00:00.000Z
Dataset:  2015-01-01T00:00:00.000Z
Named Dataset:  dsn=2015-01-01T00:00:00.000Z
```
So note there's a strange behavior where if the dataset is named then
the name is reported. Note also that it becomes somewhat ambiguous how
to get the formatted value out of the dataset, whether it is named or
not.

Since toString() must always be considered a human-readable function, so
this is somewhat colloquial, I suggest that this logic be continued and
the following logic should always work:

```
dsst= ds
i= dsst.find('=')
print dsst[(i+1):]
```
Note this logic happens to work for both cases, because of the +1.

When the dataset is an enumeration, then the value without the name
property (name=) should be returned.

Several years ago a new rank 0 accessor "svalue" was introduced, which
will give a string representation of the rank 0 data. "print
dsn.svalue()" shows the value without printing the name.

# Rank N datasets

When data is rank 1 or more, the toString method should show the dataset
name, the dimensions, and the units of the data.

```
ds= zeros(4,3)
ds.putProperty( QDataSet.NAME, 'ds' )
ds.putProperty( QDataSet.UNITS, Units.MeV )
print ds  # prints ds[4,3] (MeV)
```
The dimensions printed imply that the data is a QUBE (all 4 records have
length 3). When the data is not a qube, then the dimensions of the 0th
record are printed with an asterisk (\*):

```
ds1= zeros(4,3)
ds1.putProperty( QDataSet.NAME, 'ds1' )
ds1.putProperty( QDataSet.UNITS, Units.MeV )
ds2= zeros(4,5)
ds2.putProperty( QDataSet.NAME, 'ds2' )
ds2.putProperty( QDataSet.UNITS, Units.MeV )
ds= join(ds1,ds2)
ds.putProperty( QDataSet.NAME, 'ds' )
print ds  # prints ds[2,4*,3*] (MeV)
```
Datasets without a name may appear with the implicit name "dataset," for
example:

```
ds= zeros(4,3)
print ds  # prints dataset[4,3] (dimensionless)
```
Note too that dataset should appear as "dataset" and not "dataSet" (I
could break out into a rant here about where camel case should be used
and where everything should be lower case: xAxis vs xaxis. Autoplot vs
AutoPlot. starttime vs startTime. timerange vs timeRange. QDataSet vs
QDataset.)

# value and slice

The method slice was introduced several years after QDataSet was begun,
and it's proved to be useful as a method for grabbing values with all
their metadata. This should be encouraged.

The svalue method will show a string representation of the rank 0 data
set. The capability LongReadAccess provides a means of reading the
values of longs, when available.

```
from org.das2.qds import LongReadAccess
ds= getDataSet('vap+cdaweb:ds=RBSP-A_DENSITY_EMFISIS-L4&filter=rbsp&id=y&timerange=2019-10-12')
tt= xtags(ds)
ll= tt.capability(LongReadAccess)
print ll.lvalue(0)
```
# bins datasets

Bins datasets have a special case that is used often, where
BINS\_0='min,max'. This should be formatted as a DatumRange would be.

```
ds= dataset([0,3600])
ds= putProperty( ds, QDataSet.UNITS, Units.t2000 )
ds= putProperty( ds, QDataSet.BINS_0, QDataSet.VALUE_BINS_MIN_MAX )
print ds  # prints "2000-01-01 0:00 to 1:00"

ds= dataset([[0,3600],[7200,9800],[86400-3600,86400]])
ds= putProperty( ds, QDataSet.UNITS, Units.t2000 )
ds= putProperty( ds, QDataSet.BINS_1, QDataSet.VALUE_BINS_MIN_MAX )
print ds  # prints "dataset[3,min max] (t2000)"
```
# commas and semicolons

When it is appealing to separate items within a label by a comma, then a
semicolon should be used to delimit the dimensions. This is to make way
for BUNDLES, where it would be nice to show each column name.

```
ds= getDataSet('`<http://autoplot.org/data/crres_orbits.dat?bundle=>`:')
print ds  # prints "dataset[1061,DEPEND_1=3] (dimensionless)"   
# this should print "dataset[1061;st,en,orbit]"
```
TODO: why is the events mode not automatically detected for this file?

