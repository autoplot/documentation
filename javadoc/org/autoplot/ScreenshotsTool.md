# org.autoplot.ScreenshotsToolJeremy's experiment that will create automatic documentation.
 This is intended to provide a means for users to more easily communicate and 
 to make it easier to create documentation.
 
 This is being modified a bit, namely to delay work such as screening
 private regions, to improve responsiveness and to allow the user the option
 of screening or not.
ScreenshotsTool( java.awt.Window parent, String outLocationFolder )
create a new ScreenshotsTool, which will write screenshots to the location.

ScreenshotsTool( java.awt.Window parent, String outLocationFolder, boolean clearFolder )
create a new ScreenshotsTool, which will write screenshots to the location.  The
 output folder must not exist or be empty, or clearFolder must be set to true.
 This is created and then pushed to the event stack, so that screenshots will
 be taken when activity occurs (see start which manages this), or will takePicture
 is called to manually take screenshots (e.g. from scripts).  When the
 session is done, requestFinish is called to clean up.

***
<a name="dispatchEvent"></a>
# dispatchEvent
dispatchEvent( java.awt.AWTEvent theEvent ) &rarr; void



### Parameters:
theEvent - an AWTEvent

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=dispatchEvent&unscoped_q=dispatchEvent">[search for examples]</a>

***
<a name="getScreenShot"></a>
# getScreenShot
getScreenShot(  ) &rarr; BufferedImage

get a screenshot of the display Autoplot's main UI is running within.

### Returns:
a java.awt.image.BufferedImage


<a href="https://github.com/autoplot/dev/search?q=getScreenShot&unscoped_q=getScreenShot">[search for examples]</a>

getScreenShot( int active ) &rarr; BufferedImage<br>
***
<a name="getScreenShotNoPointer"></a>
# getScreenShotNoPointer
getScreenShotNoPointer(  ) &rarr; BufferedImage

get a screenshot of the display Autoplot's main UI is running within, but without the pointer.

### Returns:
a java.awt.image.BufferedImage


<a href="https://github.com/autoplot/dev/search?q=getScreenShotNoPointer&unscoped_q=getScreenShotNoPointer">[search for examples]</a>

***
<a name="getTrim"></a>
# getTrim
getTrim( java.io.File root, ProgressMonitor monitor ) &rarr; Rectangle

return the common bounding rectangle to all png images in the directory.

### Parameters:
root - folder containing png images.
<br>monitor - progress monitor for the task

### Returns:
the rectangle common to all images.
### See Also:
<a href='#getTrim'>getTrim(java.awt.image.BufferedImage)</a> <br>

<a href="https://github.com/autoplot/dev/search?q=getTrim&unscoped_q=getTrim">[search for examples]</a>

getTrim( java.awt.image.BufferedImage source ) &rarr; Rectangle<br>
***
<a name="requestFinish"></a>
# requestFinish
requestFinish( boolean trimAll ) &rarr; void

This was introduced to provide a method for Jemmy tests to record videos 
 (so that videos are tested), but it looks like this won't work.  However
 this would probably be useful from scripts, so I will leave it.

### Parameters:
trimAll - trim off the portions of all screenshots which are not used.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=requestFinish&unscoped_q=requestFinish">[search for examples]</a>

***
<a name="start"></a>
# start
start( java.awt.Window parent ) &rarr; void

start should be called from the event thread.

### Parameters:
parent - the device

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=start&unscoped_q=start">[search for examples]</a>

***
<a name="takePicture"></a>
# takePicture
takePicture( int id ) &rarr; void

manually trigger a screenshot, which is put in the output directory.

### Parameters:
id - user-provided id (&le; 99999) for the image, which is the last part of the filename.

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=takePicture&unscoped_q=takePicture">[search for examples]</a>

takePicture( int id, String caption ) &rarr; void<br>
takePicture( int id, String caption, java.awt.Component c, java.awt.Point p, int buttons ) &rarr; void<br>
***
<a name="trim"></a>
# trim
trim( java.awt.image.BufferedImage image ) &rarr; BufferedImage

trim off the excess white to make a smaller image

### Parameters:
image - a BufferedImage

### Returns:
a java.awt.image.BufferedImage


<a href="https://github.com/autoplot/dev/search?q=trim&unscoped_q=trim">[search for examples]</a>

trim( java.awt.image.BufferedImage image, java.awt.Rectangle r ) &rarr; BufferedImage<br>
***
<a name="trimAll"></a>
# trimAll
trimAll( java.io.File dir ) &rarr; void

find the common trim bounding box and trim all the images in the directory.

### Parameters:
dir - a File

### Returns:
void (returns nothing)


<a href="https://github.com/autoplot/dev/search?q=trimAll&unscoped_q=trimAll">[search for examples]</a>

trimAll( java.io.File dir, java.awt.Rectangle r, ProgressMonitor monitor ) &rarr; void<br>
