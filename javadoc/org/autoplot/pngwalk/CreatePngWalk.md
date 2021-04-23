# org.autoplot.pngwalk.CreatePngWalk

CreatePngWalk makes a sequence of images from a .vap file or the current state.
 This is used with PngWalkTool to quickly flip through the images once they
 are created.  This was once a Python script, but it got complex enough that it was useful to
 rewrite it in Java.

# CreatePngWalk( )


***
<a name="doBatch"></a>
# doBatch
doBatch( java.lang.String[] times, org.autoplot.dom.Application readOnlyDom, org.autoplot.pngwalk.CreatePngWalk.Params params, ProgressMonitor mon ) &rarr; int

run the pngwalk for the list of times.  The dom argument is copied so the
 scientist can continue working while the pngwalk is run.

### Parameters:
times - list of times to run.  If a time contains a ": ", then the first part is the label and after is the exact time.
<br>readOnlyDom - the dom to render for each time.
<br>params - outputFolder and spec.
<br>mon - progress monitor to provide feedback about the run.

### Returns:
0 if any were successful, 10 otherwise.

<a href="https://github.com/autoplot/dev/search?q=doBatch&unscoped_q=doBatch">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

doBatch( java.util.Iterator times, int size, org.autoplot.dom.Application readOnlyDom, org.autoplot.pngwalk.CreatePngWalk.Params params, ProgressMonitor mon ) &rarr; int<br>
***
<a name="doIt"></a>
# doIt
doIt( org.autoplot.dom.Application dom, org.autoplot.pngwalk.CreatePngWalk.Params params ) &rarr; int

run the pngwalk. If the params are null, then prompt the user with a GUI.
 The pngwalk is run by resetting the timeRange field of the vap to each step
 of the sequence.

### Parameters:
dom - the state from which a pngwalk is to be produced.
<br>params - a parameters structure (e.g. batch processing) or null.

### Returns:
an integer exit code where 0=success, 10=bad time format, 11=caught exception, 12=uncaught exception

<a href="https://github.com/autoplot/dev/search?q=doIt&unscoped_q=doIt">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="main"></a>
# main
main( java.lang.String[] args ) &rarr; void

command-line support for creating PNGWalks.  When PNGWalks are created 
 interactively in Autoplot, this is used as well.

### Parameters:
args - see the code for the argument list.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=main&unscoped_q=main">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

***
<a name="writeHTMLFile"></a>
# writeHTMLFile
writeHTMLFile( org.autoplot.pngwalk.CreatePngWalk.Params params, java.util.ArrayList pngFilenameArrayThumbs, java.util.ArrayList pngFilenameArrayBig, java.util.ArrayList timeLabels ) &rarr; void

Method to write HTML file of all the pictures to give a gallery view

### Parameters:
params - a CreatePngWalk.Params
<br>pngFilenameArrayThumbs - a java.util.ArrayList
<br>pngFilenameArrayBig - a java.util.ArrayList
<br>timeLabels - a java.util.ArrayList

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=writeHTMLFile&unscoped_q=writeHTMLFile">[search for examples]</a>

<a href="https://github.com/autoplot/documentation/blob/master/javadoc/index-all.md">[return to index]</a>

