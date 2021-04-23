# org.autoplot.pngwalk.CreatePngWalk.Params

parameters specifying the creation of a pngwalk.

# Params( )


***
<a name="outputFolder"></a>
# outputFolder

output folder for the walk, e.g. /home/user/pngwalk/

***
<a name="timeRangeStr"></a>
# timeRangeStr

timerange to cover for the walk, e.g. 2012 through 2014.

***
<a name="rescalex"></a>
# rescalex

rescale to show context for each step, e.g. "0%,100%" or "0%-1hr,100%+1hr"

***
<a name="autorange"></a>
# autorange

autorange dependent dimensions

***
<a name="autorangeFlags"></a>
# autorangeFlags

consider autorange flags for each axis.

***
<a name="runOnCopy"></a>
# runOnCopy

clone the dom and run on the copy, so the original Autoplot is free.

***
<a name="version"></a>
# version

version tag to apply to each image, if non-null

***
<a name="product"></a>
# product

product name for the walk, e.g. product

***
<a name="timeFormat"></a>
# timeFormat

timeformat for the walk, e.g. $Y$m$d

***
<a name="batchUri"></a>
# batchUri

Uri that creates an events dataset, like 
 'http://emfisis.physics.uiowa.edu/events/rbsp-a/burst/rbsp-a_burst_times_20130201.txt?eventListColumn=3'
 or null for automatically generating names based on template.

***
<a name="useBatchUri"></a>
# useBatchUri

if true, use the URI to source the list of events.

***
<a name="batchUriName"></a>
# batchUriName

if non-null, use the name in the event list column instead of the 
 product and timeFormat.  For example,
 the batch file contains lines like:
 2015-03-05T02:10 2015-03-05T02:14 marsex/event1
 so this png will have the name outputFolder + "marsex/event1" + ".png"
 This must be either empty "" or "$o" for now.

***
<a name="createThumbs"></a>
# createThumbs



***
<a name="update"></a>
# update

if true, skip over products that appear to be created already.

***
<a name="outputFormat"></a>
# outputFormat

presently this is png or pdf

***
<a name="writeVap"></a>
# writeVap

also write a .vap file

***
<a name="removeNoData"></a>
# removeNoData

check that image contains data.

***
<a name="toString"></a>
# toString
toString(  ) &rarr; String



### Returns:
java.lang.String


<a href="https://github.com/autoplot/dev/search?q=toString&unscoped_q=toString">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

