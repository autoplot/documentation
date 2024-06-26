Purpose: specify panel rank reduction and implementation details.

Audience: Autoplot developers

See also:
<https://sourceforge.net/tracker/index.php?func=detail&aid=2809825&group_id=199733&atid=970682>

Currently Autoplot's DataSourceFilter objects will reduce a rank 3
dataset to rank 2 for plotting. This was introduced to provide access to
rank 3 data early in Autoplot's development. This has a number of
shortcomings:

  - multiple slices of the same dataset cannot be displayed without
    loading the data for each slice.
  - only slices can be displayed, not collapsed (averaging over a
    dimension) data.
  - rank 2 data cannot be sliced using this mechanism to provide a rank
    1 view.
  - rank 4 data cannot be sliced twice to provide a rank 2 view.
  - future renderings of data may support viewing rank 3 data.
  - this is not extensible, for example allowing new slice types.

# proposed solutions

## dataSourceFilters

allow dataSourceFilters to filter another dataSource. This leverages
existing mechanisms, for example where the URI is
vap+internal:data\_1,data\_2. This means that panels would need the
authority to add dataSourceFilter nodes to reduce the data to an
acceptable rank.

### Example Specs

` data_1|slice0(23)`  
` data_1|slice0(23)|slice0(2)`  
` data_1|trim1(23,40)|histogram`  
` data_1|slice(energy=23)|slice(angle=2)`  
` data_1|collapse(where energy>1000)`  
` data_1(where data_2>0)    sql-like queries`

## panels

extend the panel node's component property, which is just special a
slice of the data, to include a full API.

### Example Specs

` Bx     display a component to support legacy behavior`  
` |slice0(23)   pipe indicates non-component`  
` |collapse()   reduce the last dimension by averaging all leaf elements.`

# Use Cases

Rank 4 data is loaded from a CDF and the user wants to view rank 2
slices of the data. Autoplot resolves the rank 4 dataset and guesses the
two dimensions for slicing. It provides a GUI to allow control of the
two slices, and instead of slicing the user can trim and collapse a
dimension instead. Title is updated to indicate slice location.

Support Bob's data filters, such as smoothing the data before viewing.
Allow for view of histogram of the dataset.

Support view of dataset when other conditions are true.
data\_1(where(data\_2.gt(0.) and data\_3.gt(1000.)))

Slicing spectrogram panel configures the slice in the lower panel. This
might mean that the lower panel's rank reduction spec (component
property) would be bound to the upper panel's slice position.

# Implementation

Extending panel component behavior is the lowest impact way to introduce
the functionality. The code that decides to break up a spectrogram into
components is similar to what would be needed when a high-rank data set
is encountered and must be sliced for display. It's possible that both
should be introduced, so that operations can be performed in both the
model and view of the data.

Performance is an issue, because we want to support slicing data on an
animation-interactive time scale. This probably excludes the possibility
of using Jython to implement. A parser that doesn't limit speed will be
developed.

Clearly these specs are like URIs in that they are complex enough that
humans won't be constructing them. Instead GUIs are provided to
construct them.

dataSourceFilter.sliceIndex equal to -1 indicates that there should be
no slicing. Legacy vaps should still work, except for the case where
sliceDimension=0 and sliceIndex=0. This should not be difficult to deal
with, because of the small number of vaps in the wild, and known
instances were not slicing on the first dimension.
