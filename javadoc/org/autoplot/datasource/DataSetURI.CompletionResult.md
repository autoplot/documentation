# org.autoplot.datasource.DataSetURI.CompletionResultRepresents a single suggestion in a completion list.  For example,
 http://autoplot.org/data/versioning/data_&lt;C&gt; would result in completions for each file in the folder,
 and the aggregation, and each is represented by one completion result.  The completion result contains
 the human-readable label and a documentation string, as well as the replacement text.
***
<a name="completion"></a>
# completion

the suggestion to replace the completeable string.

***
<a name="doc"></a>
# doc

human-readable documentation.

***
<a name="label"></a>
# label

human-readable label.

***
<a name="completable"></a>
# completable

the string that will be replaced, or null.

***
<a name="maybePlot"></a>
# maybePlot

If true then the service-provider code believes this completion should be usable after the completion.

***
<a name="SEPARATOR"></a>
# SEPARATOR



