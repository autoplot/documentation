# org.das2.dataset.DataSetAdapterPresents legacy das2 datasets as QDataSets. See also TableDataSetAdapter,VectorDataSetAdapter
DataSetAdapter( )


***
<a name="PROPERTY_SOURCE"></a>
# PROPERTY_SOURCE



***
<a name="create"></a>
# create
create( org.das2.dataset.DataSet ds ) &rarr; AbstractDataSet

Created a new QDataSet given a Das2 DataSet

 This function and createLegacyDataSet() are inverses, though a round trip conversion 
 is not guaranteed to preserve all properties

### Parameters:
ds - A Das2 Dataset

### Returns:
A new QDataSet

<a href="https://github.com/autoplot/dev/search?q=create&unscoped_q=create">[search for examples]</a>

***
<a name="createLegacyDataSet"></a>
# createLegacyDataSet
createLegacyDataSet( QDataSet ds ) &rarr; DataSet

Created a new Das2 DataSet given a QDataSet

 This function and create() are inverses, though a round trip conversion is not guaranteed to
 preserve all properties. Note that not all QDataSets can be represented as Das2 DataSets. If
 the given QDataSet has no Das2 analog, an IllegalArgumentException is thrown.

### Parameters:
ds - A QDataSet

### Returns:
A new Das2 DataSet
 
   DON'T USE THIS CODE!  Use org.das2.qstream.QdsToD2sStream IN THE QStream project!

<a href="https://github.com/autoplot/dev/search?q=createLegacyDataSet&unscoped_q=createLegacyDataSet">[search for examples]</a>

